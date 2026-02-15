<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Happy Valentine's Day Raveesha ♥</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700;900&family=Cormorant+Garamond:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * {
            -webkit-tap-highlight-color: transparent;
        }

        body {
            overflow-x: hidden;
            -webkit-overflow-scrolling: touch;
        }

        @keyframes float-up {
            0% { transform: translateY(0) rotate(0deg); opacity: 0; }
            10% { opacity: 0.4; }
            90% { opacity: 0.3; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }

        @keyframes pulse-glow {
            0%, 100% { filter: drop-shadow(0 0 8px rgba(244, 114, 182, 0.4)); }
            50% { filter: drop-shadow(0 0 16px rgba(244, 114, 182, 0.6)); }
        }

        @keyframes fade-in-up {
            from { 
                opacity: 0; 
                transform: translateY(40px);
            }
            to { 
                opacity: 1; 
                transform: translateY(0);
            }
        }

        @keyframes reveal {
            from { opacity: 0; transform: scale(0.8) rotate(-5deg); }
            to { opacity: 1; transform: scale(1) rotate(0deg); }
        }

        @keyframes zoom-in {
            from { opacity: 0; transform: scale(0.9); }
            to { opacity: 1; transform: scale(1); }
        }

        .fade-in-up {
            animation: fade-in-up 0.8s ease-out forwards;
            opacity: 0;
        }

        .animate-reveal { 
            animation: reveal 0.6s cubic-bezier(0.34, 1.56, 0.64, 1) forwards; 
        }

        .animate-zoom-in { 
            animation: zoom-in 0.5s ease-out forwards; 
        }

        .pulse-glow { 
            animation: pulse-glow 2s infinite; 
        }
        
        .floating-heart {
            animation: float-up 5s ease-in forwards;
        }

        .font-display { 
            font-family: 'Playfair Display', serif; 
        }

        .font-body { 
            font-family: 'Cormorant Garamond', serif; 
        }

        .photo-grid-item {
            position: relative;
            overflow: hidden;
            border-radius: 1rem;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .photo-grid-item:active {
            transform: scale(0.95);
        }

        .photo-grid-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.95);
            animation: fade-in 0.3s ease;
        }

        .modal.active {
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            max-width: 95%;
            max-height: 85%;
            object-fit: contain;
            border-radius: 1rem;
            animation: zoom-in 0.3s ease;
        }

        @keyframes fade-in {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Smooth scroll */
        html {
            scroll-behavior: smooth;
        }

        /* Hide scrollbar for cleaner look but keep functionality */
        ::-webkit-scrollbar {
            width: 0px;
            background: transparent;
        }

        /* Intersection observer trigger */
        .scroll-reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }

        .scroll-reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body class="min-h-screen bg-gradient-to-br from-rose-50 via-pink-50 to-purple-50 relative">
    
    <!-- Floating Hearts Background -->
    <div id="floating-hearts" class="fixed inset-0 pointer-events-none overflow-hidden z-0"></div>

    <!-- Photo Modal -->
    <div id="photo-modal" class="modal" onclick="closeModal()">
        <span class="absolute top-4 right-4 text-white text-4xl font-light cursor-pointer hover:text-pink-300 transition-colors z-50 p-2">&times;</span>
        <img id="modal-image" class="modal-content" onclick="event.stopPropagation()">
        <div id="modal-caption" class="absolute bottom-4 left-1/2 transform -translate-x-1/2 text-white text-lg font-body text-center bg-black/60 px-6 py-3 rounded-full max-w-xs"></div>
    </div>

    <!-- Main Content - Single Scroll -->
    <div class="relative z-10">
        
        <!-- Hero Section -->
        <section class="min-h-screen flex flex-col items-center justify-center px-6 py-12 text-center">
            <div class="mb-6 fade-in-up" style="animation-delay: 0.2s">
                <div class="inline-block p-6 rounded-full bg-gradient-to-br from-pink-200 to-purple-200 pulse-glow">
                    <svg class="w-20 h-20 text-rose-600" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
                    </svg>
                </div>
            </div>
            
            <h1 class="text-5xl font-black mb-4 bg-gradient-to-r from-pink-600 via-rose-600 to-purple-600 bg-clip-text text-transparent font-display fade-in-up" style="animation-delay: 0.4s">
                Happy Valentine's Day
            </h1>
            
            <h2 class="text-4xl text-gray-800 mb-6 font-display font-bold fade-in-up" style="animation-delay: 0.6s">
                My Loving Raveesha
            </h2>
            
            <p class="text-2xl text-gray-700 mb-8 font-body max-w-md fade-in-up" style="animation-delay: 0.8s">
                To the most amazing person in my life ♥
            </p>

            <div class="bg-white/70 backdrop-blur-sm rounded-3xl p-8 shadow-2xl border border-pink-100 max-w-lg fade-in-up" style="animation-delay: 1s">
                <p class="text-xl leading-relaxed text-gray-800 font-body">
                    Raveesha, every day with you is a beautiful adventure. You've filled my life with joy, 
                    laughter, and endless love. ♥
                </p>
            </div>

            <div class="mt-8 text-pink-400 animate-bounce fade-in-up" style="animation-delay: 1.2s">
                <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
                </svg>
            </div>
        </section>

        <!-- Feature Cards Section -->
        <section class="px-6 py-12">
            <div class="max-w-lg mx-auto grid grid-cols-1 gap-6 scroll-reveal">
               
                <div class="bg-white/60 backdrop-blur-sm rounded-3xl p-8 shadow-xl hover:shadow-2xl transition-all duration-300 border-2 border-pink-100">
                    <div class="text-6xl mb-4 text-center">🌹</div>
                    <h3 class="text-2xl font-bold text-gray-800 mb-3 font-display text-center">Beautiful Soul</h3>
                    <p class="text-lg text-gray-600 font-body text-center">Your beauty shines from the inside out</p>
                </div>
                <div class="bg-white/60 backdrop-blur-sm rounded-3xl p-8 shadow-xl hover:shadow-2xl transition-all duration-300 border-2 border-pink-100">
                    <div class="text-6xl mb-4 text-center">✨</div>
                    <h3 class="text-2xl font-bold text-gray-800 mb-3 font-display text-center">Forever Together</h3>
                    <p class="text-lg text-gray-600 font-body text-center">You and me, always</p>
                </div>
            </div>
        </section>

        <!-- Divider -->
        <div class="flex justify-center py-8">
            <div class="flex gap-2">
                <div class="w-2 h-2 rounded-full bg-pink-300"></div>
                <div class="w-2 h-2 rounded-full bg-rose-300"></div>
                <div class="w-2 h-2 rounded-full bg-purple-300"></div>
            </div>
        </div>

        <!-- Photos Section -->
        <section class="px-6 py-12">
            <div class="max-w-lg mx-auto scroll-reveal">
                <h2 class="text-5xl font-black text-center mb-3 bg-gradient-to-r from-pink-600 to-purple-600 bg-clip-text text-transparent font-display">
                    Our Beautiful Moments
                </h2>
                <p class="text-xl text-center text-gray-600 mb-8 font-body">
                    Every picture tells our love story ♥
                </p>

                <!-- Photo Upload Section -->
                <div class="bg-gradient-to-r from-pink-100 to-purple-100 rounded-3xl p-6 mb-8 border-2 border-pink-200">
                    <div class="text-center mb-4">
                        <svg class="w-12 h-12 mx-auto mb-3 text-pink-600" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M21 19V5c0-1.1-.9-2-2-2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2zM8.5 13.5l2.5 3.01L14.5 12l4.5 6H5l3.5-4.5z"/>
                        </svg>
                        <h3 class="text-xl font-bold text-gray-800 mb-2 font-display">Add Your Photos</h3>
                        <p class="text-base text-gray-600 font-body mb-4">Tap to choose photos from your gallery</p>
                    </div>
                    <div class="flex justify-center">
                        <input type="file" id="photo-upload" accept="image/*" multiple class="hidden">
                        <button onclick="document.getElementById('photo-upload').click()" class="px-8 py-4 bg-gradient-to-r from-pink-500 to-purple-500 text-white rounded-full font-bold text-lg shadow-lg active:scale-95 transition-transform duration-150 font-body">
                            📷 Choose Photos
                        </button>
                    </div>
                </div>

                <!-- Photo Grid -->
                <div id="photo-grid" class="grid grid-cols-2 gap-3"></div>

                <!-- Placeholder when no photos -->
                <div id="photo-placeholder" class="text-center py-12">
                    <div class="text-5xl mb-3">📸</div>
                    <p class="text-xl text-gray-600 font-body mb-2">
                        Upload your beautiful photos!
                    </p>
                    <p class="text-base text-gray-500 font-body">
                        Tap "Choose Photos" above
                    </p>
                </div>

                <div class="mt-8">
                    <div class="bg-gradient-to-r from-pink-500 to-purple-500 text-white rounded-3xl p-6 shadow-2xl">
                        <p class="text-xl leading-relaxed font-body text-center">
                            Every photo with you is a treasure, Raveesha 📸💕
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Divider -->
        <div class="flex justify-center py-8">
            <div class="flex gap-2">
                <div class="w-2 h-2 rounded-full bg-pink-300"></div>
                <div class="w-2 h-2 rounded-full bg-rose-300"></div>
                <div class="w-2 h-2 rounded-full bg-purple-300"></div>
            </div>
        </div>

        <!-- Reasons Section -->
        <section class="px-6 py-12">
            <div class="max-w-lg mx-auto scroll-reveal">
                <h2 class="text-5xl font-black text-center mb-3 bg-gradient-to-r from-pink-600 to-purple-600 bg-clip-text text-transparent font-display">
                    Why I Love You
                </h2>
                <p class="text-xl text-center text-gray-600 mb-8 font-body">
                    Tap each card to reveal, Raveesha ♥
                </p>

                <div class="space-y-4" id="reasons-grid"></div>

                <div class="mt-8">
                    <div class="bg-gradient-to-r from-pink-500 to-purple-500 text-white rounded-3xl p-6 shadow-2xl">
                        <p class="text-xl leading-relaxed font-body text-center">
                            And a thousand more reasons I discover every day, my Loving Raveesha... 💝
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Final Message Section -->
        <section class="px-6 py-16">
            <div class="max-w-lg mx-auto text-center scroll-reveal">
                <div class="bg-gradient-to-br from-rose-500 via-pink-500 to-purple-500 text-white rounded-3xl p-10 shadow-2xl">
                    <div class="mb-6">
                        <svg class="w-16 h-16 mx-auto" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
                        </svg>
                    </div>
                    <h3 class="text-3xl font-bold mb-4 font-display">Forever & Always</h3>
                    <p class="text-xl leading-relaxed font-body">
                        You are my everything. Thank you for being you, for loving me, 
                        and for making every moment special. I love you more than words can express. ♥
                    </p>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="text-center py-8 px-6 border-t border-pink-100 bg-white/30 backdrop-blur-sm">
            <p class="text-lg text-gray-600 font-body mb-2">
                Made with <svg class="inline w-5 h-5 text-rose-500 mx-1" fill="currentColor" viewBox="0 0 24 24"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg> for Raveesha
            </p>
            <p class="text-base text-gray-500 font-body">
                Happy Valentine's Day 2026 💕
            </p>
        </footer>
    </div>

    <script>
        // Data
        const reasons = [
            { icon: "💫", text: "Raveesha, your smile lights up my entire world", color: "from-pink-400 to-rose-500" },
            { icon: "🌸", text: "You make every ordinary moment extraordinary", color: "from-purple-400 to-pink-500" },
            { icon: "✨", text: "Your laugh is my favorite sound in the universe", color: "from-rose-400 to-pink-500" },
            { icon: "🎨", text: "You inspire me to be a better person every day", color: "from-pink-500 to-red-400" },
            { icon: "🌙", text: "You're my first thought in the morning and my last at night", color: "from-purple-500 to-pink-400" },
            { icon: "💝", text: "Your kindness and warmth touch everyone around you", color: "from-rose-500 to-pink-600" },
            { icon: "🌺", text: "You understand me in ways no one else does", color: "from-pink-400 to-purple-500" },
            { icon: "⭐", text: "Being with you, Raveesha, feels like coming home", color: "from-red-400 to-pink-500" }
        ];

        const revealedReasons = new Set();
        let uploadedPhotos = [];

        // Load photos from localStorage
        function loadPhotos() {
            const saved = localStorage.getItem('valentinePhotosRaveesha');
            if (saved) {
                uploadedPhotos = JSON.parse(saved);
                renderPhotos();
            }
        }

        // Save photos to localStorage
        function savePhotos() {
            localStorage.setItem('valentinePhotosRaveesha', JSON.stringify(uploadedPhotos));
        }

        // Floating hearts
        setInterval(() => {
            const heart = document.createElement('div');
            heart.textContent = '♥';
            heart.className = 'absolute text-pink-300 opacity-20 floating-heart';
            heart.style.left = Math.random() * 100 + '%';
            heart.style.bottom = '-20px';
            heart.style.fontSize = (1 + Math.random() * 0.5) + 'rem';
            heart.style.animationDuration = (4 + Math.random() * 3) + 's';
            document.getElementById('floating-hearts').appendChild(heart);
            setTimeout(() => heart.remove(), 8000);
        }, 1200);

        // Photo upload handling
        document.getElementById('photo-upload').addEventListener('change', function(e) {
            const files = Array.from(e.target.files);
            
            files.forEach(file => {
                if (file.type.startsWith('image/')) {
                    const reader = new FileReader();
                    reader.onload = function(event) {
                        uploadedPhotos.push({
                            src: event.target.result,
                            caption: `Our moment together ♥`,
                            date: new Date().toLocaleDateString()
                        });
                        savePhotos();
                        renderPhotos();
                    };
                    reader.readAsDataURL(file);
                }
            });
        });

        // Render photos
        function renderPhotos() {
            const grid = document.getElementById('photo-grid');
            const placeholder = document.getElementById('photo-placeholder');
            
            if (uploadedPhotos.length === 0) {
                placeholder.style.display = 'block';
                grid.innerHTML = '';
                return;
            }
            
            placeholder.style.display = 'none';
            grid.innerHTML = uploadedPhotos.map((photo, index) => `
                <div class="photo-grid-item animate-zoom-in" style="animation-delay: ${index * 0.1}s; height: 200px" onclick="openModal(${index})">
                    <img src="${photo.src}" alt="${photo.caption}">
                    <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-3">
                        <p class="text-white font-body text-xs">${photo.caption}</p>
                    </div>
                </div>
            `).join('');
        }

        // Modal functions
        function openModal(index) {
            const modal = document.getElementById('photo-modal');
            const img = document.getElementById('modal-image');
            const caption = document.getElementById('modal-caption');
            
            modal.classList.add('active');
            img.src = uploadedPhotos[index].src;
            caption.textContent = uploadedPhotos[index].caption;
            document.body.style.overflow = 'hidden';
        }

        function closeModal() {
            document.getElementById('photo-modal').classList.remove('active');
            document.body.style.overflow = 'auto';
        }

        // Close modal on Escape key
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') closeModal();
        });

        // Render reasons
        function renderReasons() {
            const grid = document.getElementById('reasons-grid');
            grid.innerHTML = reasons.map((reason, index) => `
                <div onclick="revealReason(${index})" 
                     id="reason-${index}"
                     class="relative bg-white/70 backdrop-blur-sm rounded-3xl p-6 cursor-pointer transition-all duration-500 border-2 border-pink-100 shadow-lg active:scale-95">
                    <div class="flex items-start gap-4">
                        <div class="text-4xl transition-all duration-500 flex-shrink-0" id="reason-icon-${index}">${reason.icon}</div>
                        <div class="flex-1">
                            <p class="text-lg text-gray-500 italic font-body" id="reason-placeholder-${index}">
                                Tap to reveal...
                            </p>
                            <p class="text-lg text-gray-800 leading-relaxed font-body hidden animate-reveal" id="reason-text-${index}">
                                ${reason.text}
                            </p>
                        </div>
                    </div>
                    <div class="absolute inset-0 bg-gradient-to-br ${reason.color} opacity-0 rounded-3xl pointer-events-none transition-opacity duration-500" id="reason-bg-${index}"></div>
                </div>
            `).join('');
        }

        function revealReason(index) {
            if (revealedReasons.has(index)) return;
            revealedReasons.add(index);
            
            document.getElementById(`reason-${index}`).classList.add('border-pink-300', 'shadow-2xl', 'scale-105');
            document.getElementById(`reason-icon-${index}`).classList.add('scale-110');
            document.getElementById(`reason-placeholder-${index}`).classList.add('hidden');
            document.getElementById(`reason-text-${index}`).classList.remove('hidden');
            document.getElementById(`reason-bg-${index}`).classList.remove('opacity-0');
            document.getElementById(`reason-bg-${index}`).classList.add('opacity-10');
        }

        // Intersection Observer for scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('revealed');
                }
            });
        }, observerOptions);

        // Observe all scroll-reveal elements
        document.addEventListener('DOMContentLoaded', () => {
            document.querySelectorAll('.scroll-reveal').forEach(el => {
                observer.observe(el);
            });
        });

        // Initialize
        loadPhotos();
        renderReasons();

        // Prevent pull-to-refresh on mobile
        let lastTouchY = 0;
        document.addEventListener('touchstart', (e) => {
            lastTouchY = e.touches[0].clientY;
        }, { passive: true });

        document.addEventListener('touchmove', (e) => {
            const touchY = e.touches[0].clientY;
            const touchYDelta = touchY - lastTouchY;
            lastTouchY = touchY;

            if (window.scrollY === 0 && touchYDelta > 0) {
                e.preventDefault();
            }
        }, { passive: false });
    </script>
</body>
</html>
