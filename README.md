```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Incredible Tours & Travels - Discover Extraordinary India</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Playfair+Display:ital,wght@0,600;0,800;1,600&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        saffron: {
                            50: '#fffbf0',
                            100: '#fef3c7',
                            500: '#f59e0b',
                            600: '#d97706',
                            700: '#b45309'
                        },
                        royal: {
                            800: '#0f172a',
                            900: '#030712'
                        }
                    },
                    fontFamily: {
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                        serif: ['"Playfair Display"', 'serif']
                    }
                }
            }
        }
    </script>

    <style>
        .glass-panel {
            background: rgba(255, 255, 255, 0.75);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.4);
        }
        .glass-dark {
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .hero-gradient {
            background: linear-gradient(180deg, rgba(3,7,18,0.2) 0%, rgba(3,7,18,0.85) 100%);
        }
        .text-gradient {
            background: linear-gradient(135deg, #f59e0b 0%, #d97706 50%, #ec4899 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 font-sans antialiased selection:bg-saffron-500 selection:text-white">

    <header id="navbar" class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 py-4 px-4 sm:px-8">
        <div class="max-w-7xl mx-auto">
            <nav class="glass-panel rounded-2xl px-6 py-3 flex items-center justify-between shadow-lg shadow-black/5">
                <!-- Brand Logo -->
                <a href="#" class="flex items-center space-x-3 group">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-saffron-500 to-amber-600 flex items-center justify-center text-white shadow-md shadow-saffron-500/30 group-hover:scale-105 transition-transform">
                        <i class="fa-solid font-bold fa-compass text-xl"></i>
                    </div>
                    <div>
                        <span class="text-xl font-extrabold tracking-tight text-slate-900 block leading-none">INCREDIBLE</span>
                        <span class="text-[10px] tracking-widest text-saffron-600 font-bold uppercase">Tours & Travels</span>
                    </div>
                </a>

                <!-- Desktop Menu -->
                <div class="hidden md:flex items-center space-x-8 font-medium text-sm text-slate-700">
                    <a href="#home" class="hover:text-saffron-600 transition-colors">Home</a>
                    <a href="#packages" class="hover:text-saffron-600 transition-colors">Packages</a>
                    <a href="#estimator" class="hover:text-saffron-600 transition-colors">Price Estimator</a>
                    <a href="#gallery" class="hover:text-saffron-600 transition-colors">Gallery</a>
                    <a href="#reviews" class="hover:text-saffron-600 transition-colors">Reviews</a>
                    <a href="#contact" class="hover:text-saffron-600 transition-colors">Contact</a>
                </div>

                <!-- Action Button -->
                <div class="hidden md:flex items-center space-x-4">
                    <a href="tel:+919643797788" class="text-xs font-semibold px-3 py-2 rounded-lg bg-amber-50 text-saffron-700 hover:bg-amber-100 transition-colors">
                        <i class="fa-solid fa-phone mr-1"></i> +91 96437 97788
                    </a>
                    <button onclick="openBookingModal('Golden Triangle Circuit')" class="bg-gradient-to-r from-saffron-500 to-amber-600 hover:from-saffron-600 hover:to-amber-700 text-white font-semibold text-sm px-5 py-2.5 rounded-xl shadow-md shadow-saffron-500/20 hover:shadow-lg transition-all transform hover:-translate-y-0.5">
                        Book Trip
                    </button>
                </div>

                <!-- Mobile Hamburger Button -->
                <button id="menu-toggle" class="md:hidden text-slate-700 hover:text-saffron-600 text-2xl focus:outline-none">
                    <i class="fa-solid fa-bars"></i>
                </button>
            </nav>
        </div>

        <!-- Mobile Menu Nav Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden max-w-7xl mx-auto mt-2 px-2">
            <div class="glass-panel rounded-2xl p-5 flex flex-col space-y-4 shadow-xl">
                <a href="#home" class="mobile-link text-slate-800 font-medium py-1">Home</a>
                <a href="#packages" class="mobile-link text-slate-800 font-medium py-1">Packages</a>
                <a href="#estimator" class="mobile-link text-slate-800 font-medium py-1">Price Estimator</a>
                <a href="#gallery" class="mobile-link text-slate-800 font-medium py-1">Gallery</a>
                <a href="#reviews" class="mobile-link text-slate-800 font-medium py-1">Reviews</a>
                <a href="#contact" class="mobile-link text-slate-800 font-medium py-1">Contact</a>
                <hr class="border-slate-200">
                <a href="tel:+919643797788" class="text-sm font-semibold text-saffron-700">
                    <i class="fa-solid fa-phone mr-2"></i>+91 96437 97788
                </a>
                <button onclick="openBookingModal('Golden Triangle Circuit')" class="w-full bg-saffron-500 text-white font-semibold py-3 rounded-xl">
                    Book Now
                </button>
            </div>
        </div>
    </header>

    <section id="home" class="relative min-h-screen flex items-center justify-center pt-24 pb-16 px-4 overflow-hidden">
        <!-- Background Image Slider Overlay -->
        <div class="absolute inset-0 z-0">
            <img id="hero-bg" src="https://images.unsplash.com/photo-1564507592333-c60657eea523?auto=format&fit=crop&w=1920&q=80" alt="Taj Mahal" class="w-full h-full object-cover transition-opacity duration-1000">
            <div class="absolute inset-0 hero-gradient"></div>
        </div>

        <div class="relative z-10 max-w-5xl mx-auto text-center text-white px-4">
            <span class="inline-flex items-center gap-2 px-4 py-2 rounded-full glass-dark text-saffron-500 font-semibold text-xs sm:text-sm tracking-wide uppercase mb-6 shadow-inner">
                <i class="fa-solid fa-award text-amber-400"></i> India's Premier Luxury Tour Operator
            </span>
            <h1 class="text-4xl sm:text-6xl md:text-7xl font-extrabold font-serif tracking-tight leading-tight mb-6">
                Explore the Unseen <br class="hidden sm:inline">
                <span class="text-gradient">Incredible India</span>
            </h1>
            <p class="text-lg sm:text-xl text-slate-200 max-w-2xl mx-auto mb-10 font-light leading-relaxed">
                Handcrafted luxury itineraries, private transfers, and bespoke local experiences across heritage, spiritual, and coastal landscapes.
            </p>

            <!-- Search / Quick Filter Bar -->
            <div class="glass-dark p-3 sm:p-4 rounded-2xl sm:rounded-3xl shadow-2xl max-w-4xl mx-auto grid grid-cols-1 sm:grid-cols-3 gap-3">
                <div class="bg-white/10 rounded-xl px-4 py-2 text-left border border-white/10">
                    <label class="block text-xs text-slate-300 font-medium uppercase tracking-wider">Destination</label>
                    <select id="hero-dest" class="w-full bg-transparent text-white focus:outline-none font-semibold text-sm cursor-pointer mt-0.5">
                        <option value="all" class="text-slate-900">All Destinations</option>
                        <option value="north" class="text-slate-900">North India & Heritage</option>
                        <option value="south" class="text-slate-900">South India & Backwaters</option>
                        <option value="mountains" class="text-slate-900">Himalayas & Ladakh</option>
                        <option value="coastal" class="text-slate-900">Goa & Beaches</option>
                    </select>
                </div>
                <div class="bg-white/10 rounded-xl px-4 py-2 text-left border border-white/10">
                    <label class="block text-xs text-slate-300 font-medium uppercase tracking-wider">Duration</label>
                    <select id="hero-dur" class="w-full bg-transparent text-white focus:outline-none font-semibold text-sm cursor-pointer mt-0.5">
                        <option value="all" class="text-slate-900">Any Duration</option>
                        <option value="short" class="text-slate-900">3 - 5 Days</option>
                        <option value="medium" class="text-slate-900">6 - 9 Days</option>
                        <option value="long" class="text-slate-900">10+ Days</option>
                    </select>
                </div>
                <button onclick="applyHeroFilter()" class="bg-saffron-500 hover:bg-saffron-600 text-slate-950 font-bold rounded-xl py-3.5 px-6 transition-all flex items-center justify-center space-x-2 shadow-lg shadow-saffron-500/30">
                    <i class="fa-solid fa-magnifying-glass"></i>
                    <span>Search Tours</span>
                </button>
            </div>

            <!-- Stats Bar -->
            <div class="mt-12 grid grid-cols-2 md:grid-cols-4 gap-4 text-center max-w-3xl mx-auto pt-6 border-t border-white/10">
                <div>
                    <h3 class="text-2xl sm:text-3xl font-extrabold text-white">15,000+</h3>
                    <p class="text-xs text-slate-300">Happy Travelers</p>
                </div>
                <div>
                    <h3 class="text-2xl sm:text-3xl font-extrabold text-white">4.9 / 5</h3>
                    <p class="text-xs text-slate-300">Customer Rating</p>
                </div>
                <div>
                    <h3 class="text-2xl sm:text-3xl font-extrabold text-white">120+</h3>
                    <p class="text-xs text-slate-300">Tour Routes</p>
                </div>
                <div>
                    <h3 class="text-2xl sm:text-3xl font-extrabold text-white">24/7</h3>
                    <p class="text-xs text-slate-300">Concierge Support</p>
                </div>
            </div>
        </div>
    </section>

    <section id="packages" class="py-20 px-4 max-w-7xl mx-auto">
        <div class="text-center max-w-2xl mx-auto mb-12">
            <span class="text-saffron-600 text-sm font-bold tracking-widest uppercase">Handpicked Itineraries</span>
            <h2 class="text-3xl sm:text-4xl font-extrabold font-serif text-slate-900 mt-2">Popular Tour Packages</h2>
            <p class="text-slate-600 mt-3 text-base">Select from our curated collections designed for couples, families, and solo explorers.</p>
        </div>

        <!-- Category Filters -->
        <div class="flex flex-wrap justify-center gap-2 mb-10">
            <button onclick="filterPackages('all')" class="pkg-filter-btn active px-5 py-2.5 rounded-full text-sm font-semibold bg-slate-900 text-white shadow-md transition-all" data-category="all">All Packages</button>
            <button onclick="filterPackages('heritage')" class="pkg-filter-btn px-5 py-2.5 rounded-full text-sm font-semibold bg-white text-slate-700 hover:bg-slate-100 border border-slate-200 transition-all" data-category="heritage">Heritage & Forts</button>
            <button onclick="filterPackages('spiritual')" class="pkg-filter-btn px-5 py-2.5 rounded-full text-sm font-semibold bg-white text-slate-700 hover:bg-slate-100 border border-slate-200 transition-all" data-category="spiritual">Spiritual & Ghats</button>
            <button onclick="filterPackages('nature')" class="pkg-filter-btn px-5 py-2.5 rounded-full text-sm font-semibold bg-white text-slate-700 hover:bg-slate-100 border border-slate-200 transition-all" data-category="nature">Backwaters & Nature</button>
            <button onclick="filterPackages('adventure')" class="pkg-filter-btn px-5 py-2.5 rounded-full text-sm font-semibold bg-white text-slate-700 hover:bg-slate-100 border border-slate-200 transition-all" data-category="adventure">Mountains & Adventure</button>
        </div>

        <!-- Package Cards Grid -->
        <div id="packages-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Dynamic Injection via JS -->
        </div>
    </section>

    <section id="estimator" class="py-20 bg-gradient-to-b from-slate-900 to-slate-950 text-white relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                <!-- Info Column -->
                <div class="lg:col-span-5">
                    <span class="text-saffron-500 font-bold tracking-widest text-xs uppercase">Instant Travel Calculator</span>
                    <h2 class="text-3xl sm:text-4xl font-extrabold font-serif mt-2 leading-tight">Custom Trip Budget Estimator</h2>
                    <p class="text-slate-300 mt-4 leading-relaxed font-light">
                        Plan your trip instantly. Calculate approximate pricing based on luxury tiers, duration, group size, and custom addon experiences.
                    </p>
                    <ul class="mt-6 space-y-3 text-sm text-slate-300">
                        <li class="flex items-center space-x-3">
                            <i class="fa-solid fa-circle-check text-saffron-500"></i>
                            <span>Transparent pricing with no hidden charges</span>
                        </li>
                        <li class="flex items-center space-x-3">
                            <i class="fa-solid fa-circle-check text-saffron-500"></i>
                            <span>Private air-conditioned transfers & dedicated guide</span>
                        </li>
                        <li class="flex items-center space-x-3">
                            <i class="fa-solid fa-circle-check text-saffron-500"></i>
                            <span>5-Star & Heritage Palace accommodation options</span>
                        </li>
                    </ul>
                </div>

                <!-- Calculator Form Column -->
                <div class="lg:col-span-7">
                    <div class="glass-dark p-6 sm:p-8 rounded-3xl border border-white/10 shadow-2xl">
                        <form id="estimator-form" class="space-y-6">
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                                <div>
                                    <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Primary Region</label>
                                    <select id="est-region" onchange="calculateEstimate()" class="w-full bg-slate-800 border border-slate-700 rounded-xl py-3 px-4 text-white text-sm focus:outline-none focus:border-saffron-500">
                                        <option value="golden-triangle">Golden Triangle (Delhi-Agra-Jaipur)</option>
                                        <option value="kerala">Kerala Backwaters & Munnar</option>
                                        <option value="goa">Goa Coastal Experience</option>
                                        <option value="ladakh">Ladakh High Altitude Circuit</option>
                                        <option value="varanasi">Varanasi & Spiritual North</option>
                                    </select>
                                </div>
                                <div>
                                    <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Hotel Category</label>
                                    <select id="est-hotel" onchange="calculateEstimate()" class="w-full bg-slate-800 border border-slate-700 rounded-xl py-3 px-4 text-white text-sm focus:outline-none focus:border-saffron-500">
                                        <option value="3">3-Star Comfort Hotels</option>
                                        <option value="4" selected>4-Star Premium Resorts</option>
                                        <option value="5">5-Star Luxury / Heritage Palaces</option>
                                    </select>
                                </div>
                            </div>

                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                                <div>
                                    <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Travelers (<span id="est-travelers-val">2</span> People)</label>
                                    <input type="range" id="est-travelers" min="1" max="10" value="2" oninput="calculateEstimate()" class="w-full accent-saffron-500">
                                </div>
                                <div>
                                    <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Duration (<span id="est-days-val">6</span> Days)</label>
                                    <input type="range" id="est-days" min="3" max="15" value="6" oninput="calculateEstimate()" class="w-full accent-saffron-500">
                                </div>
                            </div>

                            <!-- Addons -->
                            <div>
                                <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Optional Addons</label>
                                <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 text-sm">
                                    <label class="flex items-center space-x-3 bg-slate-800/60 p-3 rounded-xl border border-slate-700 cursor-pointer hover:border-saffron-500/50">
                                        <input type="checkbox" id="add-guide" onchange="calculateEstimate()" class="accent-saffron-500 rounded">
                                        <span class="text-xs text-slate-200">Private Tour Guide (+₹2,500/day)</span>
                                    </label>
                                    <label class="flex items-center space-x-3 bg-slate-800/60 p-3 rounded-xl border border-slate-700 cursor-pointer hover:border-saffron-500/50">
                                        <input type="checkbox" id="add-dinner" onchange="calculateEstimate()" class="accent-saffron-500 rounded">
                                        <span class="text-xs text-slate-200">Candlelight Dinners (+₹4,000)</span>
                                    </label>
                                </div>
                            </div>

                            <!-- Total Display -->
                            <div class="pt-4 border-t border-slate-800 flex flex-col sm:flex-row sm:items-center justify-between gap-4">
                                <div>
                                    <span class="text-xs text-slate-400 block uppercase">Estimated Total Cost</span>
                                    <span id="est-total-price" class="text-3xl font-extrabold text-saffron-500">₹42,000</span>
                                    <span class="text-[10px] text-slate-400 block">*Excluding GST & flight tickets</span>
                                </div>
                                <button type="button" onclick="bookCalculatedTrip()" class="bg-gradient-to-r from-saffron-500 to-amber-600 hover:from-saffron-600 hover:to-amber-700 text-white font-bold py-3 px-6 rounded-xl shadow-lg transition-all text-sm text-center">
                                    Request Quotation
                                </button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="gallery" class="py-20 px-4 max-w-7xl mx-auto">
        <div class="text-center max-w-2xl mx-auto mb-12">
            <span class="text-saffron-600 text-sm font-bold tracking-widest uppercase">Visual Journeys</span>
            <h2 class="text-3xl sm:text-4xl font-extrabold font-serif text-slate-900 mt-2">Destinations Showcase</h2>
            <p class="text-slate-600 mt-3">Immerse yourself in stunning imagery captured across iconic landmarks in Bharat.</p>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Gallery Item 1 -->
            <div class="group relative rounded-2xl overflow-hidden shadow-lg aspect-[4/3] cursor-pointer">
                <img src="https://images.unsplash.com/photo-1564507592333-c60657eea523?auto=format&fit=crop&w=800&q=80" alt="Taj Mahal Agra" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-80 group-hover:opacity-90 transition-opacity"></div>
                <div class="absolute bottom-4 left-4 right-4 text-white">
                    <span class="text-xs text-saffron-400 font-semibold uppercase tracking-wider">Agra, Uttar Pradesh</span>
                    <h3 class="text-xl font-bold font-serif">Taj Mahal & Forts</h3>
                </div>
            </div>

            <!-- Gallery Item 2 -->
            <div class="group relative rounded-2xl overflow-hidden shadow-lg aspect-[4/3] cursor-pointer">
                <img src="https://images.unsplash.com/photo-1477587458883-47145ed94245?auto=format&fit=crop&w=800&q=80" alt="Jaipur Amber Fort" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-80 group-hover:opacity-90 transition-opacity"></div>
                <div class="absolute bottom-4 left-4 right-4 text-white">
                    <span class="text-xs text-saffron-400 font-semibold uppercase tracking-wider">Jaipur, Rajasthan</span>
                    <h3 class="text-xl font-bold font-serif">Amber Fort & Palaces</h3>
                </div>
            </div>

            <!-- Gallery Item 3 -->
            <div class="group relative rounded-2xl overflow-hidden shadow-lg aspect-[4/3] cursor-pointer">
                <img src="https://images.unsplash.com/photo-1602216056096-3b40cc0c9944?auto=format&fit=crop&w=800&q=80" alt="Kerala Houseboat Backwaters" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-80 group-hover:opacity-90 transition-opacity"></div>
                <div class="absolute bottom-4 left-4 right-4 text-white">
                    <span class="text-xs text-saffron-400 font-semibold uppercase tracking-wider">Alleppey, Kerala</span>
                    <h3 class="text-xl font-bold font-serif">Backwaters & Houseboats</h3>
                </div>
            </div>

            <!-- Gallery Item 4 -->
            <div class="group relative rounded-2xl overflow-hidden shadow-lg aspect-[4/3] cursor-pointer">
                <img src="https://images.unsplash.com/photo-1512343879784-a960bf40e7f2?auto=format&fit=crop&w=800&q=80" alt="Goa Beach" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-80 group-hover:opacity-90 transition-opacity"></div>
                <div class="absolute bottom-4 left-4 right-4 text-white">
                    <span class="text-xs text-saffron-400 font-semibold uppercase tracking-wider">North & South Goa</span>
                    <h3 class="text-xl font-bold font-serif">Sun, Sand & Heritage</h3>
                </div>
            </div>

            <!-- Gallery Item 5 -->
            <div class="group relative rounded-2xl overflow-hidden shadow-lg aspect-[4/3] cursor-pointer">
                <img src="https://images.unsplash.com/photo-1561361513-2d000a50f0dc?auto=format&fit=crop&w=800&q=80" alt="Varanasi Ghats" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-80 group-hover:opacity-90 transition-opacity"></div>
                <div class="absolute bottom-4 left-4 right-4 text-white">
                    <span class="text-xs text-saffron-400 font-semibold uppercase tracking-wider">Varanasi, UP</span>
                    <h3 class="text-xl font-bold font-serif">Ganga Aarti & Spiritual Ghats</h3>
                </div>
            </div>

            <!-- Gallery Item 6 -->
            <div class="group relative rounded-2xl overflow-hidden shadow-lg aspect-[4/3] cursor-pointer">
                <img src="https://images.unsplash.com/photo-1626621341517-bbf3d9990a23?auto=format&fit=crop&w=800&q=80" alt="Ladakh Pangong Tso" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent opacity-80 group-hover:opacity-90 transition-opacity"></div>
                <div class="absolute bottom-4 left-4 right-4 text-white">
                    <span class="text-xs text-saffron-400 font-semibold uppercase tracking-wider">Ladakh Circuit</span>
                    <h3 class="text-xl font-bold font-serif">Pangong Tso & Valleys</h3>
                </div>
            </div>
        </div>
    </section>

    <section id="reviews" class="py-20 bg-slate-100/70 border-y border-slate-200">
        <div class="max-w-7xl mx-auto px-4">
            <div class="text-center max-w-2xl mx-auto mb-12">
                <span class="text-saffron-600 text-sm font-bold tracking-widest uppercase">Client Testimonials</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold font-serif text-slate-900 mt-2">What Our Travelers Say</h2>
                <p class="text-slate-600 mt-3">Read genuine experiences shared by domestic and international guests.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Review 1 -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 flex flex-col justify-between">
                    <div>
                        <div class="flex items-center text-amber-400 mb-4 text-sm">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-slate-700 italic text-sm leading-relaxed">
                            "Incredible Tours & Travels planned our Golden Triangle trip seamlessly. Driver was punctual, hotels were top notch, and private guides were super knowledgeable!"
                        </p>
                    </div>
                    <div class="mt-6 flex items-center space-x-3 border-t border-slate-100 pt-4">
                        <div class="w-10 h-10 rounded-full bg-saffron-100 text-saffron-700 font-bold flex items-center justify-center">
                            RK
                        </div>
                        <div>
                            <h4 class="font-bold text-slate-900 text-sm">Rajesh Kumar</h4>
                            <span class="text-xs text-slate-500">New Delhi, India</span>
                        </div>
                    </div>
                </div>

                <!-- Review 2 -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 flex flex-col justify-between">
                    <div>
                        <div class="flex items-center text-amber-400 mb-4 text-sm">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-slate-700 italic text-sm leading-relaxed">
                            "Our Kerala houseboat stay was a dream come true. The team handled every tiny detail including special dietary preferences. Highly recommended!"
                        </p>
                    </div>
                    <div class="mt-6 flex items-center space-x-3 border-t border-slate-100 pt-4">
                        <div class="w-10 h-10 rounded-full bg-saffron-100 text-saffron-700 font-bold flex items-center justify-center">
                            SM
                        </div>
                        <div>
                            <h4 class="font-bold text-slate-900 text-sm">Sarah Miller</h4>
                            <span class="text-xs text-slate-500">London, UK</span>
                        </div>
                    </div>
                </div>

                <!-- Review 3 -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 flex flex-col justify-between">
                    <div>
                        <div class="flex items-center text-amber-400 mb-4 text-sm">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-slate-700 italic text-sm leading-relaxed">
                            "The Ladakh motorcycling & SUV tour was coordinated with military precision. Oxygen support, backup vehicle, and emergency backup were present throughout."
                        </p>
                    </div>
                    <div class="mt-6 flex items-center space-x-3 border-t border-slate-100 pt-4">
                        <div class="w-10 h-10 rounded-full bg-saffron-100 text-saffron-700 font-bold flex items-center justify-center">
                            AS
                        </div>
                        <div>
                            <h4 class="font-bold text-slate-900 text-sm">Amit Sharma</h4>
                            <span class="text-xs text-slate-500">Mumbai, India</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="py-20 px-4 max-w-7xl mx-auto">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
            <!-- Contact Info -->
            <div class="lg:col-span-5 space-y-8">
                <div>
                    <span class="text-saffron-600 text-sm font-bold tracking-widest uppercase">Get In Touch</span>
                    <h2 class="text-3xl font-extrabold font-serif text-slate-900 mt-2">Connect With Travel Experts</h2>
                    <p class="text-slate-600 mt-3 text-sm">Have a question or looking to customize a group itinerary? Reach out directly via call or email.</p>
                </div>

                <div class="space-y-4">
                    <div class="flex items-start space-x-4 p-4 rounded-2xl bg-white border border-slate-200 shadow-sm">
                        <div class="w-12 h-12 rounded-xl bg-saffron-100 text-saffron-700 flex items-center justify-center text-xl shrink-0">
                            <i class="fa-solid fa-phone"></i>
                        </div>
                        <div>
                            <h4 class="font-bold text-slate-900 text-sm">Phone Support</h4>
                            <p class="text-xs text-slate-600 mt-1">Available 24/7 for active bookings</p>
                            <div class="mt-2 space-y-1">
                                <a href="tel:+919643797788" class="block text-sm font-semibold text-saffron-700 hover:underline">+91 96437 97788</a>
                                <a href="tel:+919999444497" class="block text-sm font-semibold text-saffron-700 hover:underline">+91 99994 44497</a>
                            </div>
                        </div>
                    </div>

                    <div class="flex items-start space-x-4 p-4 rounded-2xl bg-white border border-slate-200 shadow-sm">
                        <div class="w-12 h-12 rounded-xl bg-saffron-100 text-saffron-700 flex items-center justify-center text-xl shrink-0">
                            <i class="fa-solid fa-envelope"></i>
                        </div>
                        <div>
                            <h4 class="font-bold text-slate-900 text-sm">Email Address</h4>
                            <p class="text-xs text-slate-600 mt-1">Send us your itinerary requirements</p>
                            <a href="mailto:info@incrediblebharat.co.in" class="block text-sm font-semibold text-saffron-700 hover:underline mt-1">info@incrediblebharat.co.in</a>
                        </div>
                    </div>

                    <div class="flex items-start space-x-4 p-4 rounded-2xl bg-white border border-slate-200 shadow-sm">
                        <div class="w-12 h-12 rounded-xl bg-saffron-100 text-saffron-700 flex items-center justify-center text-xl shrink-0">
                            <i class="fa-solid fa-location-dot"></i>
                        </div>
                        <div>
                            <h4 class="font-bold text-slate-900 text-sm">Headquarters</h4>
                            <p class="text-xs text-slate-600 mt-1 leading-relaxed">
                                Incredible Tours & Travels, Main Travel Hub, Connaught Place / Airport Zone, New Delhi, India
                            </p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Inquiry Form -->
            <div class="lg:col-span-7 bg-white p-8 rounded-3xl border border-slate-200 shadow-xl">
                <h3 class="text-2xl font-bold font-serif text-slate-900 mb-6">Send Direct Inquiry</h3>
                <form id="contact-form" onsubmit="handleContactSubmit(event)" class="space-y-4">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Full Name *</label>
                            <input type="text" required placeholder="John Doe" class="w-full bg-slate-50 border border-slate-300 rounded-xl py-3 px-4 text-sm focus:outline-none focus:border-saffron-500">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Phone Number *</label>
                            <input type="tel" required placeholder="+91 98765 43210" class="w-full bg-slate-50 border border-slate-300 rounded-xl py-3 px-4 text-sm focus:outline-none focus:border-saffron-500">
                        </div>
                    </div>

                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Email Address *</label>
                            <input type="email" required placeholder="john@example.com" class="w-full bg-slate-50 border border-slate-300 rounded-xl py-3 px-4 text-sm focus:outline-none focus:border-saffron-500">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Preferred Destination</label>
                            <input type="text" placeholder="e.g. Rajasthan / Kerala" class="w-full bg-slate-50 border border-slate-300 rounded-xl py-3 px-4 text-sm focus:outline-none focus:border-saffron-500">
                        </div>
                    </div>

                    <div>
                        <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Message / Travel Details</label>
                        <textarea rows="4" placeholder="Tell us about dates, number of travelers, or custom needs..." class="w-full bg-slate-50 border border-slate-300 rounded-xl py-3 px-4 text-sm focus:outline-none focus:border-saffron-500"></textarea>
                    </div>

                    <button type="submit" class="w-full bg-slate-900 hover:bg-slate-800 text-white font-bold py-3.5 rounded-xl transition-all shadow-md">
                        Submit Travel Request
                    </button>
                </form>
            </div>
        </div>
    </section>

    <footer class="bg-slate-950 text-slate-400 py-12 px-4 border-t border-slate-800">
        <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
            <div>
                <span class="text-xl font-extrabold text-white tracking-tight">INCREDIBLE</span>
                <span class="text-[10px] text-saffron-500 block font-bold uppercase tracking-widest">Tours & Travels</span>
                <p class="text-xs text-slate-400 mt-3 leading-relaxed">
                    Crafting unforgettable tailor-made travel experiences across India with luxury standards and authentic local culture.
                </p>
            </div>

            <div>
                <h4 class="text-white text-sm font-bold uppercase tracking-wider mb-4">Quick Links</h4>
                <ul class="space-y-2 text-xs">
                    <li><a href="#packages" class="hover:text-white transition-colors">Tour Packages</a></li>
                    <li><a href="#estimator" class="hover:text-white transition-colors">Trip Estimator</a></li>
                    <li><a href="#gallery" class="hover:text-white transition-colors">Gallery</a></li>
                    <li><a href="#reviews" class="hover:text-white transition-colors">Testimonials</a></li>
                </ul>
            </div>

            <div>
                <h4 class="text-white text-sm font-bold uppercase tracking-wider mb-4">Top Circuits</h4>
                <ul class="space-y-2 text-xs">
                    <li><a href="#packages" class="hover:text-white transition-colors">Golden Triangle Circuit</a></li>
                    <li><a href="#packages" class="hover:text-white transition-colors">Kerala Backwaters</a></li>
                    <li><a href="#packages" class="hover:text-white transition-colors">Ladakh Expedition</a></li>
                    <li><a href="#packages" class="hover:text-white transition-colors">Varanasi Spiritual Tour</a></li>
                </ul>
            </div>

            <div>
                <h4 class="text-white text-sm font-bold uppercase tracking-wider mb-4">Direct Contacts</h4>
                <p class="text-xs text-slate-300">Helpline Numbers:</p>
                <a href="tel:+919643797788" class="block text-xs font-semibold text-saffron-500 hover:underline mt-1">+91 96437 97788</a>
                <a href="tel:+919999444497" class="block text-xs font-semibold text-saffron-500 hover:underline">+91 99994 44497</a>
                <p class="text-xs text-slate-300 mt-3">Email Support:</p>
                <a href="mailto:info@incrediblebharat.co.in" class="block text-xs font-semibold text-saffron-500 hover:underline mt-1">info@incrediblebharat.co.in</a>
            </div>
        </div>

        <div class="max-w-7xl mx-auto pt-8 border-t border-slate-900 flex flex-col sm:flex-row items-center justify-between text-xs text-slate-500">
            <p>&copy; 2026 Incredible Tours & Travels. All Rights Reserved.</p>
            <div class="flex space-x-4 mt-4 sm:mt-0">
                <a href="#" class="hover:text-slate-300">Privacy Policy</a>
                <a href="#" class="hover:text-slate-300">Terms of Service</a>
                <a href="#" class="hover:text-slate-300">Refund Policy</a>
            </div>
        </div>
    </footer>

    <div id="booking-modal" class="fixed inset-0 z-50 bg-slate-950/70 backdrop-blur-sm hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-lg w-full p-6 sm:p-8 relative shadow-2xl animate-fade-in">
            <button onclick="closeBookingModal()" class="absolute top-4 right-4 text-slate-400 hover:text-slate-600 text-xl font-bold w-8 h-8 flex items-center justify-center rounded-full hover:bg-slate-100">
                &times;
            </button>
            <h3 class="text-2xl font-bold font-serif text-slate-900">Book Tour Package</h3>
            <p class="text-xs text-slate-500 mt-1">Fill out this quick form and our travel expert will call you back within 15 minutes.</p>

            <form onsubmit="handleModalSubmit(event)" class="mt-6 space-y-4">
                <div>
                    <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Selected Package</label>
                    <input type="text" id="modal-package-name" readonly class="w-full bg-slate-100 border border-slate-200 rounded-xl py-2.5 px-4 text-sm font-semibold text-saffron-700">
                </div>
                <div>
                    <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Your Full Name *</label>
                    <input type="text" required class="w-full border border-slate-300 rounded-xl py-2.5 px-4 text-sm focus:border-saffron-500 focus:outline-none">
                </div>
                <div>
                    <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Contact Number *</label>
                    <input type="tel" required placeholder="+91" class="w-full border border-slate-300 rounded-xl py-2.5 px-4 text-sm focus:border-saffron-500 focus:outline-none">
                </div>
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Travel Date</label>
                        <input type="date" required class="w-full border border-slate-300 rounded-xl py-2.5 px-3 text-xs focus:border-saffron-500 focus:outline-none">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold text-slate-700 uppercase mb-1">Travelers</label>
                        <input type="number" min="1" max="20" value="2" required class="w-full border border-slate-300 rounded-xl py-2.5 px-3 text-xs focus:border-saffron-500 focus:outline-none">
                    </div>
                </div>
                <button type="submit" class="w-full bg-saffron-500 hover:bg-saffron-600 text-slate-950 font-bold py-3.5 rounded-xl shadow-lg transition-all mt-2 text-sm">
                    Confirm Quotation Request
                </button>
            </form>
        </div>
    </div>

    <!-- Notification Toast -->
    <div id="toast" class="fixed bottom-5 right-5 z-50 bg-slate-900 text-white px-5 py-3 rounded-2xl shadow-xl flex items-center space-x-3 hidden transition-all">
        <i class="fa-solid fa-circle-check text-saffron-500 text-lg"></i>
        <span id="toast-msg" class="text-xs font-medium">Request submitted successfully!</span>
    </div>

    <script>
        // Tour Packages Data Array
        const tourPackages = [
            {
                id: 1,
                title: "Golden Triangle Luxury Experience",
                location: "Delhi - Agra - Jaipur",
                category: "heritage",
                duration: "6 Days / 5 Nights",
                price: "₹28,500",
                rating: "4.9",
                img: "https://images.unsplash.com/photo-1564507592333-c60657eea523?auto=format&fit=crop&w=600&q=80",
                tags: ["Taj Mahal", "Palace Stay", "Private SUV"]
            },
            {
                id: 2,
                title: "Kerala Backwaters & Tea Gardens",
                location: "Cochin - Munnar - Alleppey",
                category: "nature",
                duration: "5 Days / 4 Nights",
                price: "₹24,900",
                rating: "4.8",
                img: "https://images.unsplash.com/photo-1602216056096-3b40cc0c9944?auto=format&fit=crop&w=600&q=80",
                tags: ["Private Houseboat", "Tea Plantations"]
            },
            {
                id: 3,
                title: "Varanasi Spiritual & Ganga Aarti",
                location: "Varanasi - Sarnath",
                category: "spiritual",
                duration: "4 Days / 3 Nights",
                price: "₹18,200",
                rating: "4.9",
                img: "https://images.unsplash.com/photo-1561361513-2d000a50f0dc?auto=format&fit=crop&w=600&q=80",
                tags: ["Boat Cruise", "Evening Aarti", "Temple Tour"]
            },
            {
                id: 4,
                title: "Ladakh High Mountain Expedition",
                location: "Leh - Nubra - Pangong",
                category: "adventure",
                duration: "7 Days / 6 Nights",
                price: "₹36,000",
                rating: "4.9",
                img: "https://images.unsplash.com/photo-1626621341517-bbf3d9990a23?auto=format&fit=crop&w=600&q=80",
                tags: ["High Passes", "Camping", "Oxygen Support"]
            },
            {
                id: 5,
                title: "Royal Rajasthan Heritage Trail",
                location: "Jaipur - Jodhpur - Udaipur",
                category: "heritage",
                duration: "8 Days / 7 Nights",
                price: "₹39,500",
                rating: "4.8",
                img: "https://images.unsplash.com/photo-1477587458883-47145ed94245?auto=format&fit=crop&w=600&q=80",
                tags: ["Forts", "Lake Cruise", "Cultural Shows"]
            },
            {
                id: 6,
                title: "Goa Beach & Portuguese Heritage",
                location: "North & South Goa",
                category: "nature",
                duration: "5 Days / 4 Nights",
                price: "₹21,000",
                rating: "4.7",
                img: "https://images.unsplash.com/photo-1512343879784-a960bf40e7f2?auto=format&fit=crop&w=600&q=80",
                tags: ["Beach Resort", "Water Sports", "Cruises"]
            }
        ];

        // Render Tour Cards
        function renderPackages(items) {
            const grid = document.getElementById('packages-grid');
            grid.innerHTML = items.map(pkg => `
                <div class="bg-white rounded-3xl overflow-hidden border border-slate-200 shadow-md hover:shadow-xl transition-all duration-300 flex flex-col">
                    <div class="relative h-52 overflow-hidden">
                        <img src="${pkg.img}" alt="${pkg.title}" class="w-full h-full object-cover transition-transform duration-500 hover:scale-105">
                        <div class="absolute top-3 right-3 bg-white/90 backdrop-blur-md px-3 py-1 rounded-full text-xs font-bold text-slate-800 shadow">
                            <i class="fa-solid fa-star text-amber-400 mr-1"></i>${pkg.rating}
                        </div>
                        <div class="absolute bottom-3 left-3 flex flex-wrap gap-1">
                            ${pkg.tags.map(t => `<span class="bg-slate-900/80 backdrop-blur-md text-white text-[10px] font-medium px-2 py-0.5 rounded-md">${t}</span>`).join('')}
                        </div>
                    </div>
                    <div class="p-6 flex-1 flex flex-col justify-between">
                        <div>
                            <span class="text-xs font-bold text-saffron-600 uppercase tracking-wider">${pkg.location}</span>
                            <h3 class="text-xl font-bold font-serif text-slate-900 mt-1">${pkg.title}</h3>
                            <p class="text-xs text-slate-500 mt-2 flex items-center gap-2">
                                <i class="fa-regular fa-clock"></i> ${pkg.duration}
                            </p>
                        </div>
                        <div class="mt-6 pt-4 border-t border-slate-100 flex items-center justify-between">
                            <div>
                                <span class="text-[10px] text-slate-400 block uppercase">Starting From</span>
                                <span class="text-2xl font-extrabold text-slate-900">${pkg.price}</span>
                            </div>
                            <button onclick="openBookingModal('${pkg.title}')" class="bg-slate-900 hover:bg-saffron-500 hover:text-slate-950 text-white text-xs font-bold px-4 py-2.5 rounded-xl transition-colors">
                                Book Package
                            </button>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        // Category Filter
        function filterPackages(category) {
            document.querySelectorAll('.pkg-filter-btn').forEach(btn => {
                if (btn.dataset.category === category) {
                    btn.classList.remove('bg-white', 'text-slate-700');
                    btn.classList.add('bg-slate-900', 'text-white');
                } else {
                    btn.classList.remove('bg-slate-900', 'text-white');
                    btn.classList.add('bg-white', 'text-slate-700');
                }
            });

            if (category === 'all') {
                renderPackages(tourPackages);
            } else {
                renderPackages(tourPackages.filter(p => p.category === category));
            }
        }

        // Hero Search Filter
        function applyHeroFilter() {
            const dest = document.getElementById('hero-dest').value;
            let filtered = tourPackages;
            if (dest === 'north') filtered = tourPackages.filter(p => p.id === 1 || p.id === 5);
            else if (dest === 'south') filtered = tourPackages.filter(p => p.id === 2);
            else if (dest === 'mountains') filtered = tourPackages.filter(p => p.id === 4);
            else if (dest === 'coastal') filtered = tourPackages.filter(p => p.id === 6);

            renderPackages(filtered);
            document.getElementById('packages').scrollIntoView({ behavior: 'smooth' });
        }

        // Interactive Price Estimator Math
        function calculateEstimate() {
            const regionRates = { 'golden-triangle': 3500, 'kerala': 4200, 'goa': 3800, 'ladakh': 5000, 'varanasi': 3000 };
            const hotelMultiplier = { '3': 1.0, '4': 1.4, '5': 2.1 };

            const region = document.getElementById('est-region').value;
            const hotel = document.getElementById('est-hotel').value;
            const travelers = parseInt(document.getElementById('est-travelers').value);
            const days = parseInt(document.getElementById('est-days').value);
            const addGuide = document.getElementById('add-guide').checked;
            const addDinner = document.getElementById('add-dinner').checked;

            document.getElementById('est-travelers-val').innerText = travelers;
            document.getElementById('est-days-val').innerText = days;

            let baseCost = regionRates[region] * days * hotelMultiplier[hotel];
            let groupMultiplier = travelers > 2 ? 1 + ((travelers - 2) * 0.35) : (travelers === 1 ? 0.75 : 1.0);
            
            let total = baseCost * groupMultiplier;
            if (addGuide) total += (2500 * days);
            if (addDinner) total += 4000;

            document.getElementById('est-total-price').innerText = '₹' + Math.round(total).toLocaleString('en-IN');
        }

        // Booking Modal Operations
        function openBookingModal(pkgName) {
            document.getElementById('modal-package-name').value = pkgName || 'Customized Itinerary';
            document.getElementById('booking-modal').classList.remove('hidden');
        }

        function closeBookingModal() {
            document.getElementById('booking-modal').classList.add('hidden');
        }

        function bookCalculatedTrip() {
            const region = document.getElementById('est-region').selectedOptions[0].text;
            openBookingModal(`Custom Trip: ${region}`);
        }

        // Toast Notification Trigger
        function showToast(msg) {
            const toast = document.getElementById('toast');
            document.getElementById('toast-msg').innerText = msg;
            toast.classList.remove('hidden');
            setTimeout(() => toast.classList.add('hidden'), 4000);
        }

        function handleContactSubmit(e) {
            e.preventDefault();
            showToast("Thank you! Your travel request has been received.");
            e.target.reset();
        }

        function handleModalSubmit(e) {
            e.preventDefault();
            closeBookingModal();
            showToast("Booking request sent! Our expert will contact you shortly.");
        }

        // Mobile Menu Toggle
        document.getElementById('menu-toggle').addEventListener('click', () => {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });

        document.querySelectorAll('.mobile-link').forEach(link => {
            link.addEventListener('click', () => {
                document.getElementById('mobile-menu').classList.add('hidden');
            });
        });

        // Initialize On Load
        window.onload = function() {
            renderPackages(tourPackages);
            calculateEstimate();
        };
    </script>
</body>
</html>
```
