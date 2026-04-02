# HB-MOBILE<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HB Mobile - Official Site</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: { hbDark: '#1a1a2e', hbAccent: '#e94560' }
                }
            }
        }
    </script>
    <style>
        .page-section { display: none; }
        .page-section.active { display: block; }
        .nav-link.active { color: #e94560; border-bottom: 2px solid #e94560; }
    </style>
</head>
<body class="bg-gray-50 text-gray-900 transition-colors duration-300">

    <header class="bg-white shadow-md sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center gap-3">
                <img src="https://miaoda-conversation-file.s3cdn.medo.dev/user-aoxd71nyb5s0/20260403/file-aoxdl2s24agw.jpg" alt="HB Logo" class="h-10 w-10 rounded-full">
                <span class="text-xl font-bold tracking-tighter">HB MOBILE</span>
            </div>
            
            <nav class="hidden md:flex gap-6 font-semibold text-sm uppercase">
                <a href="#" onclick="showPage('shop')" class="nav-link active py-1" id="nav-shop">Shop</a>
                <a href="#" onclick="showPage('topup')" class="nav-link py-1" id="nav-topup">Top-Up</a>
                <a href="#" onclick="showPage('admin')" class="nav-link py-1" id="nav-admin">Admin</a>
            </nav>

            <div class="flex gap-3">
                <button id="langToggle" class="px-3 py-1 bg-hbDark text-white rounded text-xs font-bold">සිංහල</button>
            </div>
        </div>
    </header>

    <section id="shop-page" class="page-section active max-w-7xl mx-auto p-6">
        <h2 class="text-2xl font-bold mb-6 lang-en">Mobile Accessories</h2>
        <h2 class="text-2xl font-bold mb-6 lang-si hidden">ජංගම දුරකථන උපාංග</h2>
        <div class="grid grid-cols-2 md:grid-cols-4 gap-6" id="productGrid">
            </div>
    </section>

    <section id="topup-page" class="page-section max-w-4xl mx-auto p-6">
        <div class="bg-hbDark text-white p-8 rounded-2xl shadow-xl">
            <h2 class="text-2xl font-bold mb-6 text-center lang-en">Game Top-Up Portal</h2>
            <h2 class="text-2xl font-bold mb-6 text-center lang-si hidden">ක්‍රීඩා Top-Up ද්වාරය</h2>
            
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-8">
                <div class="cursor-pointer border-2 border-gray-700 p-3 rounded-lg text-center hover:border-hbAccent transition" onclick="alert('Selected: Free Fire')">
                    <img src="https://placehold.co/80x80/e94560/ffffff?text=FF" class="mx-auto mb-2 rounded">
                    <p class="text-xs font-bold uppercase">Free Fire</p>
                </div>
                <div class="cursor-pointer border-2 border-gray-700 p-3 rounded-lg text-center hover:border-hbAccent transition" onclick="alert('Selected: PUBG')">
                    <img src="https://placehold.co/80x80/e94560/ffffff?text=PUBG" class="mx-auto mb-2 rounded">
                    <p class="text-xs font-bold uppercase">PUBG</p>
                </div>
                <div class="cursor-pointer border-2 border-gray-700 p-3 rounded-lg text-center hover:border-hbAccent transition" onclick="alert('Selected: MLBB')">
                    <img src="https://placehold.co/80x80/e94560/ffffff?text=MLBB" class="mx-auto mb-2 rounded">
                    <p class="text-xs font-bold uppercase">MLBB</p>
                </div>
                <div class="cursor-pointer border-2 border-gray-700 p-3 rounded-lg text-center hover:border-hbAccent transition" onclick="alert('Selected: HOK')">
                    <img src="https://placehold.co/80x80/e94560/ffffff?text=HOK" class="mx-auto mb-2 rounded">
                    <p class="text-xs font-bold uppercase text-[10px]">Honor of Kings</p>
                </div>
            </div>

            <div class="space-y-4">
                <input type="text" placeholder="Player ID" class="w-full bg-gray-800 p-3 rounded border border-gray-600 focus:outline-none focus:border-hbAccent">
                <select class="w-full bg-gray-800 p-3 rounded border border-gray-600 focus:outline-none focus:border-hbAccent">
                    <option>100 Diamonds - LKR 350</option>
                    <option>520 Diamonds - LKR 1800</option>
                </select>
                <button class="w-full bg-hbAccent py-3 rounded-lg font-bold text-lg hover:bg-red-600 transition">Pay via PayHere</button>
            </div>
        </div>
    </section>

    <section id="admin-page" class="page-section max-w-7xl mx-auto p-6">
        <div class="bg-white p-6 rounded-xl shadow-sm border">
            <div class="flex justify-between items-center mb-6">
                <h2 class="text-xl font-bold">Admin Dashboard</h2>
                <span class="text-sm text-gray-500">Log: jh_mobile@gmail.com</span>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-8">
                <div class="bg-blue-50 p-4 rounded-lg border border-blue-100">
                    <p class="text-xs text-blue-600 font-bold uppercase">Total Orders</p>
                    <p class="text-2xl font-bold">48</p>
                </div>
                <div class="bg-green-50 p-4 rounded-lg border border-green-100">
                    <p class="text-xs text-green-600 font-bold uppercase">Revenue</p>
                    <p class="text-2xl font-bold">LKR 125k</p>
                </div>
                <div class="bg-orange-50 p-4 rounded-lg border border-orange-100">
                    <p class="text-xs text-orange-600 font-bold uppercase">Pending Topups</p>
                    <p class="text-2xl font-bold">12</p>
                </div>
            </div>
            <table class="w-full text-left border-collapse">
                <tr class="bg-gray-100 text-xs font-bold uppercase">
                    <th class="p-3">Order ID</th>
                    <th class="p-3">Item</th>
                    <th class="p-3">Status</th>
                </tr>
                <tr class="border-b text-sm">
                    <td class="p-3">#1092</td>
                    <td class="p-3">FF Topup (520)</td>
                    <td class="p-3 text-orange-600 font-bold">Pending</td>
                </tr>
            </table>
        </div>
    </section>

    <script>
        const products = [
            { nameEn: "Sony Fast Charger", nameSi: "Sony වේගවත් චාජරය", price: "LKR 4,500", img: "https://placehold.co/300x300/1a1a2e/ffffff?text=Sony" },
            { nameEn: "Tempered Glass", nameSi: "තිර ආවරණය", price: "LKR 850", img: "https://placehold.co/300x300/1a1a2e/ffffff?text=Glass" },
            { nameEn: "Silicone Case", nameSi: "සිලිකොන් කවරය", price: "LKR 1,200", img: "https://placehold.co/300x300/1a1a2e/ffffff?text=Case" },
            { nameEn: "Gaming Headset", nameSi: "ගේමිං හෙඩ්සෙට්", price: "LKR 6,500", img: "https://placehold.co/300x300/1a1a2e/ffffff?text=Audio" }
        ];

        let currentLang = 'en';

        function renderProducts() {
            const grid = document.getElementById('productGrid');
            grid.innerHTML = products.map(p => `
                <div class="bg-white rounded-lg shadow-sm border p-4 hover:shadow-md transition">
                    <img src="${p.img}" class="w-full h-40 object-cover rounded mb-4">
                    <h3 class="font-bold text-sm mb-2">${currentLang === 'en' ? p.nameEn : p.nameSi}</h3>
                    <p class="text-hbAccent font-bold mb-4">${p.price}</p>
                    <button class="w-full bg-hbDark text-white py-2 rounded text-xs uppercase font-bold hover:opacity-90">Add to Cart</button>
                </div>
            `).join('');
        }

        function showPage(pageId) {
            document.querySelectorAll('.page-section').forEach(p => p.classList.remove('active'));
            document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
            document.getElementById(pageId + '-page').classList.add('active');
            document.getElementById('nav-' + pageId).classList.add('active');
        }

        document.getElementById('langToggle').addEventListener('click', function() {
            currentLang = currentLang === 'en' ? 'si' : 'en';
            this.textContent = currentLang === 'en' ? 'සිංහල' : 'English';
            document.querySelectorAll('.lang-en').forEach(el => el.classList.toggle('hidden'));
            document.querySelectorAll('.lang-si').forEach(el => el.classList.toggle('hidden'));
            renderProducts();
        });

        renderProducts();
    </script>
</body>
</html>
