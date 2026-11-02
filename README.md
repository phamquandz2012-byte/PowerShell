<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shop King Game - Chuyên Mua Bán Acc Game Uy Tín</title>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6c5ce7;
            --primary-hover: #5b4bc4;
            --secondary: #a29bfe;
            --dark-bg: #0f0f1b;
            --card-bg: rgba(255, 255, 255, 0.06);
            --card-hover: rgba(255, 255, 255, 0.12);
            --light: #dfe6e9;
            --text-gray: #a0aec0;
            --success: #00b894;
            --danger: #d63031;
            --warning: #fdcb6e;
            --accent-gold: #ffd700;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0d0e15 0%, #1a1a2e 50%, #16213e 100%);
            color: #fff;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        /* Scrollbar styling */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0f0f1b;
        }
        ::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 4px;
        }

        /* Header & Navbar */
        header {
            background: rgba(15, 15, 27, 0.95);
            backdrop-filter: blur(10px);
            padding: 15px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 20px rgba(0,0,0,0.6);
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }

        .logo {
            font-size: 26px;
            font-weight: 800;
            color: #fff;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
            letter-spacing: 0.5px;
        }
        .logo span {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 25px;
        }
        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
        }
        .nav-links a:hover {
            color: var(--secondary);
            transform: translateY(-2px);
        }

        .cart-icon-wrapper {
            position: relative;
        }
        .cart-badge {
            position: absolute;
            top: -8px;
            right: -12px;
            background: var(--danger);
            color: white;
            border-radius: 50%;
            padding: 2px 7px;
            font-size: 11px;
            font-weight: bold;
            box-shadow: 0 0 8px rgba(214, 48, 49, 0.8);
        }

        /* Container */
        .container {
            max-width: 1250px;
            margin: 0 auto;
            padding: 30px 20px;
            flex: 1;
        }

        /* Hero Banner */
        .hero {
            text-align: center;
            padding: 60px 20px;
            background: radial-gradient(circle, rgba(108,92,231,0.3) 0%, rgba(15,15,27,0.7) 100%);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 20px;
            margin-bottom: 35px;
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.4);
        }
        .hero h1 {
            font-size: 42px;
            margin-bottom: 15px;
            font-weight: 800;
            background: linear-gradient(45deg, #fff, var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .hero p {
            font-size: 18px;
            color: var(--light);
            max-width: 650px;
            margin: 0 auto;
            opacity: 0.9;
        }

        /* Controls Section (Search & Filters) */
        .controls-section {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin-bottom: 35px;
            background: rgba(255, 255, 255, 0.03);
            padding: 20px;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .search-box {
            position: relative;
            width: 100%;
        }
        .search-box i {
            position: absolute;
            left: 18px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--text-gray);
            font-size: 18px;
        }
        .search-bar {
            width: 100%;
            padding: 14px 20px 14px 50px;
            border: 1px solid rgba(255, 255, 255, 0.15);
            border-radius: 10px;
            font-size: 16px;
            background: rgba(0, 0, 0, 0.4);
            color: #fff;
            outline: none;
            transition: all 0.3s ease;
        }
        .search-bar:focus {
            border-color: var(--primary);
            box-shadow: 0 0 12px rgba(108, 92, 231, 0.4);
        }

        .filters-wrapper {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        .category-filter {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        .category-btn {
            background: rgba(255,255,255,0.08);
            color: var(--light);
            padding: 10px 22px;
            border: 1px solid transparent;
            border-radius: 25px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .category-btn:hover {
            background: rgba(255,255,255,0.15);
            transform: translateY(-2px);
        }
        .category-btn.active {
            background: var(--primary);
            color: #fff;
            box-shadow: 0 4px 15px rgba(108, 92, 231, 0.4);
        }

        .sort-wrapper select {
            background: rgba(0,0,0,0.4);
            color: var(--light);
            border: 1px solid rgba(255,255,255,0.15);
            padding: 10px 15px;
            border-radius: 8px;
            outline: none;
            cursor: pointer;
            font-size: 14px;
        }

        /* Product Grid */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }

        .product-card {
            background: var(--card-bg);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 16px;
            padding: 18px;
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            position: relative;
            display: flex;
            flex-direction: column;
            overflow: hidden;
        }
        .product-card:hover {
            transform: translateY(-7px);
            background: var(--card-hover);
            box-shadow: 0 12px 30px rgba(0,0,0,0.5);
            border-color: rgba(108, 92, 231, 0.3);
        }

        .img-container {
            position: relative;
            width: 100%;
            height: 190px;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 15px;
        }
        .product-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        .product-card:hover img {
            transform: scale(1.05);
        }

        .badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background: linear-gradient(45deg, var(--danger), #ff7675);
            color: #fff;
            padding: 4px 10px;
            border-radius: 6px;
            font-size: 11px;
            font-weight: bold;
            box-shadow: 0 2px 8px rgba(0,0,0,0.4);
            text-transform: uppercase;
        }
        .badge.vip { background: linear-gradient(45deg, #f1c40f, #f39c12); color: #000; }
        .badge.hot { background: linear-gradient(45deg, #e74c3c, #c0392b); }
        .badge.top { background: linear-gradient(45deg, #9b59b6, #8e44ad); }

        .product-card h3 {
            font-size: 18px;
            font-weight: 700;
            margin-bottom: 12px;
            line-height: 1.3;
            color: #fff;
        }

        .product-specs {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 8px;
            margin-bottom: 15px;
            background: rgba(0,0,0,0.25);
            padding: 10px;
            border-radius: 8px;
            font-size: 13px;
        }
        .spec-item {
            color: var(--text-gray);
            display: flex;
            align-items: center;
            gap: 6px;
        }
        .spec-item strong {
            color: var(--light);
        }

        .price-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: auto;
            padding-top: 10px;
            border-top: 1px solid rgba(255,255,255,0.05);
        }
        .price {
            font-size: 20px;
            color: var(--success);
            font-weight: 800;
        }

        /* Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            background: var(--primary);
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 8px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        .btn:hover {
            background: var(--primary-hover);
            box-shadow: 0 4px 15px rgba(108,92,231,0.4);
        }
        .btn-success { background: var(--success); }
        .btn-success:hover { background: #00a383; }
        .btn-danger { background: var(--danger); }
        .btn-danger:hover { background: #c0392b; }

        .no-results {
            grid-column: 1 / -1;
            text-align: center;
            padding: 50px 0;
            color: var(--text-gray);
            font-size: 18px;
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(5px);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        .modal.show {
            display: flex;
            opacity: 1;
        }

        .modal-content {
            background: #161b26;
            padding: 30px;
            border-radius: 16px;
            max-width: 500px;
            width: 90%;
            border: 1px solid rgba(255,255,255,0.1);
            box-shadow: 0 20px 40px rgba(0,0,0,0.6);
            position: relative;
            transform: translateY(-20px);
            transition: transform 0.3s ease;
        }
        .modal.show .modal-content {
            transform: translateY(0);
        }

        .close-modal {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 24px;
            color: var(--text-gray);
            cursor: pointer;
            transition: color 0.3s;
        }
        .close-modal:hover { color: #fff; }

        .modal-title {
            font-size: 22px;
            font-weight: 700;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--secondary);
        }

        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 6px;
            font-size: 14px;
            color: var(--text-gray);
        }
        .form-control {
            width: 100%;
            padding: 12px;
            background: rgba(0,0,0,0.3);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 8px;
            color: #fff;
            font-size: 15px;
            outline: none;
        }
        .form-control:focus {
            border-color: var(--primary);
        }

        /* Cart Specifics */
        .cart-list {
            max-height: 280px;
            overflow-y: auto;
            margin-bottom: 20px;
        }
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px;
            background: rgba(255,255,255,0.03);
            border-radius: 8px;
            margin-bottom: 10px;
            border: 1px solid rgba(255,255,255,0.05);
        }
        .cart-item-title {
            font-weight: 600;
            font-size: 14px;
        }
        .cart-item-price {
            color: var(--success);
            font-weight: bold;
            font-size: 14px;
        }

        .cart-summary {
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 15px;
            margin-top: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 18px;
            font-weight: 700;
        }

        /* Notifications */
        .toast {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background: var(--success);
            color: #fff;
            padding: 14px 24px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.4);
            display: flex;
            align-items: center;
            gap: 10px;
            transform: translateY(100px);
            opacity: 0;
            transition: all 0.3s ease;
            z-index: 2000;
        }
        .toast.show {
            transform: translateY(0);
            opacity: 1;
        }

        /* Footer */
        footer {
            background: rgba(10, 10, 18, 0.95);
            border-top: 1px solid rgba(255,255,255,0.05);
            padding: 30px 20px;
            text-align: center;
            margin-top: 60px;
            color: var(--text-gray);
            font-size: 14px;
        }
        footer p {
            margin-bottom: 8px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 { font-size: 30px; }
            .filters-wrapper { flex-direction: column; align-items: stretch; }
            .nav-links span { display: none; }
        }
    </style>
</head>
<body>

    <!-- Header / Nav -->
    <header>
        <a href="#" class="logo">
            <i class="fa-solid fa-gamepad"></i>
            Shop<span>AccPro</span>
        </a>
        <nav class="nav-links">
            <a href="#products"><i class="fa-solid fa-store"></i> <span>Sản phẩm</span></a>
            <a href="#" onclick="openModal('loginModal')"><i class="fa-solid fa-right-to-bracket"></i> <span>Đăng nhập</span></a>
            <a href="#" onclick="openModal('cartModal')" class="cart-icon-wrapper">
                <i class="fa-solid fa-cart-shopping"></i>
                <span>Giỏ hàng</span>
                <span class="cart-badge" id="cartCount">0</span>
            </a>
        </nav>
    </header>

    <div class="container">
        <!-- Hero Banner -->
        <div class="hero">
            <h1>Sàn Giao Dịch Acc Game Số 1</h1>
            <p>Hệ thống bán tài khoản tự động, uy tín, bảo hành vĩnh viễn với mức giá ưu đãi nhất thị trường.</p>
        </div>

        <!-- Controls Section -->
        <div class="controls-section" id="products">
            <div class="search-box">
                <i class="fa-solid fa-magnifying-glass"></i>
                <input type="text" class="search-bar" id="searchInput" placeholder="Tìm kiếm theo tên acc, mã số...">
            </div>

            <div class="filters-wrapper">
                <div class="category-filter" id="categoryFilter">
                    <button class="category-btn active" data-category="all"><i class="fa-solid fa-border-all"></i> Tất cả</button>
                    <button class="category-btn" data-category="lien-quan"><i class="fa-solid fa-shield-halved"></i> Liên Quân</button>
                    <button class="category-btn" data-category="freefire"><i class="fa-solid fa-crosshairs"></i> Free Fire</button>
                    <button class="category-btn" data-category="ngoc-rong"><i class="fa-solid fa-dragon"></i> Ngọc Rồng</button>
                </div>

                <div class="sort-wrapper">
                    <select id="sortSelect">
                        <option value="default">Sắp xếp: Mặc định</option>
                        <option value="price-asc">Giá: Thấp đến Cao</option>
                        <option value="price-desc">Giá: Cao đến Thấp</option>
                    </select>
                </div>
            </div>
        </div>

        <!-- Product Grid -->
        <div class="product-grid" id="productGrid"></div>
    </div>

    <!-- Login Modal -->
    <div class="modal" id="loginModal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('loginModal')">&times;</span>
            <div class="modal-title"><i class="fa-solid fa-user-lock"></i> Đăng Nhập</div>
            <form onsubmit="handleLogin(event)">
                <div class="form-group">
                    <label>Tên tài khoản hoặc Email</label>
                    <input type="text" class="form-control" placeholder="Nhập tên tài khoản..." required>
                </div>
                <div class="form-group">
                    <label>Mật khẩu</label>
                    <input type="password" class="form-control" placeholder="Nhập mật khẩu..." required>
                </div>
                <button type="submit" class="btn" style="width: 100%; margin-top: 10px;">Đăng Nhập</button>
            </form>
            <p style="text-align: center; margin-top: 15px; font-size: 14px; color: var(--text-gray);">
                Chưa có tài khoản? <a href="#" style="color: var(--primary); text-decoration: none;">Đăng ký ngay</a>
            </p>
        </div>
    </div>

    <!-- Cart Modal -->
    <div class="modal" id="cartModal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('cartModal')">&times;</span>
            <div class="modal-title"><i class="fa-solid fa-cart-shopping"></i> Giỏ Hàng Của Bạn</div>
            <div class="cart-list" id="cartItems"></div>
            <div class="cart-summary">
                <span>Tổng tiền:</span>
                <span id="totalPrice" style="color: var(--success);">0 VNĐ</span>
            </div>
            <button class="btn btn-success" style="width: 100%; margin-top: 15px;" onclick="checkout()">
                <i class="fa-solid fa-credit-card"></i> Thanh Toán Ngay
            </button>
        </div>
    </div>

    <!-- Toast Notification -->
    <div class="toast" id="toast">
        <i class="fa-solid fa-circle-check"></i>
        <span id="toastMsg">Thông báo</span>
    </div>

    <!-- Footer -->
    <footer>
        <p>© 2026 ShopAccPro. All Rights Reserved.</p>
        <p style="font-size: 12px; color: #666;">Hệ thống giao dịch tài khoản game tự động an toàn 100%.</p>
    </footer>

    <!-- JavaScript Logic -->
    <script>
        const products = [
            {
                id: 1,
                title: "Acc Liên Quân Cao Thủ Full Tướng",
                category: "lien-quan",
                price: 250000,
                rank: "Cao Thủ",
                level: 30,
                heroes: "110/110",
                skins: 85,
                image: "https://images.unsplash.com/photo-1542751371-adc38448a05e?auto=format&fit=crop&w=600&q=80",
                badge: "HOT"
            },
            {
                id: 2,
                title: "Acc Free Fire VIP Súng 6 Sao",
                category: "freefire",
                price: 180000,
                rank: "Huyền Thoại",
                level: 52,
                heroes: "Đủ Nhân Vật",
                skins: 120,
                image: "https://images.unsplash.com/photo-1538481199705-c710c4e965fc?auto=format&fit=crop&w=600&q=80",
                badge: "MỚI"
            },
            {
                id: 3,
                title: "Acc Ngọc Rồng Server 1 Xayda VIP",
                category: "ngoc-rong",
                price: 350000,
                rank: "Sức Mạnh 80B",
                level: 120,
                heroes: "Đệ Tử Mabuu",
                skins: "Đủ Cải Trang",
                image: "https://images.unsplash.com/photo-1563089145-599997674d42?auto=format&fit=crop&w=600&q=80"
            },
            {
                id: 4,
                title: "Acc Liên Quân Thách Đấu SSS Skin",
                category: "lien-quan",
                price: 1200000,
                rank: "Thách Đấu",
                level: 30,
                heroes: "Full Tướng",
                skins: 210,
                image: "https://images.unsplash.com/photo-1511512578047-dfb367046420?auto=format&fit=crop&w=600&q=80",
                badge: "VIP"
            },
            {
                id: 5,
                title: "Acc Free Fire Trang Phục Quỷ Dạ Xoa",
                category: "freefire",
                price: 450000,
                rank: "Tướng Lĩnh",
                level: 65,
                heroes: "Full Nhân Vật",
                skins: 90,
                image: "https://images.unsplash.com/photo-1579373903781-fd5c0c30c4cd?auto=format&fit=crop&w=600&q=80"
            },
            {
                id: 6,
                title: "Acc Ngọc Rồng Bá Chủ Đệ Trái Đất",
                category: "ngoc-rong",
                price: 750000,
                rank: "Sức Mạnh 110B",
                level: 150,
                heroes: "Đệ Tử Siêu Cấp",
                skins: "Găng 8 Sao",
                image: "https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&fit=crop&w=600&q=80",
                badge: "TOP"
            }
        ];

        let cart = JSON.parse(localStorage.getItem('shop_cart')) || [];
        let currentCategory = 'all';

        // Display Products
        function displayProducts() {
            const grid = document.getElementById('productGrid');
            const searchTerm = document.getElementById('searchInput').value.toLowerCase();
            const sortValue = document.getElementById('sortSelect').value;
            
            // Filter
            let filtered = products.filter(p => {
                const matchCategory = currentCategory === 'all' || p.category === currentCategory;
                const matchSearch = p.title.toLowerCase().includes(searchTerm) || p.id.toString().includes(searchTerm);
                return matchCategory && matchSearch;
            });

            // Sort
            if (sortValue === 'price-asc') {
                filtered.sort((a, b) => a.price - b.price);
            } else if (sortValue === 'price-desc') {
                filtered.sort((a, b) => b.price - a.price);
            }

            if (filtered.length === 0) {
                grid.innerHTML = `<div class="no-results"><i class="fa-solid fa-box-open" style="font-size: 40px; margin-bottom: 10px;"></i><br>Không tìm thấy tài khoản phù hợp</div>`;
                return;
            }

            grid.innerHTML = filtered.map(p => `
                <div class="product-card">
                    <div class="img-container">
                        ${p.badge ? `<span class="badge ${p.badge.toLowerCase()}">${p.badge}</span>` : ''}
                        <img src="${p.image}" alt="${p.title}" loading="lazy">
                    </div>
                    <h3>${p.title}</h3>
                    <div class="product-specs">
                        <div class="spec-item"><i class="fa-solid fa-trophy"></i> <strong>${p.rank}</strong></div>
                        <div class="spec-item"><i class="fa-solid fa-chart-line"></i> Lv: <strong>${p.level}</strong></div>
                        <div class="spec-item"><i class="fa-solid fa-user-shield"></i> <strong>${p.heroes}</strong></div>
                        <div class="spec-item"><i class="fa-solid fa-shirt"></i> Trang phục: <strong>${p.skins}</strong></div>
                    </div>
                    <div class="price-row">
                        <div class="price">${formatPrice(p.price)}đ</div>
                        <button class="btn" onclick="addToCart(${p.id})">
                            <i class="fa-solid fa-cart-plus"></i> Mua
                        </button>
                    </div>
                </div>
            `).join('');
        }

        // Helper: Format Price
        function formatPrice(price) {
            return price.toLocaleString('vi-VN');
        }

        // Cart Actions
        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            if (!cart.some(item => item.id === productId)) {
                cart.push(product);
                saveCart();
                showToast(`Đã thêm MS#${product.id} vào giỏ hàng!`);
            } else {
                showToast(`Tài khoản này đã có trong giỏ hàng!`);
            }
        }

        function removeFromCart(index) {
            cart.splice(index, 1);
            saveCart();
        }

        function saveCart() {
            localStorage.setItem('shop_cart', JSON.stringify(cart));
            updateCartUI();
        }

        function updateCartUI() {
            const cartItems = document.getElementById('cartItems');
            const cartCount = document.getElementById('cartCount');
            const totalPriceEl = document.getElementById('totalPrice');

            cartCount.innerText = cart.length;

            if (cart.length === 0) {
                cartItems.innerHTML = '<p style="text-align: center; color: var(--text-gray); padding: 20px;">Giỏ hàng trống</p>';
                totalPriceEl.innerText = '0 VNĐ';
                return;
            }

            let total = 0;
            cartItems.innerHTML = cart.map((item, index) => {
                total += item.price;
                return `
                    <div class="cart-item">
                        <div>
                            <div class="cart-item-title">${item.title}</div>
                            <div class="cart-item-price">${formatPrice(item.price)} VNĐ</div>
                        </div>
                        <button class="btn btn-danger" style="padding: 6px 10px; font-size: 12px;" onclick="removeFromCart(${index})">
                            <i class="fa-solid fa-trash"></i>
                        </button>
                    </div>
                `;
            }).join('');

            totalPriceEl.innerText = formatPrice(total) + ' VNĐ';
        }

        function checkout() {
            if (cart.length === 0) {
                alert('Giỏ hàng của bạn đang trống!');
                return;
            }
            alert('Cảm ơn bạn đã đặt hàng! Hệ thống sẽ chuyển sang trang thanh toán.');
            cart = [];
            saveCart();
            closeModal('cartModal');
        }

        // Modals Logic
        function openModal(id) {
            const modal = document.getElementById(id);
            modal.classList.add('show');
        }

        function closeModal(id) {
            const modal = document.getElementById(id);
            modal.classList.remove('show');
        }

        function handleLogin(e) {
            e.preventDefault();
            showToast('Đăng nhập thành công!');
            closeModal('loginModal');
        }

        // Toast Notification
        function showToast(msg) {
            const toast = document.getElementById('toast');
            document.getElementById('toastMsg').innerText = msg;
            toast.classList.add('show');
            setTimeout(() => {
                toast.classList.remove('show');
            }, 3000);
        }

        // Event Listeners
        document.querySelectorAll('.category-btn').forEach(btn => {
            btn.addEventListener('click', () => {
                document.querySelectorAll('.category-btn').forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                currentCategory = btn.dataset.category;
                displayProducts();
            });
        });

        document.getElementById('searchInput').addEventListener('input', displayProducts);
        document.getElementById('sortSelect').addEventListener('change', displayProducts);

        // Close modal when clicking background
        window.addEventListener('click', (e) => {
            if (e.target.classList.contains('modal')) {
                e.target.classList.remove('show');
            }
        });

        // Initialize App
        displayProducts();
        updateCartUI();
    </script>
</body>
</html>
