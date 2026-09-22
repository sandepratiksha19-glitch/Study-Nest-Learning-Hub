<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StudySphere - Free School Study Materials & Notes</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Poppins', sans-serif; }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 min-h-screen flex flex-col">

    <!-- Navbar -->
    <header class="bg-indigo-600 text-white shadow-md sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <span class="text-2xl font-bold bg-white text-indigo-600 px-3 py-1.5 rounded-xl shadow flex items-center gap-2">
                    🚀 <span>StudySphere</span>
                </span>
            </div>
            <nav class="hidden md:flex space-x-6 text-sm font-medium">
                <a href="#classes" class="hover:text-indigo-200 transition">Classes</a>
                <a href="#materials" class="hover:text-indigo-200 transition">Study Materials</a>
                <a href="#science-section" class="hover:text-indigo-200 transition">Class 10 Science</a>
                <a href="#maths-section" class="hover:text-indigo-200 transition">Class 10 Maths</a>
            </nav>
            <button onclick="alert('Student portal login coming soon!')" class="bg-indigo-700 hover:bg-indigo-800 px-4 py-2 rounded-xl text-sm font-medium transition shadow-sm border border-indigo-500">Student Login</button>
        </div>
    </header>

    <!-- Live Syllabus & Update Ticker -->
    <div class="bg-amber-50 border-y border-amber-200 py-3 px-4">
        <div class="max-w-7xl mx-auto flex flex-col sm:flex-row items-center justify-between text-sm">
            <div class="flex items-center space-x-2 text-amber-900 font-medium mb-2 sm:mb-0">
                <span class="animate-pulse bg-red-500 text-white text-xs font-bold px-2 py-0.5 rounded-full uppercase tracking-wider">Live Update</span>
                <span>📚 2026–2027 Revised Syllabus & Chapter-Wise Notes are now live for Classes 6 to 12!</span>
            </div>
            <a href="#materials" class="text-indigo-600 font-semibold hover:underline">Explore New Material &rarr;</a>
        </div>
    </div>

    <!-- Hero Section -->
    <section class="bg-gradient-to-br from-indigo-600 via-indigo-700 to-sky-500 text-white py-16 px-4 text-center">
        <div class="max-w-3xl mx-auto">
            <span class="bg-white/10 text-indigo-100 text-xs font-semibold px-3 py-1 rounded-full uppercase tracking-widest border border-white/20">Launch Your Learning</span>
            <h1 class="text-4xl md:text-5xl font-extrabold mt-4 mb-4 tracking-tight">Master Every Chapter, Ace Every Exam</h1>
            <p class="text-base md:text-lg text-indigo-100 mb-8">Access 100% free chapter-wise notes, NCERT solutions, practice quizzes, and previous years' questions for all classes.</p>
            
            <!-- Quick Search -->
            <div class="bg-white p-2 rounded-2xl shadow-xl flex items-center max-w-xl mx-auto border border-white/20">
                <input type="text" id="searchInput" placeholder="Search subject, chapter or topic (e.g. Real Numbers, Light)..." class="w-full px-4 py-2 text-slate-700 focus:outline-none rounded-xl text-sm md:text-base">
                <button onclick="filterMaterials()" class="bg-indigo-600 hover:bg-indigo-700 text-white px-6 py-3 rounded-xl font-medium transition shadow-sm">Search</button>
            </div>
        </div>
    </section>

    <!-- Classes Section -->
    <section id="classes" class="max-w-7xl mx-auto px-4 py-12 w-full">
        <div class="text-center mb-10">
            <h2 class="text-3xl font-bold text-slate-900">Select Your Class</h2>
            <p class="text-slate-500 mt-2">Choose your grade level to explore tailored syllabus and notes</p>
        </div>

        <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-6 gap-4">
            <button onclick="selectClass('Class 6')" class="class-btn bg-white border border-slate-200 p-6 rounded-2xl text-center shadow-sm hover:shadow-md hover:border-indigo-500 transition group">
                <div class="text-3xl mb-2">🌱</div>
                <h3 class="font-bold text-slate-800 group-hover:text-indigo-600">Class 6</h3>
            </button>
            <button onclick="selectClass('Class 7')" class="class-btn bg-white border border-slate-200 p-6 rounded-2xl text-center shadow-sm hover:shadow-md hover:border-indigo-500 transition group">
                <div class="text-3xl mb-2">🌿</div>
                <h3 class="font-bold text-slate-800 group-hover:text-indigo-600">Class 7</h3>
            </button>
            <button onclick="selectClass('Class 8')" class="class-btn bg-white border border-slate-200 p-6 rounded-2xl text-center shadow-sm hover:shadow-md hover:border-indigo-500 transition group">
                <div class="text-3xl mb-2">🚀</div>
                <h3 class="font-bold text-slate-800 group-hover:text-indigo-600">Class 8</h3>
            </button>
            <button onclick="selectClass('Class 9')" class="class-btn bg-white border border-slate-200 p-6 rounded-2xl text-center shadow-sm hover:shadow-md hover:border-indigo-500 transition group">
                <div class="text-3xl mb-2">⚡</div>
                <h3 class="font-bold text-slate-800 group-hover:text-indigo-600">Class 9</h3>
            </button>
            <button onclick="selectClass('Class 10')" class="class-btn bg-white border border-slate-200 p-6 rounded-2xl text-center shadow-sm hover:shadow-md hover:border-indigo-500 transition group ring-2 ring-indigo-600">
                <div class="text-3xl mb-2">🎯</div>
                <h3 class="font-bold text-indigo-600 group-hover:text-indigo-700">Class 10</h3>
            </button>
            <button onclick="selectClass('Class 12')" class="class-btn bg-white border border-slate-200 p-6 rounded-2xl text-center shadow-sm hover:shadow-md hover:border-indigo-500 transition group">
                <div class="text-3xl mb-2">🎓</div>
                <h3 class="font-bold text-slate-800 group-hover:text-indigo-600">Class 12</h3>
            </button>
        </div>

        <!-- Materials Display Area -->
        <div id="materials" class="mt-16">
            <div class="flex items-center justify-between mb-8">
                <div>
                    <h3 id="currentSelectionTitle" class="text-2xl font-bold text-slate-900">Featured Study Materials</h3>
                    <p class="text-slate-500 text-sm mt-1">Organized precisely chapter-by-chapter as per revised board guidelines</p>
                </div>
                <span class="bg-indigo-100 text-indigo-800 text-xs font-semibold px-3 py-1.5 rounded-full hidden sm:inline-block">100% Free Downloads</span>
            </div>

            <!-- CLASS 10 SCIENCE CHAPTERS SECTION -->
            <div id="science-section" class="mb-12">
                <h4 class="text-xl font-bold text-slate-800 mb-4 flex items-center gap-2">
                    <span>🔬 Class 10 Science (Physics, Chemistry, Biology)</span>
                </h4>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <!-- Chemistry Ch 1 -->
                    <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col justify-between">
                        <div>
                            <span class="bg-amber-100 text-amber-800 text-xs font-semibold px-3 py-1 rounded-full">Chemistry • Ch 1</span>
                            <h5 class="text-lg font-bold mt-3 text-slate-900">Chemical Reactions & Equations</h5>
                            <p class="text-slate-500 text-sm mt-1">Balanced equations, types of reactions, and oxidation-reduction revision notes.</p>
                        </div>
                        <div class="mt-6 flex space-x-2">
                            <button onclick="alert('Downloading Chemistry Ch 1 PDF...')" class="flex-1 bg-indigo-600 hover:bg-indigo-700 text-white py-2 rounded-xl text-xs font-medium transition text-center shadow-sm">📥 Notes PDF</button>
                            <button onclick="alert('Starting Quiz: Chemical Reactions')" class="flex-1 bg-slate-100 hover:bg-slate-200 text-slate-700 py-2 rounded-xl text-xs font-medium transition text-center">📝 Quiz</button>
                        </div>
                    </div>

                    <!-- Physics Ch 5 -->
                    <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col justify-between">
                        <div>
                            <span class="bg-sky-100 text-sky-800 text-xs font-semibold px-3 py-1 rounded-full">Physics • Ch 5</span>
                            <h5 class="text-lg font-bold mt-3 text-slate-900">Light – Reflection & Refraction</h5>
                            <p class="text-slate-500 text-sm mt-1">Mirror formulas, ray diagrams, refractive index, and numerical problem sheets.</p>
                        </div>
                        <div class="mt-6 flex space-x-2">
                            <button onclick="alert('Downloading Physics Ch 5 PDF...')" class="flex-1 bg-indigo-600 hover:bg-indigo-700 text-white py-2 rounded-xl text-xs font-medium transition text-center shadow-sm">📥 Notes PDF</button>
                            <button onclick="alert('Starting Quiz: Light Formulas')" class="flex-1 bg-slate-100 hover:bg-slate-200 text-slate-700 py-2 rounded-xl text-xs font-medium transition text-center">📝 Quiz</button>
                        </div>
                    </div>

                    <!-- Biology Ch 9 -->
                    <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col justify-between">
                        <div>
                            <span class="bg-emerald-100 text-emerald-800 text-xs font-semibold px-3 py-1 rounded-full">Biology • Ch 9</span>
                            <h5 class="text-lg font-bold mt-3 text-slate-900">Life Processes</h5>
                            <p class="text-slate-500 text-sm mt-1">Nutrition, human respiratory & circulatory systems, and labeled diagram guides.</p>
                        </div>
                        <div class="mt-6 flex space-x-2">
                            <button onclick="alert('Downloading Biology Ch 9 PDF...')" class="flex-1 bg-indigo-600 hover:bg-indigo-700 text-white py-2 rounded-xl text-xs font-medium transition text-center shadow-sm">📥 Notes PDF</button>
                            <button onclick="alert('Starting Quiz: Life Processes')" class="flex-1 bg-slate-100 hover:bg-slate-200 text-slate-700 py-2 rounded-xl text-xs font-medium transition text-center">📝 Quiz</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- CLASS 10 MATHS CHAPTERS SECTION -->
            <div id="maths-section" class="mt-12">
                <h4 class="text-xl font-bold text-slate-800 mb-4 flex items-center gap-2">
                    <span>📐 Class 10 Mathematics</span>
                </h4>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <!-- Maths Ch 1 -->
                    <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col justify-between">
                        <div>
                            <span class="bg-purple-100 text-purple-800 text-xs font-semibold px-3 py-1 rounded-full">Maths • Ch 1</span>
                            <h5 class="text-lg font-bold mt-3 text-slate-900">Real Numbers</h5>
                            <p class="text-slate-500 text-sm mt-1">Fundamental theorem of arithmetic, rational/irrational proofs, and formulas.</p>
                        </div>
                        <div class="mt-6 flex space-x-2">
                            <button onclick="alert('Downloading Maths Ch 1 PDF...')" class="flex-1 bg-indigo-600 hover:bg-indigo-700 text-white py-2 rounded-xl text-xs font-medium transition text-center shadow-sm">📥 Notes PDF</button>
                            <button onclick="alert('Starting Quiz: Real Numbers')" class="flex-1 bg-slate-100 hover:bg-slate-200 text-slate-700 py-2 rounded-xl text-xs font-medium transition text-center">📝 Quiz</button>
                        </div>
                    </div>

                    <!-- Maths Ch 2 -->
                    <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col justify-between">
                        <div>
                            <span class="bg-purple-100 text-purple-800 text-xs font-semibold px-3 py-1 rounded-full">Maths • Ch 2</span>
                            <h5 class="text-lg font-bold mt-3 text-slate-900">Polynomials</h5>
                            <p class="text-slate-500 text-sm mt-1">Geometrical meaning of zeroes, relationship between coefficients and zeroes.</p>
                        </div>
                        <div class="mt-6 flex space-x-2">
                            <button onclick="alert('Downloading Maths Ch 2 PDF...')" class="flex-1 bg-indigo-600 hover:bg-indigo-700 text-white py-2 rounded-xl text-xs font-medium transition text-center shadow-sm">📥 Notes PDF</button>
                            <button onclick="alert('Starting Quiz: Polynomials')" class="flex-1 bg-slate-100 hover:bg-slate-200 text-slate-700 py-2 rounded-xl text-xs font-medium transition text-center">📝 Quiz</button>
                        </div>
                    </div>

                    <!-- Maths Ch 8 -->
                    <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col justify-between">
                        <div>
                            <span class="bg-purple-100 text-purple-800 text-xs font-semibold px-3 py-1 rounded-full">Maths • Ch 8</span>
                            <h5 class="text-lg font-bold mt-3 text-slate-900">Introduction to Trigonometry</h5>
                            <p class="text-slate-500 text-sm mt-1">Trigonometric ratios, table of specific values, and identity proof shortcuts.</p>
                        </div>
                        <div class="mt-6 flex space-x-2">
                            <button onclick="alert('Downloading Maths Ch 8 PDF...')" class="flex-1 bg-indigo-600 hover:bg-indigo-700 text-white py-2 rounded-xl text-xs font-medium transition text-center shadow-sm">📥 Notes PDF</button>
                            <button onclick="alert('Starting Quiz: Trigonometry')" class="flex-1 bg-slate-100 hover:bg-slate-200 text-slate-700 py-2 rounded-xl text-xs font-medium transition text-center">📝 Quiz</button>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-slate-900 text-slate-400 py-12 mt-20 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <div class="flex items-center justify-center space-x-2 mb-3">
                <span class="text-xl font-bold text-white flex items-center gap-2">🚀 StudySphere</span>
            </div>
            <p class="text-sm max-w-md mx-auto">Empowering school students everywhere with free, high-quality chapter-wise learning resources and automatically updated syllabi.</p>
            <p class="text-xs text-slate-500 mt-8">&copy; 2026 StudySphere. Built with ❤️ for Students.</p>
        </div>
    </footer>

    <script>
        function selectClass(className) {
            document.getElementById('currentSelectionTitle').innerText = `Study Material & Syllabus for ${className}`;
            window.location.hash = '#materials';
        }

        function filterMaterials() {
            const query = document.getElementById('searchInput').value;
            if(query.trim() !== '') {
                alert(`Searching study database for: "${query}"`);
            } else {
                alert('Please enter a chapter or subject name to search.');
            }
        }
    </script>
</body>
</html>
