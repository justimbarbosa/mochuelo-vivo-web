<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mochuelo Vivo | Turismo Rural Comunitario y Biciturismo</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#f2f8f3',
                            100: '#e1efe4',
                            200: '#c5e0cb',
                            600: '#2d7a46',
                            700: '#236137',
                            800: '#1b4b2b',
                            900: '#153c22',
                        },
                        amber: {
                            500: '#f59e0b',
                            600: '#d97706',
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f9fbf9;
            color: #1f2937;
        }
        .hero-bg {
            background: linear-gradient(135deg, rgba(21, 60, 34, 0.92), rgba(45, 122, 70, 0.82)), 
                        url('https://images.unsplash.com/photo-1544197150-b99a580bb7a8?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
        }
        .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out, padding 0.3s ease;
        }
        .accordion-content.active {
            max-height: 300px;
        }
    </style>
</head>
<body class="antialiased text-gray-800">

    <!-- NAV BAR -->
    <header class="sticky top-0 z-50 bg-white/95 backdrop-blur-md border-b border-gray-100 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Logo -->
                <a href="#" class="flex items-center space-x-3 group">
                    <div class="w-11 h-11 bg-brand-600 rounded-xl flex items-center justify-center text-white shadow-md group-hover:bg-brand-700 transition-all">
                        <i class="fa-solid font-bold fa-bicycle text-xl"></i>
                    </div>
                    <div>
                        <span class="text-xl font-extrabold text-brand-900 tracking-tight block leading-none">Mochuelo Vivo</span>
                        <span class="text-xs font-semibold text-brand-600 uppercase tracking-widest">Conociéndonos en bici</span>
                    </div>
                </a>

                <!-- Desktop Nav Navigation -->
                <nav class="hidden lg:flex items-center space-x-6 font-medium text-sm text-gray-700">
                    <a href="#quienes-somos" class="hover:text-brand-600 transition-colors">Quiénes somos</a>
                    <a href="#mision-vision" class="hover:text-brand-600 transition-colors">Misión y Visión</a>
                    <a href="#servicios" class="hover:text-brand-600 transition-colors">Servicios</a>
                    <a href="#la-ruta" class="hover:text-brand-600 transition-colors">La ruta</a>
                    <a href="#montanas-bici" class="hover:text-brand-600 transition-colors">Montañas en bici</a>
                    <a href="#testimonios" class="hover:text-brand-600 transition-colors">Testimonios</a>
                    <a href="#como-llegar" class="hover:text-brand-600 transition-colors">Cómo llegar</a>
                    <a href="#faq" class="hover:text-brand-600 transition-colors">FAQ</a>
                    <a href="#contacto" class="hover:text-brand-600 transition-colors">Contacto</a>
                </nav>

                <!-- CTA Button -->
                <div class="hidden lg:flex">
                    <a href="https://wa.me/573025467899?text=Hola,%20quisiera%20más%20información%20sobre%20las%20rutas%20de%20Mochuelo%20Vivo" 
                       target="_blank"
                       class="inline-flex items-center px-5 py-2.5 rounded-full bg-brand-600 text-white font-semibold text-sm hover:bg-brand-700 transition-all shadow-md hover:shadow-lg">
                        <i class="fa-brands fa-whatsapp text-lg mr-2"></i> Reservar
                    </a>
                </div>

                <!-- Mobile Menu Button -->
                <button id="mobile-menu-btn" class="lg:hidden text-gray-700 hover:text-brand-600 focus:outline-none">
                    <i class="fa-solid fa-bars text-2xl"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden lg:hidden bg-white border-b border-gray-200 px-4 pt-2 pb-6 space-y-3">
            <a href="#quienes-somos" class="block px-3 py-2 rounded-md font-medium text-gray-700 hover:bg-brand-50 hover:text-brand-600">Quiénes somos</a>
            <a href="#mision-vision" class="block px-3 py-2 rounded-md font-medium text-gray-700 hover:bg-brand-50 hover:text-brand-600">Misión y Visión</a>
            <a href="#servicios" class="block px-3 py-2 rounded-md font-medium text-gray-700 hover:bg-brand-50 hover:text-brand-600">Servicios</a>
            <a href="#la-ruta" class="block px-3 py-2 rounded-md font-medium text-gray-700 hover:bg-brand-50 hover:text-brand-600">La ruta</a>
            <a href="#montanas-bici" class="block px-3 py-2 rounded-md font-medium text-gray-700 hover:bg-brand-50 hover:text-brand-600">Montañas en bici</a>
            <a href="#testimonios" class="block px-3 py-2 rounded-md font-medium text-gray-700 hover:bg-brand-50 hover:text-brand-600">Testimonios</a>
            <a href="#como-llegar" class="block px-3 py-2 rounded-md font-medium text-gray-700 hover:bg-brand-50 hover:text-brand-600">Cómo llegar</a>
            <a href="#faq" class="block px-3 py-2 rounded-md font-medium text-gray-700 hover:bg-brand-50 hover:text-brand-600">FAQ</a>
            <a href="#contacto" class="block px-3 py-2 rounded-md font-medium text-gray-700 hover:bg-brand-50 hover:text-brand-600">Contacto</a>
            <a href="https://wa.me/573025467899?text=Hola,%20quisiera%20más%20información%20sobre%20las%20rutas%20de%20Mochuelo%20Vivo" 
               target="_blank"
               class="flex items-center justify-center w-full mt-4 px-4 py-2.5 rounded-full bg-brand-600 text-white font-semibold text-center">
               <i class="fa-brands fa-whatsapp text-lg mr-2"></i> Reservar por WhatsApp
            </a>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="hero-bg relative py-24 lg:py-36 text-white overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="max-w-3xl">
                <span class="inline-flex items-center px-3.5 py-1.5 rounded-full text-xs font-semibold bg-emerald-500/30 backdrop-blur-md text-emerald-200 border border-emerald-400/30 mb-6">
                    <i class="fa-solid fa-leaf mr-2 text-emerald-300"></i> Biciturismo Rural Comunitario
                </span>
                <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight leading-tight mb-6">
                    Pedaleando por la vida: <span class="text-emerald-300">una nueva mirada</span> al territorio
                </h1>
                <p class="text-lg sm:text-xl text-gray-200 leading-relaxed mb-8">
                    Turismo rural comunitario y cicloturismo que conecta visitantes con la gente, el paisaje y las historias de Mochuelo Bajo.
                </p>
                <div class="flex flex-col sm:flex-row gap-4">
                    <a href="#la-ruta" class="inline-flex items-center justify-center px-8 py-4 rounded-xl bg-amber-500 hover:bg-amber-600 text-gray-900 font-bold transition-all shadow-lg hover:shadow-xl transform hover:-translate-y-0.5">
                        Conoce la ruta <i class="fa-solid fa-arrow-right ml-3"></i>
                    </a>
                    <a href="#quienes-somos" class="inline-flex items-center justify-center px-8 py-4 rounded-xl bg-white/10 hover:bg-white/20 text-white font-semibold backdrop-blur-md border border-white/30 transition-all">
                        Saber más
                    </a>
                </div>
            </div>
        </div>
        <!-- Decorative subtle wave bottom -->
        <div class="absolute bottom-0 left-0 right-0 h-12 bg-[#f9fbf9] [clip-path:polygon(0_100%,100%_100%,100%_0)]"></div>
    </section>

    <!-- QUIÉNES SOMOS -->
    <section id="quienes-somos" class="py-20 bg-[#f9fbf9]">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                
                <div class="lg:col-span-6 space-y-6">
                    <div class="inline-flex items-center space-x-2 text-brand-600 font-bold text-sm tracking-wider uppercase">
                        <i class="fa-solid fa-heart"></i>
                        <span>Quiénes Somos</span>
                    </div>
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900 tracking-tight leading-snug">
                        Una apuesta social desde la bicicleta
                    </h2>
                    <p class="text-gray-600 text-lg leading-relaxed">
                        <strong class="text-gray-900">Mochuelo Vivo</strong> es una iniciativa de turismo rural y comunitario ubicada en la <strong class="text-brand-700">Vereda Mochuelo Bajo</strong>, en los cerros del sur de Bogotá. A través de recorridos en bicicleta, mostramos otra cara del territorio: su paisaje, su gente y su memoria campesina.
                    </p>
                    <div class="p-6 bg-brand-50 rounded-2xl border border-brand-100 flex items-start space-x-4">
                        <div class="w-12 h-12 rounded-xl bg-brand-600 text-white flex items-center justify-center flex-shrink-0 text-xl shadow">
                            <i class="fa-solid fa-users"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-brand-900 text-lg mb-1">Programa "Conociéndonos en bici"</h3>
                            <p class="text-gray-600 text-sm leading-relaxed">
                                Nuestro programa busca re-significar Mochuelo Bajo y visibilizar a las organizaciones sociales que trabajan día a día por la dignidad y sostenibilidad de su territorio.
                            </p>
                        </div>
                    </div>
                </div>

                <!-- Visual Photo Card Representation -->
                <div class="lg:col-span-6 relative">
                    <div class="relative rounded-3xl overflow-hidden shadow-2xl border-4 border-white">
                        <img src="https://images.unsplash.com/photo-1544197150-b99a580bb7a8?auto=format&fit=crop&w=1000&q=80" alt="Ciclistas en Mochuelo Bajo" class="w-full h-[400px] object-cover">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent flex items-end p-8">
                            <div class="text-white">
                                <span class="bg-brand-600 text-xs uppercase px-3 py-1 rounded-full font-bold">Comunidad & Vida</span>
                                <p class="text-xl font-bold mt-2">Vereda Mochuelo Bajo — Bogotá, Colombia</p>
                            </div>
                        </div>
                    </div>
                    <!-- Small overlay card -->
                    <div class="absolute -bottom-6 -left-6 bg-white p-4 rounded-2xl shadow-xl hidden sm:flex items-center space-x-4 border border-gray-100 max-w-xs">
                        <div class="w-10 h-10 rounded-full bg-amber-100 text-amber-600 flex items-center justify-center font-bold">
                            <i class="fa-solid fa-mountain"></i>
                        </div>
                        <div>
                            <p class="text-xs text-gray-500 uppercase font-semibold">Ubicación</p>
                            <p class="text-sm font-bold text-gray-800">Cerros del Sur de Bogotá</p>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- NUEVA SECCIÓN: MISIÓN Y VISIÓN -->
    <section id="mision-vision" class="py-20 bg-gradient-to-b from-[#f9fbf9] to-white border-t border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="bg-brand-100 text-brand-800 font-bold px-3.5 py-1.5 rounded-full text-xs uppercase tracking-wider inline-flex items-center">
                    <i class="fa-solid fa-compass mr-2 text-brand-600"></i> Nuestro Propósito & Horizonte
                </span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900 mt-4">Misión y Visión Orgullo Local</h2>
                <p class="text-gray-600 text-lg mt-3">Transformando la narrativa del territorio a través del biciturismo y el desarrollo sostenible de la comunidad.</p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-stretch">
                <!-- Tarjeta Misión -->
                <div class="bg-white rounded-3xl p-8 sm:p-10 border border-brand-100 shadow-xl relative overflow-hidden flex flex-col justify-between group hover:border-brand-300 transition-all">
                    <div class="absolute -right-8 -bottom-8 w-36 h-36 bg-brand-50 rounded-full opacity-50 group-hover:scale-110 transition-transform"></div>
                    
                    <div class="relative z-10">
                        <div class="flex items-center justify-between mb-6">
                            <div class="w-14 h-14 bg-brand-600 text-white rounded-2xl flex items-center justify-center text-2xl shadow-lg">
                                <i class="fa-solid fa-bullseye"></i>
                            </div>
                            <span class="text-xs font-extrabold tracking-widest text-brand-600 uppercase bg-brand-50 px-3 py-1.5 rounded-lg border border-brand-100">
                                Misión
                            </span>
                        </div>
                        
                        <h3 class="text-2xl font-bold text-brand-900 mb-4">Empresa Social de Turismo Sostenible</h3>
                        <p class="text-gray-600 leading-relaxed text-base">
                            Somos una empresa social de turismo sostenible que visibiliza y conecta la riqueza humana y natural de la vereda Mochuelo Bajo con el mundo. Transformamos el estigma territorial en orgullo local a través de experiencias ciclísticas que generan ingresos justos para la comunidad, fortalecen el tejido social y protegen el patrimonio ambiental de nuestro territorio.
                        </p>
                    </div>

                    <div class="relative z-10 mt-8 pt-6 border-t border-gray-100 grid grid-cols-3 gap-2 text-center">
                        <div class="p-2 bg-brand-50/50 rounded-xl">
                            <i class="fa-solid fa-hand-holding-dollar text-brand-600 mb-1"></i>
                            <span class="block text-[11px] font-bold text-gray-700">Ingresos Justos</span>
                        </div>
                        <div class="p-2 bg-brand-50/50 rounded-xl">
                            <i class="fa-solid fa-people-roof text-brand-600 mb-1"></i>
                            <span class="block text-[11px] font-bold text-gray-700">Tejido Social</span>
                        </div>
                        <div class="p-2 bg-brand-50/50 rounded-xl">
                            <i class="fa-solid fa-tree text-brand-600 mb-1"></i>
                            <span class="block text-[11px] font-bold text-gray-700">Patrimonio Ambiental</span>
                        </div>
                    </div>
                </div>

                <!-- Tarjeta Visión -->
                <div class="bg-brand-900 text-white rounded-3xl p-8 sm:p-10 shadow-xl relative overflow-hidden flex flex-col justify-between group">
                    <div class="absolute -right-8 -bottom-8 w-40 h-40 bg-emerald-500/10 rounded-full group-hover:scale-110 transition-transform"></div>
                    
                    <div class="relative z-10">
                        <div class="flex items-center justify-between mb-6">
                            <div class="w-14 h-14 bg-amber-500 text-gray-900 rounded-2xl flex items-center justify-center text-2xl shadow-lg">
                                <i class="fa-solid fa-eye"></i>
                            </div>
                            <span class="text-xs font-extrabold tracking-widest text-amber-300 uppercase bg-white/10 backdrop-blur-md px-3 py-1.5 rounded-lg border border-white/20">
                                Visión 2030
                            </span>
                        </div>
                        
                        <h3 class="text-2xl font-bold text-white mb-4">Modelo Referente de Turismo Rural</h3>
                        <p class="text-gray-200 leading-relaxed text-base">
                            Para el año 2030, seremos el modelo referente de turismo rural y resignificación territorial en Bogotá. Lograremos que Mochuelo Bajo sea reconocido regionalmente como un destino de turismo ecológico de alta calidad, donde la narrativa de la basura haya sido reemplazada por una historia de resiliencia, naturaleza y desarrollo comunitario liderado por sus propios habitantes.
                        </p>
                    </div>

                    <div class="relative z-10 mt-8 pt-6 border-t border-white/10 grid grid-cols-3 gap-2 text-center">
                        <div class="p-2 bg-white/5 rounded-xl border border-white/10">
                            <i class="fa-solid fa-seedling text-amber-400 mb-1"></i>
                            <span class="block text-[11px] font-semibold text-gray-200">Resignificación</span>
                        </div>
                        <div class="p-2 bg-white/5 rounded-xl border border-white/10">
                            <i class="fa-solid fa-leaf text-amber-400 mb-1"></i>
                            <span class="block text-[11px] font-semibold text-gray-200">Ecoturismo</span>
                        </div>
                        <div class="p-2 bg-white/5 rounded-xl border border-white/10">
                            <i class="fa-solid fa-heart-pulse text-amber-400 mb-1"></i>
                            <span class="block text-[11px] font-semibold text-gray-200">Resiliencia</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICIOS -->
    <section id="servicios" class="py-20 bg-white border-y border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <span class="text-brand-600 font-bold text-sm tracking-wider uppercase block mb-2">Servicios</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900">Lo que hacemos</h2>
                <p class="text-gray-600 mt-3">Experiencias auténticas diseñadas para transformar miradas y fortalecer el desarrollo local.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Card 1 -->
                <div class="bg-[#f9fbf9] p-8 rounded-2xl border border-gray-100 hover:border-brand-200 transition-all hover:shadow-xl group">
                    <div class="w-14 h-14 bg-brand-100 text-brand-700 rounded-2xl flex items-center justify-center text-2xl mb-6 group-hover:bg-brand-600 group-hover:text-white transition-all shadow-sm">
                        <i class="fa-solid fa-route"></i>
                    </div>
                    <h3 class="text-xl font-bold text-brand-900 mb-3">Rutas Guiadas</h3>
                    <p class="text-gray-600 leading-relaxed text-sm">
                        Rutas guiadas en bicicleta por senderos rurales, con paradas clave en puntos de alto valor paisajístico, cultural e histórico de la vereda.
                    </p>
                </div>

                <!-- Card 2 -->
                <div class="bg-[#f9fbf9] p-8 rounded-2xl border border-gray-100 hover:border-brand-200 transition-all hover:shadow-xl group">
                    <div class="w-14 h-14 bg-amber-100 text-amber-700 rounded-2xl flex items-center justify-center text-2xl mb-6 group-hover:bg-amber-500 group-hover:text-gray-900 transition-all shadow-sm">
                        <i class="fa-solid fa-wheat-awn"></i>
                    </div>
                    <h3 class="text-xl font-bold text-brand-900 mb-3">Vivencias Campesinas</h3>
                    <p class="text-gray-600 leading-relaxed text-sm">
                        Vivencias interactivas junto a familias campesinas localizadas: agricultura, ganadería responsable y tradiciones vivas del campo bogotano.
                    </p>
                </div>

                <!-- Card 3 -->
                <div class="bg-[#f9fbf9] p-8 rounded-2xl border border-gray-100 hover:border-brand-200 transition-all hover:shadow-xl group">
                    <div class="w-14 h-14 bg-emerald-100 text-emerald-700 rounded-2xl flex items-center justify-center text-2xl mb-6 group-hover:bg-emerald-600 group-hover:text-white transition-all shadow-sm">
                        <i class="fa-solid fa-hands-holding-circle"></i>
                    </div>
                    <h3 class="text-xl font-bold text-brand-900 mb-3">Tejido Social</h3>
                    <p class="text-gray-600 leading-relaxed text-sm">
                        Visibilizamos las organizaciones sociales de Mochuelo Bajo y construimos colaborativamente una nueva narrativa positiva sobre el territorio.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- LA RUTA (MOCHUELO BAJO) -->
    <section id="la-ruta" class="py-20 bg-[#f2f8f3]">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="bg-white rounded-3xl p-8 sm:p-12 shadow-xl border border-brand-100">
                <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center mb-10">
                    <div class="lg:col-span-8">
                        <span class="bg-brand-100 text-brand-800 font-bold px-3 py-1 rounded-full text-xs uppercase tracking-wider">Pasadía Especial</span>
                        <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900 mt-3">Ruta Mochuelo Bajo</h2>
                        <p class="text-gray-600 mt-2 text-lg">Portal Tunal &rarr; Mochuelo Bajo</p>
                    </div>
                    <div class="lg:col-span-4 lg:text-right">
                        <span class="text-xs uppercase text-gray-500 font-semibold block">Valor por persona</span>
                        <span class="text-3xl sm:text-4xl font-extrabold text-brand-700">$300.000 COP</span>
                    </div>
                </div>

                <!-- Grid Details -->
                <div class="grid grid-cols-2 sm:grid-cols-2 lg:grid-cols-4 gap-6 py-6 border-y border-gray-100">
                    <div class="flex items-center space-x-4">
                        <div class="w-12 h-12 rounded-xl bg-brand-50 text-brand-600 flex items-center justify-center text-xl">
                            <i class="fa-regular fa-clock"></i>
                        </div>
                        <div>
                            <p class="text-xs text-gray-500 font-medium uppercase">Duración</p>
                            <p class="text-base font-bold text-gray-800">8 horas</p>
                        </div>
                    </div>

                    <div class="flex items-center space-x-4">
                        <div class="w-12 h-12 rounded-xl bg-brand-50 text-brand-600 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-sun"></i>
                        </div>
                        <div>
                            <p class="text-xs text-gray-500 font-medium uppercase">Hora de salida</p>
                            <p class="text-base font-bold text-gray-800">8:00 a.m.</p>
                        </div>
                    </div>

                    <div class="flex items-center space-x-4">
                        <div class="w-12 h-12 rounded-xl bg-brand-50 text-brand-600 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-gauge-high"></i>
                        </div>
                        <div>
                            <p class="text-xs text-gray-500 font-medium uppercase">Nivel</p>
                            <p class="text-base font-bold text-gray-800">Intermedio</p>
                        </div>
                    </div>

                    <div class="flex items-center space-x-4">
                        <div class="w-12 h-12 rounded-xl bg-brand-50 text-brand-600 flex items-center justify-center text-xl">
                            <i class="fa-solid fa-location-dot"></i>
                        </div>
                        <div>
                            <p class="text-xs text-gray-500 font-medium uppercase">Punto de encuentro</p>
                            <p class="text-base font-bold text-gray-800">Portal Tunal</p>
                        </div>
                    </div>
                </div>

                <!-- Incluye / Debes Llevar -->
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 my-8">
                    <div class="bg-emerald-50/60 p-6 rounded-2xl border border-emerald-100">
                        <h4 class="font-bold text-emerald-900 flex items-center text-base mb-3">
                            <i class="fa-solid fa-circle-check text-emerald-600 mr-2"></i> El plan incluye:
                        </h4>
                        <ul class="space-y-2 text-sm text-emerald-950">
                            <li class="flex items-center"><i class="fa-solid fa-check text-xs text-emerald-600 mr-2"></i> Bicicleta adecuada para el recorrido</li>
                            <li class="flex items-center"><i class="fa-solid fa-check text-xs text-emerald-600 mr-2"></i> Guía turística local especializada</li>
                            <li class="flex items-center"><i class="fa-solid fa-check text-xs text-emerald-600 mr-2"></i> Seguro de asistencia médica</li>
                        </ul>
                    </div>

                    <div class="bg-amber-50/60 p-6 rounded-2xl border border-amber-100">
                        <h4 class="font-bold text-amber-900 flex items-center text-base mb-3">
                            <i class="fa-solid fa-triangle-exclamation text-amber-600 mr-2"></i> Debes llevar:
                        </h4>
                        <ul class="space-y-2 text-sm text-amber-950">
                            <li class="flex items-center"><i class="fa-solid fa-chevron-right text-xs text-amber-600 mr-2"></i> Refrigerio personal</li>
                            <li class="flex items-center"><i class="fa-solid fa-chevron-right text-xs text-amber-600 mr-2"></i> Agua / Hidratación constante</li>
                            <li class="flex items-center"><i class="fa-solid fa-chevron-right text-xs text-amber-600 mr-2"></i> Bloqueador solar y ropa cómoda</li>
                        </ul>
                    </div>
                </div>

                <div class="text-center pt-2">
                    <a href="https://wa.me/573025467899?text=Hola!%20Me%20gustaría%20reservar%20un%20cupo%20para%20la%20Ruta%20Mochuelo%20Bajo%20($300.000)." 
                       target="_blank"
                       class="inline-flex items-center px-8 py-4 rounded-xl bg-emerald-600 text-white font-extrabold text-base hover:bg-emerald-700 transition-all shadow-lg hover:shadow-xl transform hover:-translate-y-0.5">
                        <i class="fa-brands fa-whatsapp text-2xl mr-3"></i> Reservar por WhatsApp
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- PAQUETE MONTAÑAS EN BICI -->
    <section id="montanas-bici" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="bg-amber-100 text-amber-800 text-xs font-extrabold uppercase px-3 py-1 rounded-full">Paquete Especial</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900 mt-3">PAQUETE: Montañas en Bici</h2>
                <p class="text-gray-600 text-lg mt-2">3 días y 2 noches recorriendo Bogotá, Zipaquirá y Ubaté</p>
            </div>

            <!-- Itinerary Breakdown Days -->
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-12">
                
                <!-- Día 1 -->
                <div class="bg-[#f9fbf9] border border-gray-200 rounded-3xl p-6 flex flex-col justify-between hover:border-brand-300 transition-all shadow-sm">
                    <div>
                        <div class="flex justify-between items-center mb-4">
                            <span class="px-3 py-1 bg-brand-600 text-white font-bold text-xs rounded-lg uppercase">Día 1</span>
                            <span class="text-xs font-semibold text-gray-500">Bogotá Urbana & Cerro</span>
                        </div>
                        <h3 class="text-xl font-bold text-brand-900 mb-3">Bogotá Histórica</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-6">
                            Salida 8:30 a.m. desde el Hotel Hilton hacia La Candelaria: Plaza de Bolívar, museos y Carrera Séptima. Almuerzo a las 12:30 p.m. Luego Catedral Primada y Cerro de Monserrate. Regreso al hotel cerca de las 6:30 p.m.
                        </p>
                        
                        <!-- Cost Table -->
                        <div class="border-t border-gray-200 pt-4 space-y-2 text-xs">
                            <div class="flex justify-between text-gray-600"><span>Transporte</span><span>$40.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Almuerzo</span><span>$35.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Entrada Monserrate (ida/regreso)</span><span>$42.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Hotel (1 noche)</span><span>$420.000</span></div>
                        </div>
                    </div>
                    
                    <div class="border-t border-brand-100 pt-4 mt-6 flex justify-between items-center font-bold text-brand-900">
                        <span>Total Día 1</span>
                        <span class="text-lg text-brand-700">$550.000 COP</span>
                    </div>
                </div>

                <!-- Día 2 -->
                <div class="bg-[#f9fbf9] border border-gray-200 rounded-3xl p-6 flex flex-col justify-between hover:border-brand-300 transition-all shadow-sm">
                    <div>
                        <div class="flex justify-between items-center mb-4">
                            <span class="px-3 py-1 bg-brand-600 text-white font-bold text-xs rounded-lg uppercase">Día 2</span>
                            <span class="text-xs font-semibold text-gray-500">Zipaquirá</span>
                        </div>
                        <h3 class="text-xl font-bold text-brand-900 mb-3">Catedral de Sal</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-6">
                            Recorrido por la Catedral de Sal de 8:30 a.m. a 2:00 p.m., almuerzo incluido. Después, caminata por los alrededores y regreso al hotel en la noche. Opción de conocer el centro histórico del municipio.
                        </p>
                        
                        <!-- Cost Table -->
                        <div class="border-t border-gray-200 pt-4 space-y-2 text-xs">
                            <div class="flex justify-between text-gray-600"><span>Entrada Catedral de Sal</span><span>$70.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Almuerzo</span><span>$35.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Transporte</span><span>$25.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Hotel (1 noche)</span><span>$480.000</span></div>
                        </div>
                    </div>
                    
                    <div class="border-t border-brand-100 pt-4 mt-6 flex justify-between items-center font-bold text-brand-900">
                        <span>Total Día 2</span>
                        <span class="text-lg text-brand-700">$610.000 COP</span>
                    </div>
                </div>

                <!-- Día 3 -->
                <div class="bg-[#f9fbf9] border border-gray-200 rounded-3xl p-6 flex flex-col justify-between hover:border-brand-300 transition-all shadow-sm">
                    <div>
                        <div class="flex justify-between items-center mb-4">
                            <span class="px-3 py-1 bg-brand-600 text-white font-bold text-xs rounded-lg uppercase">Día 3</span>
                            <span class="text-xs font-semibold text-gray-500">Ubaté</span>
                        </div>
                        <h3 class="text-xl font-bold text-brand-900 mb-3">Tradición Láctea & Campo</h3>
                        <p class="text-gray-600 text-sm leading-relaxed mb-6">
                            Salida temprano hacia Ubaté. Desde las 9:00 a.m. conoceremos el proceso de fabricación de productos lácteos en una hacienda y visitaremos una empresa de turismo rural. Disfruta su biodiversidad y cultura.
                        </p>
                        
                        <!-- Cost Table -->
                        <div class="border-t border-gray-200 pt-4 space-y-2 text-xs">
                            <div class="flex justify-between text-gray-600"><span>Transporte</span><span>$40.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Entrada finca turística</span><span>$25.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Entrada empresa lácteos</span><span>$65.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Almuerzo</span><span>$35.000</span></div>
                            <div class="flex justify-between text-gray-600"><span>Hotel 4 estrellas La Intania (1 noche)</span><span>$480.000</span></div>
                        </div>
                    </div>

                    <div class="border-t border-brand-100 pt-4 mt-6 flex justify-between items-center font-bold text-brand-900">
                        <span>Total Día 3</span>
                        <span class="text-lg text-brand-700">$750.000 COP</span>
                    </div>
                </div>

            </div>

            <!-- Discount Banner & Grand Total -->
            <div class="bg-gradient-to-r from-brand-900 to-brand-800 rounded-3xl p-8 sm:p-10 text-white shadow-2xl">
                <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-center">
                    <div class="md:col-span-8 space-y-3">
                        <h3 class="text-2xl sm:text-3xl font-extrabold">Resumen del Paquete Completo</h3>
                        <p class="text-gray-300 text-sm">
                            El precio por persona incluye transporte, hospedaje, entradas a atracciones y alimentación básica durante los 3 días.
                        </p>
                    </div>

                    <div class="md:col-span-4 bg-white/10 backdrop-blur-md p-6 rounded-2xl border border-white/20 text-center">
                        <span class="text-xs uppercase text-gray-300 font-semibold block mb-1">Total Aproximado del Viaje (3 días)</span>
                        <span class="text-3xl sm:text-4xl font-extrabold text-amber-400 block">$1.910.000 COP</span>
                        <span class="text-xs text-gray-300">por persona</span>

                        <a href="https://wa.me/573025467899?text=Hola,%20deseo%20solicitar%20información%20sobre%20el%20paquete%20Montañas%20en%20bici%20(3%20días)." 
                           target="_blank"
                           class="mt-4 inline-flex items-center justify-center w-full py-3 bg-amber-500 hover:bg-amber-600 text-gray-900 font-bold rounded-xl transition-all shadow">
                            Preguntar por este paquete
                        </a>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- NUEVA SECCIÓN 1: TESTIMONIOS Y RESEÑAS -->
    <section id="testimonios" class="py-20 bg-[#f2f8f3] border-t border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <span class="text-brand-600 font-bold text-sm tracking-wider uppercase block mb-2">Voces de la Comunidad y Visitantes</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900">Lo que dicen quienes pedalean con nosotros</h2>
                <p class="text-gray-600 mt-3">Historias y opiniones reales de personas que han vivido la experiencia Mochuelo Vivo.</p>
            </div>

            <!-- Testimonials Grid -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Testimonial 1 -->
                <div class="bg-white p-8 rounded-3xl border border-brand-100 shadow-md hover:shadow-xl transition-all flex flex-col justify-between">
                    <div>
                        <!-- Rating Stars -->
                        <div class="flex text-amber-500 text-sm mb-4 space-x-1">
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-gray-600 text-sm leading-relaxed italic mb-6">
                            "Una experiencia reveladora. Cambió totalmente mi percepción sobre Mochuelo Bajo. Los guías comunitarios nos contaron la verdadera historia del territorio mientras disfrutábamos de paisajes campesinos impresionantes."
                        </p>
                    </div>
                    <div class="flex items-center space-x-4 pt-4 border-t border-gray-100">
                        <div class="w-12 h-12 rounded-full bg-brand-100 text-brand-700 flex items-center justify-center font-bold text-lg">
                            CA
                        </div>
                        <div>
                            <h4 class="font-bold text-brand-900 text-sm">Camila Restrepo</h4>
                            <p class="text-xs text-gray-500">Ciclista urbana, Bogotá</p>
                        </div>
                    </div>
                </div>

                <!-- Testimonial 2 -->
                <div class="bg-white p-8 rounded-3xl border border-brand-100 shadow-md hover:shadow-xl transition-all flex flex-col justify-between">
                    <div>
                        <!-- Rating Stars -->
                        <div class="flex text-amber-500 text-sm mb-4 space-x-1">
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-gray-600 text-sm leading-relaxed italic mb-6">
                            "El trato humano y el valor pedagógico del recorrido son inigualables. Apoyar a la economía local mediante el biciturismo es el camino que Bogotá necesita. ¡100% recomendado!"
                        </p>
                    </div>
                    <div class="flex items-center space-x-4 pt-4 border-t border-gray-100">
                        <div class="w-12 h-12 rounded-full bg-amber-100 text-amber-700 flex items-center justify-center font-bold text-lg">
                            JG
                        </div>
                        <div>
                            <h4 class="font-bold text-brand-900 text-sm">Juan Gabriel Ortiz</h4>
                            <p class="text-xs text-gray-500">Investigador Ambiental</p>
                        </div>
                    </div>
                </div>

                <!-- Testimonial 3 -->
                <div class="bg-white p-8 rounded-3xl border border-brand-100 shadow-md hover:shadow-xl transition-all flex flex-col justify-between">
                    <div>
                        <!-- Rating Stars -->
                        <div class="flex text-amber-500 text-sm mb-4 space-x-1">
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-gray-600 text-sm leading-relaxed italic mb-6">
                            "Compartir el amuerzo con los agricultores locales y conocer su lucha por la soberanía alimentaria fue el punto culminante. La bici es el medio perfecto para conectar con la gente."
                        </p>
                    </div>
                    <div class="flex items-center space-x-4 pt-4 border-t border-gray-100">
                        <div class="w-12 h-12 rounded-full bg-emerald-100 text-emerald-700 flex items-center justify-center font-bold text-lg">
                            LV
                        </div>
                        <div>
                            <h4 class="font-bold text-brand-900 text-sm">Luisa Fernanda Vega</h4>
                            <p class="text-xs text-gray-500">Biciturista Internacional</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Stats Banner -->
            <div class="mt-12 bg-white rounded-2xl p-6 border border-brand-100 shadow-sm grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
                <div>
                    <span class="text-3xl font-extrabold text-brand-700 block">+350</span>
                    <span class="text-xs text-gray-500 uppercase font-semibold">Ciclistas guiados</span>
                </div>
                <div>
                    <span class="text-3xl font-extrabold text-brand-700 block">12+</span>
                    <span class="text-xs text-gray-500 uppercase font-semibold">Organizaciones aliadas</span>
                </div>
                <div>
                    <span class="text-3xl font-extrabold text-brand-700 block">100%</span>
                    <span class="text-xs text-gray-500 uppercase font-semibold">Impacto comunitario</span>
                </div>
                <div>
                    <span class="text-3xl font-extrabold text-amber-500 block">4.9 / 5</span>
                    <span class="text-xs text-gray-500 uppercase font-semibold">Calificación promedio</span>
                </div>
            </div>
        </div>
    </section>

    <!-- GALERÍA -->
    <section id="galeria" class="py-20 bg-[#f9fbf9]">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <span class="text-brand-600 font-bold text-sm tracking-wider uppercase block mb-2">Galería</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900">Nuestras rutas en imágenes</h2>
                <p class="text-gray-600 mt-2">Un vistazo a los paisajes, sonrisas y vivencias del territorio Mochuelo Bajo.</p>
            </div>

            <!-- Gallery Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="group relative overflow-hidden rounded-2xl shadow-md h-72">
                    <img src="https://images.unsplash.com/photo-1544197150-b99a580bb7a8?auto=format&fit=crop&w=800&q=80" alt="Biciturismo" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent opacity-0 group-hover:opacity-100 transition-opacity p-6 flex items-end">
                        <span class="text-white font-semibold">Conociéndonos en bici</span>
                    </div>
                </div>

                <div class="group relative overflow-hidden rounded-2xl shadow-md h-72">
                    <img src="https://images.unsplash.com/photo-1500595046743-cd271d694d30?auto=format&fit=crop&w=800&q=80" alt="Paisaje Campesino" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent opacity-0 group-hover:opacity-100 transition-opacity p-6 flex items-end">
                        <span class="text-white font-semibold">Tradición ganadera y campos de Mochuelo</span>
                    </div>
                </div>

                <div class="group relative overflow-hidden rounded-2xl shadow-md h-72">
                    <img src="https://images.unsplash.com/photo-1485965120184-e220f721d03e?auto=format&fit=crop&w=800&q=80" alt="Ciclistas en la montaña" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent opacity-0 group-hover:opacity-100 transition-opacity p-6 flex items-end">
                        <span class="text-white font-semibold">Senderos rurales y montañismo</span>
                    </div>
                </div>

                <div class="group relative overflow-hidden rounded-2xl shadow-md h-72">
                    <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=800&q=80" alt="Comunidad local" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent opacity-0 group-hover:opacity-100 transition-opacity p-6 flex items-end">
                        <span class="text-white font-semibold">Organizaciones sociales en acción</span>
                    </div>
                </div>

                <div class="group relative overflow-hidden rounded-2xl shadow-md h-72">
                    <img src="https://images.unsplash.com/photo-1517649763962-0c623266010b?auto=format&fit=crop&w=800&q=80" alt="Rutas en bici" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent opacity-0 group-hover:opacity-100 transition-opacity p-6 flex items-end">
                        <span class="text-white font-semibold">Turismo comunitario sostenible</span>
                    </div>
                </div>

                <div class="group relative overflow-hidden rounded-2xl shadow-md h-72">
                    <img src="https://images.unsplash.com/photo-1511994298241-608e28f14fde?auto=format&fit=crop&w=800&q=80" alt="Montañas de Bogotá" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent opacity-0 group-hover:opacity-100 transition-opacity p-6 flex items-end">
                        <span class="text-white font-semibold">Cerros del Sur de Bogotá</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- NUEVA SECCIÓN 2: CÓMO LLEGAR Y MAPA DE RUTA -->
    <section id="como-llegar" class="py-20 bg-white border-y border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <span class="text-brand-600 font-bold text-sm tracking-wider uppercase block mb-2">Ubicación y Logística</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900">¿Cómo llegar a Mochuelo Bajo?</h2>
                <p class="text-gray-600 mt-2">Facilitamos tu traslado desde cualquier punto de la ciudad hasta nuestro punto de encuentro.</p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-stretch">
                <!-- Transport Options Details -->
                <div class="lg:col-span-6 space-y-4 flex flex-col justify-between">
                    <!-- Option 1: Transmilenio & TransMiCable -->
                    <div class="p-6 bg-[#f9fbf9] rounded-2xl border border-gray-200 hover:border-brand-300 transition-all">
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-red-100 text-red-600 flex items-center justify-center text-xl flex-shrink-0 font-bold">
                                <i class="fa-solid fa-train-subway"></i>
                            </div>
                            <div>
                                <h3 class="font-bold text-brand-900 text-lg">En TransMilenio / TransMiCable</h3>
                                <p class="text-gray-600 text-sm mt-1">
                                    Llega a la estación <strong>Portal Tunal</strong>. Desde allí puedes tomar la ruta alimentadora o conectar con TransMiCable hasta la estación Mirador del Paraíso y descender hacia Mochuelo Bajo.
                                </p>
                            </div>
                        </div>
                    </div>

                    <!-- Option 2: SITP / Bus -->
                    <div class="p-6 bg-[#f9fbf9] rounded-2xl border border-gray-200 hover:border-brand-300 transition-all">
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-blue-100 text-blue-600 flex items-center justify-center text-xl flex-shrink-0 font-bold">
                                <i class="fa-solid fa-bus"></i>
                            </div>
                            <div>
                                <h3 class="font-bold text-brand-900 text-lg">Rutas de SITP Directas</h3>
                                <p class="text-gray-600 text-sm mt-1">
                                    Diversas rutas SITP (como C601 o 6-18) se desplazan por la Vía a Pasquilla directo a la entrada de la Vereda Mochuelo Bajo.
                                </p>
                            </div>
                        </div>
                    </div>

                    <!-- Option 3: En bicicleta propia / Carro -->
                    <div class="p-6 bg-[#f9fbf9] rounded-2xl border border-gray-200 hover:border-brand-300 transition-all">
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-emerald-100 text-emerald-600 flex items-center justify-center text-xl flex-shrink-0 font-bold">
                                <i class="fa-solid fa-bicycle"></i>
                            </div>
                            <div>
                                <h3 class="font-bold text-brand-900 text-lg">Punto de Encuentro Oficial</h3>
                                <p class="text-gray-600 text-sm mt-1">
                                    Para todas nuestras rutas programadas, nos encontramos a las <strong>8:00 a.m. en el Portal Tunal</strong>. De allí realizamos el pedaleo en grupo asistido por nuestros guías.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Interactive Visual Route Map Representation -->
                <div class="lg:col-span-6 bg-brand-900 rounded-3xl p-6 sm:p-8 text-white relative flex flex-col justify-between shadow-2xl overflow-hidden">
                    <div class="absolute -right-10 -bottom-10 opacity-10 text-white">
                        <i class="fa-solid fa-map-location-dot text-[250px]"></i>
                    </div>

                    <div class="relative z-10">
                        <span class="bg-emerald-500/30 text-emerald-200 border border-emerald-400/30 text-xs px-3 py-1 rounded-full font-bold uppercase tracking-wider">
                            Guía Rápida de Llegada
                        </span>
                        <h3 class="text-2xl font-bold mt-4 mb-2">Mapa del Recorrido Principal</h3>
                        <p class="text-gray-300 text-sm mb-6">
                            Tramo inicial de aproximación desde la zona urbana hasta el ecosistema rural sur.
                        </p>

                        <!-- Visual Step Indicator -->
                        <div class="space-y-4 my-6">
                            <div class="flex items-center space-x-4">
                                <div class="w-8 h-8 rounded-full bg-amber-500 text-gray-900 font-extrabold flex items-center justify-center text-xs">1</div>
                                <span class="text-sm font-semibold text-gray-200">Portal Tunal (Punto de Reunión)</span>
                            </div>
                            <div class="w-0.5 h-4 bg-amber-500/50 ml-4"></div>
                            <div class="flex items-center space-x-4">
                                <div class="w-8 h-8 rounded-full bg-emerald-500 text-gray-900 font-extrabold flex items-center justify-center text-xs">2</div>
                                <span class="text-sm font-semibold text-gray-200">Ascenso Avenida Boyacá Sur</span>
                            </div>
                            <div class="w-0.5 h-4 bg-emerald-500/50 ml-4"></div>
                            <div class="flex items-center space-x-4">
                                <div class="w-8 h-8 rounded-full bg-brand-200 text-gray-900 font-extrabold flex items-center justify-center text-xs">3</div>
                                <span class="text-sm font-semibold text-gray-200">Vereda Mochuelo Bajo (Corazón del Recorrido)</span>
                            </div>
                        </div>
                    </div>

                    <div class="relative z-10 pt-6 border-t border-white/10 flex flex-col sm:flex-row justify-between items-center gap-4">
                        <span class="text-xs text-gray-300">¿Tienes dudas con el trayecto?</span>
                        <a href="https://wa.me/573025467899?text=Hola!%20Necesito%20indicaciones%20para%20llegar%20al%20punto%20de%20encuentro." 
                           target="_blank" 
                           class="px-5 py-2.5 rounded-xl bg-white text-brand-900 hover:bg-emerald-100 transition-all font-bold text-xs inline-flex items-center">
                            <i class="fa-brands fa-whatsapp text-sm mr-2 text-emerald-600"></i> Ubicación exacta por Chat
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- NUEVA SECCIÓN 3: PREGUNTAS FRECUENTES (FAQ) -->
    <section id="faq" class="py-20 bg-[#f9fbf9]">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <span class="text-brand-600 font-bold text-sm tracking-wider uppercase block mb-2">Resuelve tus dudas</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900">Preguntas Frecuentes</h2>
                <p class="text-gray-600 mt-2">Todo lo que necesitas saber antes de subirte a la bici con nosotros.</p>
            </div>

            <!-- Accordion Container -->
            <div class="space-y-4" id="faq-accordion">
                
                <!-- FAQ Item 1 -->
                <div class="bg-white border border-gray-200 rounded-2xl overflow-hidden shadow-sm transition-all hover:border-brand-300">
                    <button class="accordion-btn w-full px-6 py-5 text-left font-bold text-brand-900 flex justify-between items-center text-base sm:text-lg focus:outline-none">
                        <span>¿Necesito llevar mi propia bicicleta?</span>
                        <i class="fa-solid fa-chevron-down text-brand-600 transition-transform duration-300"></i>
                    </button>
                    <div class="accordion-content px-6 text-gray-600 text-sm leading-relaxed">
                        <p class="pb-5">
                            ¡No es obligatorio! En la tarifa de la <strong>Ruta Mochuelo Bajo</strong> está incluida una bicicleta adecuada y revisada mecánicamente para el terreno. Si prefieres llevar la tuya propia, comunícanoslo al momento de reservar para realizar el ajuste en la tarifa.
                        </p>
                    </div>
                </div>

                <!-- FAQ Item 2 -->
                <div class="bg-white border border-gray-200 rounded-2xl overflow-hidden shadow-sm transition-all hover:border-brand-300">
                    <button class="accordion-btn w-full px-6 py-5 text-left font-bold text-brand-900 flex justify-between items-center text-base sm:text-lg focus:outline-none">
                        <span>¿Qué nivel de exigencia física se requiere?</span>
                        <i class="fa-solid fa-chevron-down text-brand-600 transition-transform duration-300"></i>
                    </button>
                    <div class="accordion-content px-6 text-gray-600 text-sm leading-relaxed">
                        <p class="pb-5">
                            La ruta estándar tiene un nivel <strong>intermedio</strong>. Si bien hay pendientes propias de los cerros del sur, el ritmo del grupo es moderado, con múltiples paradas pedagógicas y de descanso en las iniciativas comunitarias.
                        </p>
                    </div>
                </div>

                <!-- FAQ Item 3 -->
                <div class="bg-white border border-gray-200 rounded-2xl overflow-hidden shadow-sm transition-all hover:border-brand-300">
                    <button class="accordion-btn w-full px-6 py-5 text-left font-bold text-brand-900 flex justify-between items-center text-base sm:text-lg focus:outline-none">
                        <span>¿El recorrido es seguro?</span>
                        <i class="fa-solid fa-chevron-down text-brand-600 transition-transform duration-300"></i>
                    </button>
                    <div class="accordion-content px-6 text-gray-600 text-sm leading-relaxed">
                        <p class="pb-5">
                            Completamente. Todas nuestras rutas se desarrollan de la mano con líderes y organizaciones locales de la Vereda Mochuelo Bajo, garantizando acompañamiento permanente, acogida comunitaria y póliza de asistencia médica durante todo el trayecto.
                        </p>
                    </div>
                </div>

                <!-- FAQ Item 4 -->
                <div class="bg-white border border-gray-200 rounded-2xl overflow-hidden shadow-sm transition-all hover:border-brand-300">
                    <button class="accordion-btn w-full px-6 py-5 text-left font-bold text-brand-900 flex justify-between items-center text-base sm:text-lg focus:outline-none">
                        <span>¿Qué pasa si llueve el día de la salida?</span>
                        <i class="fa-solid fa-chevron-down text-brand-600 transition-transform duration-300"></i>
                    </button>
                    <div class="accordion-content px-6 text-gray-600 text-sm leading-relaxed">
                        <p class="pb-5">
                            El clima de Bogotá puede ser impredecible. Recomendamos llevar siempre chaqueta impermeable. En caso de lluvias torrenciales que pongan en riesgo la seguridad del grupo, la actividad se reprogramará sin costo adicional.
                        </p>
                    </div>
                </div>

                <!-- FAQ Item 5 -->
                <div class="bg-white border border-gray-200 rounded-2xl overflow-hidden shadow-sm transition-all hover:border-brand-300">
                    <button class="accordion-btn w-full px-6 py-5 text-left font-bold text-brand-900 flex justify-between items-center text-base sm:text-lg focus:outline-none">
                        <span>¿Cómo puedo realizar el pago o la reserva?</span>
                        <i class="fa-solid fa-chevron-down text-brand-600 transition-transform duration-300"></i>
                    </button>
                    <div class="accordion-content px-6 text-gray-600 text-sm leading-relaxed">
                        <p class="pb-5">
                            Puedes reservar tu cupo abonando el 50% previamente a través de Nequi, Daviplata o transferencia bancaria. Escríbenos directamente a nuestro WhatsApp oficial para agendar la fecha deseada.
                        </p>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- CONTACTO -->
    <section id="contacto" class="py-20 bg-white border-t border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
                
                <!-- Contact info -->
                <div class="lg:col-span-5 space-y-8">
                    <div>
                        <span class="text-brand-600 font-bold text-sm tracking-wider uppercase block mb-2">Contacto</span>
                        <h2 class="text-3xl sm:text-4xl font-extrabold text-brand-900">Súmate a la próxima ruta</h2>
                        <p class="text-gray-600 mt-4 leading-relaxed">
                            Escríbenos para agendar tu recorrido en bici o conocer cómo apoyar el proyecto socio-comunitario de Mochuelo Vivo.
                        </p>
                    </div>

                    <div class="space-y-6">
                        <div class="flex items-start space-x-4 p-4 rounded-2xl bg-[#f9fbf9] border border-gray-100">
                            <div class="w-12 h-12 rounded-xl bg-brand-100 text-brand-700 flex items-center justify-center text-xl flex-shrink-0">
                                <i class="fa-solid fa-location-dot"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-gray-900 text-sm">Ubicación</h4>
                                <p class="text-gray-600 text-sm mt-0.5">Vereda Mochuelo Bajo, Bogotá D.C., Colombia</p>
                            </div>
                        </div>

                        <div class="flex items-start space-x-4 p-4 rounded-2xl bg-[#f9fbf9] border border-gray-100">
                            <div class="w-12 h-12 rounded-xl bg-brand-100 text-brand-700 flex items-center justify-center text-xl flex-shrink-0">
                                <i class="fa-brands fa-whatsapp"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-gray-900 text-sm">WhatsApp</h4>
                                <p class="text-gray-600 text-sm mt-0.5"><a href="https://wa.me/573025467899" target="_blank" class="hover:text-brand-600">302 546 7899</a></p>
                            </div>
                        </div>

                        <div class="flex items-start space-x-4 p-4 rounded-2xl bg-[#f9fbf9] border border-gray-100">
                            <div class="w-12 h-12 rounded-xl bg-brand-100 text-brand-700 flex items-center justify-center text-xl flex-shrink-0">
                                <i class="fa-regular fa-envelope"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-gray-900 text-sm">Correo Electrónico</h4>
                                <p class="text-gray-600 text-sm mt-0.5"><a href="mailto:conociendonosenbici0@gmail.com" class="hover:text-brand-600">conociendonosenbici0@gmail.com</a></p>
                            </div>
                        </div>

                        <div class="flex items-start space-x-4 p-4 rounded-2xl bg-[#f9fbf9] border border-gray-100">
                            <div class="w-12 h-12 rounded-xl bg-brand-100 text-brand-700 flex items-center justify-center text-xl flex-shrink-0">
                                <i class="fa-brands fa-instagram"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-gray-900 text-sm">Síguenos en Instagram</h4>
                                <p class="text-gray-600 text-sm mt-0.5"><a href="https://instagram.com/bici_tur" target="_blank" class="hover:text-brand-600 font-semibold text-brand-700">@bici_tur</a></p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Contact form -->
                <div class="lg:col-span-7 bg-[#f9fbf9] p-8 sm:p-10 rounded-3xl border border-gray-200 shadow-sm">
                    <h3 class="text-xl font-bold text-brand-900 mb-6">Envíanos un mensaje directo</h3>
                    <form id="contact-form" onsubmit="event.preventDefault(); handleFormSubmit();" class="space-y-5">
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-600 mb-2">Nombre completo</label>
                                <input type="text" required placeholder="Tu nombre" class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-600 focus:outline-none transition-all text-sm">
                            </div>
                            <div>
                                <label class="block text-xs font-bold uppercase text-gray-600 mb-2">Teléfono / WhatsApp</label>
                                <input type="tel" required placeholder="Ej: 300 000 0000" class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-600 focus:outline-none transition-all text-sm">
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs font-bold uppercase text-gray-600 mb-2">Correo electrónico</label>
                            <input type="email" required placeholder="tuemail@ejemplo.com" class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-600 focus:outline-none transition-all text-sm">
                        </div>

                        <div>
                            <label class="block text-xs font-bold uppercase text-gray-600 mb-2">Experiencia de interés</label>
                            <select class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-600 focus:outline-none transition-all text-sm">
                                <option>Ruta Mochuelo Bajo (Pasadía)</option>
                                <option>Paquete Montañas en Bici (3 días)</option>
                                <option>Voluntariado / Apoyo Comunitario</option>
                                <option>Otro</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-xs font-bold uppercase text-gray-600 mb-2">Mensaje o Pregunta</label>
                            <textarea rows="4" placeholder="¿Cuándo te gustaría realizar la ruta o en qué podemos ayudarte?" class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:ring-2 focus:ring-brand-600 focus:outline-none transition-all text-sm"></textarea>
                        </div>

                        <button type="submit" class="w-full py-4 bg-brand-600 hover:bg-brand-700 text-white font-bold rounded-xl transition-all shadow-md">
                            Enviar consulta
                        </button>
                    </form>

                    <!-- Success Message Box -->
                    <div id="form-success" class="hidden mt-4 p-4 bg-emerald-100 border border-emerald-300 text-emerald-800 rounded-xl text-center text-sm font-semibold">
                        ¡Gracias por contactarnos! Te responderemos muy pronto por WhatsApp o correo.
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-brand-900 text-white py-10 border-t border-brand-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center sm:text-left flex flex-col sm:flex-row justify-between items-center gap-4">
            <div class="flex items-center space-x-3">
                <div class="w-8 h-8 bg-brand-600 rounded-lg flex items-center justify-center text-white">
                    <i class="fa-solid fa-bicycle text-sm"></i>
                </div>
                <span class="text-sm font-semibold tracking-wide">&copy; 2026 Mochuelo Vivo - Conociéndonos en bici</span>
            </div>
            <p class="text-xs text-gray-400">
                Mochuelo Bajo, Bogotá D.C. — Turismo rural comunitario y biciturismo.
            </p>
        </div>
    </footer>

    <!-- JavaScript Interactions -->
    <script>
        // Toggle mobile menu
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Close mobile menu on link click
        document.querySelectorAll('#mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Accordion functionality for FAQ
        const accordionBtns = document.querySelectorAll('.accordion-btn');

        accordionBtns.forEach(btn => {
            btn.addEventListener('click', function() {
                const content = this.nextElementSibling;
                const icon = this.querySelector('i');

                // Toggle current accordion
                if (content.classList.contains('active')) {
                    content.classList.remove('active');
                    icon.style.transform = 'rotate(0deg)';
                } else {
                    // Close other accordions
                    document.querySelectorAll('.accordion-content').forEach(c => c.classList.remove('active'));
                    document.querySelectorAll('.accordion-btn i').forEach(i => i.style.transform = 'rotate(0deg)');

                    content.classList.add('active');
                    icon.style.transform = 'rotate(180deg)';
                }
            });
        });

        // Contact form handling without alert()
        function handleFormSubmit() {
            const successBox = document.getElementById('form-success');
            const form = document.getElementById('contact-form');
            form.reset();
            successBox.classList.remove('hidden');
            setTimeout(() => {
                successBox.classList.add('hidden');
            }, 6000);
        }
    </script>
</body>
</html>