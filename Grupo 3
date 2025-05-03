<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Presentación Conductivismo - Grupo 3</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    .fade-in-up {
      animation: fadeInUp 0.8s ease-out;
    }
  </style>
</head>
<body class="bg-gray-900 text-white">
  <div class="max-w-5xl mx-auto py-10 px-4">
    <div id="slideContainer" class="relative w-full bg-black rounded-2xl overflow-hidden shadow-xl">
      <!-- Imagen principal -->
      <img id="slideImage" src="" class="w-full object-contain transition duration-300" alt="Diapositiva" />
      
      <!-- GIFs para slide9.png -->
      <img id="gif1" src="slide1.gif" class="absolute top-20 left-10 w-40 h-25" alt="GIF 1" />
      <img id="gif2" src="slide2.gif" class="absolute bottom-10 right-10 w-32 h-24" alt="GIF 2" />

      <!-- GIFs para slide10.png -->
      <img id="gif3" src="slide3.gif" class="absolute top-10 right-10 w-15 h-10" alt="GIF 3" />
      <img id="gif4" src="slide4.gif" class="absolute bottom-10 left-10 w-40 h-24 hidden" alt="GIF 4" />

      <!-- GIF para slide14.png -->
      <img id="gif5" src="slide5.gif" class="absolute top-16 left-20 w-90 h-80" alt="GIF 5" />
    </div>

    <div class="flex justify-between items-center mt-6">
      <button id="prevBtn" class="70bg-blue-600 hover:bg-blue-700 text-white px-5 py-2 rounded-xl disabled:opacity-50">Anterior</button>
      <span id="counter" class="text-lg font-medium">1 / 16</span>
      <button id="nextBtn" class="bg-blue-600 hover:bg-blue-700 text-white px-5 py-2 rounded-xl">Siguiente</button>
    </div>
  </div>

  <script>
    const slides = [
      'slide1.png',
      'slide2.png',
      'slide3.png',
      'slide4.png',
      'slide5.png',
      'slide6.png',
      'slide7.png',
      'slide8.png',
      'slide9.png',   // GIF 1 + 2
      'slide10.png',  // GIF 3 + 4
      'slide11.png',
      'slide12.png',
      'slide13.png',
      'slide14.png',  // GIF 5
      'slide15.png',
      'slide16.png'
    ];

    let current = 0;

    const img = document.getElementById('slideImage');
    const counter = document.getElementById('counter');
    const prev = document.getElementById('prevBtn');
    const next = document.getElementById('nextBtn');

    const gif1 = document.getElementById('gif1');
    const gif2 = document.getElementById('gif2');
    const gif3 = document.getElementById('gif3');
    const gif4 = document.getElementById('gif4');
    const gif5 = document.getElementById('gif5');

    const resetGIFs = () => {
      [gif1, gif2, gif3, gif4, gif5].forEach(gif => {
        gif.classList.add('hidden');
        gif.classList.remove('fade-in-up');
      });
    };

    const update = () => {
      const currentSlide = slides[current];
      img.src = currentSlide;
      counter.textContent = `${current + 1} / ${slides.length}`;
      prev.disabled = current === 0;
      next.disabled = current === slides.length - 1;

      // Ocultar todos los GIFs primero
      resetGIFs();

      // Mostrar los GIFs correspondientes con animación
      if (currentSlide === 'slide9.png') {
        gif1.classList.remove('hidden');
        gif2.classList.remove('hidden');
        gif1.classList.add('fade-in-up');
        gif2.classList.add('fade-in-up');
      }

      if (currentSlide === 'slide10.png') {
        gif3.classList.remove('hidden');
        gif4.classList.remove('hidden');
        gif3.classList.add('fade-in-up');
        gif4.classList.add('fade-in-up');
      }

      if (currentSlide === 'slide14.png') {
        gif5.classList.remove('hidden');
        gif5.classList.add('fade-in-up');
      }
    };

    prev.onclick = () => {
      if (current > 0) {
        current--;
        update();
      }
    };

    next.onclick = () => {
      if (current < slides.length - 1) {
        current++;
        update();
      }
    };

    update();
  </script>
</body>
</html>
