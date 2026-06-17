<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2Plus.com</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-slate-900 text-slate-100 font-sans min-h-screen flex flex-col justify-between pb-16 md:pb-0">

    <!-- 1. NAVIGATION BAR -->
    <nav class="bg-slate-950 border-b border-slate-800 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <span class="text-2xl font-black tracking-wider text-emerald-500">2<span class="text-white">PLUS</span></span>
            </div>
            <div class="hidden md:flex items-center gap-6 text-sm font-medium">
                <a href="#features" class="hover:text-emerald-400 transition">Benefits</a>
                <a href="#how-it-works" class="hover:text-emerald-400 transition">How it Works</a>
                <a href="#pricing" class="hover:text-emerald-400 transition">Payment</a>
            </div>
            <div class="flex items-center gap-3">
                <button onclick="toggleView('landing')" class="text-sm font-medium hover:text-emerald-400 transition">Logout</button>
                <button onclick="toggleView('dashboard')" class="bg-emerald-500 hover:bg-emerald-600 text-slate-950 font-bold px-4 py-2 rounded-lg text-sm transition shadow-lg shadow-emerald-500/20">Demo Dashboard</button>
            </div>
        </div>
    </nav>

    <!-- ========================================== -->
    <!-- 2. PUBLIC LANDING PAGE SECTION -->
    <!-- ========================================== -->
    <main id="landing-page" class="flex-grow">
        <!-- Hero Banner -->
        <section class="relative py-20 px-4 text-center overflow-hidden bg-gradient-to-b from-slate-950 to-slate-900">
            <div class="max-w-3xl mx-auto relative z-10">
                <span class="bg-emerald-500/10 text-emerald-400 text-xs font-semibold px-3 py-1 rounded-full border border-emerald-500/20 uppercase tracking-widest">Expert Daily Picks</span>
                <h1 class="text-4xl md:text-6xl font-extrabold mt-6 tracking-tight leading-tight">
                    Win <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-teal-200">Instantly</span>
                </h1>
                <p class="text-slate-400 mt-4 text-lg md:text-xl max-w-xl mx-auto">
                    Odds updated every day. For disciplined members looking for long-term profitability.
                </p>
                <div class="mt-10 flex flex-col sm:flex-row gap-4 justify-center">
                    <a href="#pricing" class="bg-emerald-500 hover:bg-emerald-600 text-slate-950 font-bold text-lg px-8 py-4 rounded-xl transition shadow-xl shadow-emerald-500/20">Get Today's Slip</a>
                    <button onclick="toggleView('dashboard')" class="bg-slate-800 hover:bg-slate-700 border border-slate-700 font-medium text-lg px-8 py-4 rounded-xl transition">View Live Demo</button>
                </div>
            </div>
        </section>
    <!-- Benefits Grid -->
        <section id="features" class="max-w-7xl mx-auto px-4 py-16">
            <h2 class="text-2xl md:text-3xl font-bold text-center mb-12">Why Choose 2Plus?</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-slate-800/50 p-6 rounded-2xl border border-slate-700/50">
                    <div class="w-12 h-12 bg-emerald-500/10 text-emerald-400 rounded-xl flex items-center justify-center text-xl mb-4"><i class="fa-solid fa-chart-line"></i></div>
                    <h3 class="text-lg font-bold mb-2">Expert Selections</h3>
                    <p class="text-slate-400 text-sm">Not random guesses. Our algorithms review deep statistics for every single pick.</p>
                </div>
                <div class="bg-slate-800/50 p-6 rounded-2xl border border-slate-700/50">
                    <div class="w-12 h-12 bg-emerald-500/10 text-emerald-400 rounded-xl flex items-center justify-center text-xl mb-4"><i class="fa-solid fa-shield-halved"></i></div>
                    <h3 class="text-lg font-bold mb-2">Safe & Analyzed Odds</h3>
                    <p class="text-slate-400 text-sm">We prioritize consistency and risk management over unrealistic multi-bets. Quality over quantity.</p>
                </div>
                <div class="bg-slate-800/50 p-6 rounded-2xl border border-slate-700/50">
                    <div class="w-12 h-12 bg-emerald-500/10 text-emerald-400 rounded-xl flex items-center justify-center text-xl mb-4"><i class="fa-solid fa-bolt"></i></div>
                    <h3 class="text-lg font-bold mb-2">Instant Notifications</h3>
                    <p class="text-slate-400 text-sm">Get real-time SMS, Push, or Email notifications the second today's premium slip drops.</p>
                </div>
            </div>
        </section>

        <!-- Pricing Section -->
        <section id="pricing" class="max-w-7xl mx-auto px-4 py-16 bg-slate-950/40 rounded-3xl my-8 border border-slate-800">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold">Simple, Transparent Pricing</h2>
                <p class="text-slate-400 mt-2">Unlock daily premium access instantly via Mobile Money or Cards</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl mx-auto">
                <!-- Daily -->
                <div class="bg-slate-800/40 p-8 rounded-2xl border border-slate-700 relative flex flex-col justify-between">
                    <div>
                        <h3 class="text-xl font-bold">Daily Pass</h3>
                        <div class="mt-4 mb-6">
                            <span class="text-3xl font-extrabold text-white">TZS 25,000</span>
                            <span class="text-slate-400 text-sm block"><strong>$10 USD</strong></span>
                        </div>
                        <p class="text-sm text-slate-400">Perfect for trying out our premium selection accuracy.</p>
                    </div>
                    <button onclick="openPaymentModal('Daily Pass', 'TZS 25,000')" class="w-full mt-8 bg-slate-700 hover:bg-slate-600 font-bold py-3 rounded-xl transition">Subscribe Now</button>
                </div>
                <!-- Weekly -->
                <div class="bg-slate-800/80 p-8 rounded-2xl border-2 border-emerald-500 relative flex flex-col justify-between shadow-xl shadow-emerald-500/5">
                    <span class="absolute -top-3 left-1/2 -translate-x-1/2 bg-emerald-500 text-slate-950 font-black text-xs px-3 py-1 rounded-full uppercase">Most Popular</span>
                    <div>
                        <h3 class="text-xl font-bold">Weekly Access</h3>
                        <div class="mt-4 mb-6">
                            <span class="text-3xl font-extrabold text-white">TZS 90,000</span>
                            <span class="text-slate-400 text-sm block"><strong>$35 USD</strong></span>
                        </div>
                        <p class="text-sm text-slate-400">Save big compared to daily passes. Complete 7-day coverage.</p>
                    </div>
                    <button onclick="openPaymentModal('Weekly Access', 'TZS 90,000')" class="w-full mt-8 bg-emerald-500 hover:bg-emerald-600 text-slate-950 font-bold py-3 rounded-xl transition">Subscribe Now</button>
                </div>
                <!-- Monthly -->
                <div class="bg-slate-800/40 p-8 rounded-2xl border border-slate-700 relative flex flex-col justify-between">
                    <div>
                        <h3 class="text-xl font-bold">Monthly VIP</h3>
                        <div class="mt-4 mb-6">
                            <span class="text-3xl font-extrabold text-white">TZS 350,000</span>
                            <span class="text-slate-400 text-sm block"><strong>$135 USD</strong></span>
                        </div>
                        <p class="text-sm text-slate-400">Maximum value for long term investment with dedicated VIP features.</p>
                    </div>
                    <button onclick="openPaymentModal('Monthly VIP', 'TZS 350,000')" class="w-full mt-8 bg-slate-700 hover:bg-slate-600 font-bold py-3 rounded-xl transition">Subscribe Now</button>
                </div>
            </div>
        </section>
    </main>

    <!-- ========================================== -->
    <!-- 3. USER DASHBOARD SECTION (HIDDEN BY DEFAULT) -->
    <!-- ========================================== -->
    <main id="dashboard-page" class="hidden flex-grow max-w-7xl mx-auto w-full px-4 py-8">
        <!-- Welcome Section -->
        <div class="bg-gradient-to-r from-slate-950 to-slate-900 border border-slate-800 rounded-2xl p-6 flex flex-col md:flex-row justify-between items-start md:items-center gap-4 mb-8">
            <div>
                <h2 class="text-xl md:text-2xl font-bold">Welcome Back, its.afro👋</h2>
                <p class="text-slate-400 text-sm mt-1">Track your dashboard updates here.</p>
            </div>
            <div class="flex items-center gap-3 bg-emerald-500/10 border border-emerald-500/20 px-4 py-2 rounded-xl">
                <span class="w-2.5 h-2.5 rounded-full bg-emerald-400 animate-pulse"></span>
                <div class="text-xs">
                    <p class="font-bold text-emerald-400 uppercase tracking-wider">Active Subscriber</p>
                    <p class="text-slate-400">Expires: June 24, 2026</p>
                </div>
            </div>
        </div>

        <!-- Dashboard Content Grid -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            <!-- Left/Center: Today Game -->
            <div class="lg:col-span-2 space-y-6">
                <div class="bg-slate-950 border border-slate-800 rounded-2xl overflow-hidden">
                    <div class="bg-gradient-to-r from-emerald-500 to-teal-600 p-4 flex justify-between items-center text-slate-950">
                        <div class="flex items-center gap-2 font-bold text-lg">
                            <i class="fa-solid fa-star"></i> Today Game
                        </div>
                        <span class="bg-slate-950/20 px-3 py-1 rounded-full text-xs font-black">Confidence: 95%</span>
                    </div>
                    
                    <!-- Slip Selections -->
                    <div class="p-6 divide-y divide-slate-800">
                    
                        <!-- Match -->
                        <div class="py-4 last:pb-0">
                            <div class="flex justify-between items-start text-xs text-slate-400 mb-1">
                                <span> La Liga</span>
                                <span>Kick-off: 22:00 EAT</span>
                            </div>
                            <div class="flex justify-between items-center">
                                <h4 class="font-bold text-base">Real Madrid vs Real Betis</h4>
                                <span class="bg-emerald-500/10 text-emerald-400 px-2 py-1 rounded font-mono font-bold text-sm">Tip: Under 2.5 Goals</span>
                            </div>
                            <p class="text-xs text-slate-500 mt-1">Odds: 2.48</p>
                        </div>
                    </div>

                    <!-- Slip Total Footer -->
                    <div class="bg-slate-900/60 p-4 border-t border-slate-800 flex justify-between items-center">
                        <div>
                            <span class="text-slate-400 text-xs uppercase font-bold">Total Odds</span>
                            <p class="text-2xl font-black font-mono text-emerald-400">2.48</p>
                        </div>
                    
                    </div>
                </div>

                <!-- Previous History Preview -->
                <div class="bg-slate-950 border border-slate-800 rounded-2xl p-6">
                    <h3 class="font-bold text-lg mb-4 flex items-center justify-between">
                        <span>Recent Betslip History</span>
                        <a href="#" class="text-xs text-emerald-400 hover:underline">View All History</a>
                    </h3>
                    <div class="overflow-x-auto">
                        <table class="w-full text-left text-sm">
                            <thead>
                                <tr class="text-slate-500 border-b border-slate-800 text-xs uppercase">
                                    <th class="pb-3">Date</th>
                                    <th class="pb-3">Total Odds</th>
                                    <th class="pb-3 text-right">Result</th>
                                </tr>
                            </thead>
                            <tbody class="divide-y divide-slate-800/40">
                                <tr>
                                    <td class="py-3 text-slate-300">Yesterday</td>
                                    <td class="py-3 font-mono">2.15</td>
                                    <td class="py-3 text-right text-emerald-400 font-bold"><span class="bg-emerald-500/10 px-2 py-0.5 rounded text-xs">WON</span></td>
                                </tr>
                                <tr>
                                    <td class="py-3 text-slate-300">June 15, 2026</td>
                                    <td class="py-3 font-mono">3.40</td>
                                    <td class="py-3 text-right text-emerald-400 font-bold"><span class="bg-emerald-500/10 px-2 py-0.5 rounded text-xs">WON</span></td>
                                </tr>
                                <tr>
                                    <td class="py-3 text-slate-300">June 14, 2026</td>
                                    <td class="py-3 font-mono">2.05</td>
                                    <td class="py-3 text-right text-rose-400 font-bold"><span class="bg-rose-500/10 px-2 py-0.5 rounded text-xs">LOST</span></td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>

            <!-- Right: Account Overview & Actions -->
            <div class="space-y-6">
                <!-- Notifications panel -->
                <div class="bg-slate-950 border border-slate-800 rounded-2xl p-6">
                    <h3 class="font-bold text-lg mb-4 flex items-center gap-2"><i class="fa-solid fa-bell text-emerald-400"></i> Platform Alerts</h3>
                    <div class="space-y-3">
                        <div class="bg-slate-900 p-3 rounded-xl border border-slate-800/60 text-xs">
                            <span class="text-slate-500 block mb-1">Today @ 14:10</span>
                            <p class="text-slate-300 font-medium">🔥 Today's Premium Slip has been posted and verified!</p>
                        </div>
                        <div class="bg-slate-900 p-3 rounded-xl border border-slate-800/60 text-xs">
                            <span class="text-slate-500 block mb-1">Yesterday @ 09:00</span>
                            <p class="text-slate-300">Your account renewal is scheduled for June 24th via auto-remit.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- ========================================== -->
    <!-- 4. CHECKOUT / SUBSCRIPTION PAYMENT MODAL -->
    <!-- ========================================== -->
    <div id="payment-modal" class="fixed inset-0 bg-slate-950/80 backdrop-blur-sm hidden items-center justify-center z-50 p-4">
        <div class="bg-slate-900 border border-slate-800 rounded-3xl w-full max-w-md overflow-hidden shadow-2xl">
            <div class="p-6 border-b border-slate-800 flex justify-between items-center">
                <h3 class="font-bold text-xl text-white">Complete Secure Checkout</h3>
                <button onclick="closePaymentModal()" class="text-slate-400 hover:text-white"><i class="fa-solid fa-xmark text-xl"></i></button>
            </div>
            <div class="p-6">
                <div class="bg-slate-950 p-4 rounded-xl border border-slate-800 flex justify-between items-center mb-6">
                    <div>
                        <span class="text-xs text-slate-400 uppercase tracking-wider block">Selected Plan</span>
                        <span id="modal-plan-name" class="font-bold text-white text-base">Weekly Access</span>
                    </div>
                    <span id="modal-plan-price" class="text-emerald-400 font-mono font-black text-xl">TZS 90,000</span>
                </div>
                <div class="space-y-4">
                    <div>
                        <label class="text-xs text-slate-400 block mb-1">Mobile Money Number / Card Number</label>
                        <input type="tel" placeholder="e.g. 0712345678 / 5505123456789012" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-sm focus:outline-none focus:border-emerald-500">
                    </div>
                    <button onclick="simulatePaymentSuccess()" class="w-full bg-emerald-500 hover:bg-emerald-600 text-slate-950 font-bold py-3.5 rounded-xl transition text-sm">
                        Send USSD Request
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- 5. BOTTOM NAVIGATION FOR MOBILE DEPLOYMENT -->
    <div class="fixed bottom-0 left-0 right-0 bg-slate-950 border-t border-slate-800 grid grid-cols-4 h-16 md:hidden z-40 text-center text-slate-400">
        <button onclick="toggleView('landing')" class="flex flex-col items-center justify-center gap-1 text-xs hover:text-white transition">
            <i class="fa-solid fa-house text-lg"></i><span>Home</span>
        </button>
        <button onclick="toggleView('dashboard')" class="flex flex-col items-center justify-center gap-1 text-xs hover:text-white transition">
            <i class="fa-solid fa-bullseye text-lg"></i><span>Betslips</span>
        </button>
        <a href="#pricing" onclick="toggleView('landing')" class="flex flex-col items-center justify-center gap-1 text-xs hover:text-white transition">
            <i class="fa-solid fa-credit-card text-lg"></i><span>Subscribe</span>
        </a>
        <button onclick="toggleView('dashboard')" class="flex flex-col items-center justify-center gap-1 text-xs hover:text-white transition">
            <i class="fa-solid fa-user text-lg"></i><span>Profile</span>
        </button>
    </div>

    <!-- 6. FOOTER DESKTOP -->
    <footer class="bg-slate-950 border-t border-slate-800 py-6 px-4 text-center text-xs text-slate-500">
        &copy; 2026 2Plus Platform. All rights reserved. 18+ Gamble Responsibly.
    </footer>

    <!-- INTERACTIVE SCRIPTING TOGGLES -->
    <script>
        function toggleView(view) {
            const landing = document.getElementById('landing-page');
            const dashboard = document.getElementById('dashboard-page');
            if (view === 'dashboard') {
                landing.classList.add('hidden');
                dashboard.classList.remove('hidden');
                window.scrollTo({ top: 0, behavior: 'smooth' });
            } else {
                dashboard.classList.add('hidden');
                landing.classList.remove('hidden');
            }
        }
        function openPaymentModal(plan, price) {
            document.getElementById('modal-plan-name').innerText = plan;
            document.getElementById('modal-plan-price').innerText = price;
            document.getElementById('payment-modal').classList.remove('hidden');
            document.getElementById('payment-modal').classList.add('flex');
        }
        function closePaymentModal() {
            document.getElementById('payment-modal').classList.remove('flex');
            document.getElementById('payment-modal').classList.add('hidden');
        }
        function simulatePaymentSuccess() {
            alert("USSD Request Sent ! Once confirmed, your selected plan will activate instantly.");
            closePaymentModal();
            toggleView('dashboard');
        }
    </script>
</body>
</html>
