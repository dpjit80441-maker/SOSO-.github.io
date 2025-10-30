<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>九州之旅SOSO为您领航 - 专业九州旅游服务</title>
    <meta name="description" content="专业定制日本九州深度游，体验温泉、美食与自然奇观的完美之旅。私人定制游、精品小团游、主题特色游等多种服务。">
    <meta name="keywords" content="九州旅游,日本旅游,福冈,由布院,熊本,鹿儿岛,温泉之旅">
    <style>
        /* 基础样式 */
        :root {
            --primary-color: #e62e2e;
            --secondary-color: #2a5caa;
            --accent-color: #f7b500;
            --light-color: #f8f9fa;
            --dark-color: #333;
            --text-color: #444;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Helvetica Neue', Arial, 'Hiragino Sans GB', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            color: var(--text-color);
            line-height: 1.6;
            background-color: #fff;
            scroll-behavior: smooth;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--primary-color);
            color: white;
            border: none;
            border-radius: 4px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background-color: #c52626;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: var(--secondary-color);
        }
        
        .btn-secondary:hover {
            background-color: #234a8f;
        }
        
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.2rem;
            color: var(--dark-color);
            position: relative;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: var(--primary-color);
            margin: 15px auto;
        }
        
        /* 导航栏 */
        header {
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            z-index: 1000;
            transition: background-color 0.3s ease;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary-color);
        }
        
        .logo span {
            color: var(--secondary-color);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }
        
        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--primary-color);
            transition: width 0.3s;
        }
        
        .nav-links a:hover:after {
            width: 100%;
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* 英雄区域 */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://images.unsplash.com/photo-1528164344705-47542687000d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            display: flex;
            align-items: center;
            color: white;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            animation: fadeInUp 1s ease;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
        /* 服务区域 */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }
        
        .service-content {
            padding: 25px;
        }
        
        .service-content h3 {
            margin-bottom: 15px;
            font-size: 1.4rem;
        }
        
        /* 目的地区域 */
        .destinations {
            background-color: #f8f9fa;
        }
        
        .destinations-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .destination-card {
            position: relative;
            border-radius: 8px;
            overflow: hidden;
            height: 300px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .destination-img {
            width: 100%;
            height: 100%;
            background-size: cover;
            background-position: center;
            transition: transform 0.5s ease;
        }
        
        .destination-card:hover .destination-img {
            transform: scale(1.1);
        }
        
        .destination-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(0, 0, 0, 0.8));
            color: white;
            padding: 20px;
        }
        
        .destination-overlay h3 {
            margin-bottom: 5px;
        }
        
        /* 关于我们 */
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-img {
            flex: 1;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* 联系表单 */
        .contact {
            background-color: #f8f9fa;
        }
        
        .contact-form {
            max-width: 700px;
            margin: 0 auto;
            background: white;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-control:focus {
            border-color: var(--primary-color);
            outline: none;
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* 页脚 */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            margin-bottom: 20px;
            font-size: 1.2rem;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3:after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 2px;
            background-color: var(--primary-color);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }
        
        .footer-links li:before {
            content: '•';
            color: var(--primary-color);
            margin-right: 8px;
        }
        
        .footer-links a {
            color: #bbb;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .contact-info {
            color: #bbb;
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #444;
            color: #bbb;
            font-size: 0.9rem;
        }
        
        /* 加载动画 */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* 返回顶部按钮 */
        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background-color: var(--primary-color);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            z-index: 999;
        }
        
        .back-to-top.show {
            opacity: 1;
            visibility: visible;
        }
        
        /* 响应式设计 */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: white;
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links li {
                margin: 10px 0;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .section {
                padding: 60px 0;
            }
            
            .back-to-top {
                bottom: 20px;
                right: 20px;
                width: 40px;
                height: 40px;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">九州<span>之旅</span></a>
                <ul class="nav-links">
                    <li><a href="#home">首页</a></li>
                    <li><a href="#services">服务项目</a></li>
                    <li><a href="#destinations">九州目的地</a></li>
                    <li><a href="#about">关于我们</a></li>
                    <li><a href="#contact">联系我们</a></li>
                </ul>
                <div class="mobile-menu">☰</div>
            </nav>
        </div>
    </header>

    <!-- 英雄区域 -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>探索九州之美</h1>
                <p>专业定制日本九州深度游，体验温泉、美食与自然奇观的完美之旅</p>
                <a href="#contact" class="btn">立即咨询</a>
                <a href="#services" class="btn btn-secondary">查看服务</a>
            </div>
        </div>
    </section>

    <!-- 服务区域 -->
    <section class="section" id="services">
        <div class="container">
            <h2 class="section-title">我们的服务</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1544551763-46a013bb70d5?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80');"></div>
                    <div class="service-content">
                        <h3>私人定制游</h3>
                        <p>根据您的兴趣、预算和时间，量身打造专属九州行程，享受独一无二的旅行体验。</p>
                        <a href="#contact" class="btn" style="margin-top: 15px;">定制行程</a>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1524413840807-0c3cb6fa808d?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80');"></div>
                    <div class="service-content">
                        <h3>精品小团游</h3>
                        <p>加入我们精心设计的小团行程，结识志同道合的旅伴，深度体验九州文化。</p>
                        <a href="#contact" class="btn" style="margin-top: 15px;">查看行程</a>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-img" style="background-image: url('https://images.unsplash.com/photo-1570077188670-e3a8d69ac5ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80');"></div>
                    <div class="service-content">
                        <h3>主题特色游</h3>
                        <p>温泉疗养、美食探索、铁道之旅、历史文化等主题行程，满足您的特别兴趣。</p>
                        <a href="#contact" class="btn" style="margin-top: 15px;">探索主题</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 目的地区域 -->
    <section class="section destinations" id="destinations">
        <div class="container">
            <h2 class="section-title">九州热门目的地</h2>
            <div class="destinations-grid">
                <div class="destination-card">
                    <div class="destination-img" style="background-image: url('https://images.unsplash.com/photo-1545560622-ca76e1825da0?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80');"></div>
                    <div class="destination-overlay">
                        <h3>福冈</h3>
                        <p>美食与购物的天堂</p>
                    </div>
                </div>
                <div class="destination-card">
                    <div class="destination-img" style="background-image: url('https://images.unsplash.com/photo-1586773860418-df70f7e87ab5?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80');"></div>
                    <div class="destination-overlay">
                        <h3>由布院</h3>
                        <p>温泉与艺术的完美结合</p>
                    </div>
                </div>
                <div class="destination-card">
                    <div class="destination-img" style="background-image: url('https://images.unsplash.com/photo-1576675466969-38eeae4b41f6?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80');"></div>
                    <div class="destination-overlay">
                        <h3>熊本</h3>
                        <p>熊本熊与历史名城</p>
                    </div>
                </div>
                <div class="destination-card">
                    <div class="destination-img" style="background-image: url('https://images.unsplash.com/photo-1598970605070-1d4e5ebd4ff5?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80');"></div>
                    <div class="destination-overlay">
                        <h3>鹿儿岛</h3>
                        <p>火山与大海的壮丽景色</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 关于我们 -->
    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title">关于我们</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>九州旅游专家</h3>
                    <p>我们是一支专注于日本九州地区旅游服务的专业团队，拥有多年的本地旅游经验和深厚的文化理解。我们的使命是为每一位旅客提供独特、深入且难忘的九州旅行体验。</p>
                    <p>我们的团队成员包括资深行程策划师、本地向导和客户服务专家，他们熟悉九州的每一个角落，从热门的旅游景点到只有当地人才知道的隐秘宝藏。</p>
                    <p>我们坚信，真正的旅行不仅仅是参观景点，更是与当地文化、人民和生活方式建立深刻的联系。因此，我们设计的每一个行程都旨在让您深入了解九州的独特魅力。</p>
                    <a href="#contact" class="btn" style="margin-top: 20px;">了解更多</a>
                </div>
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1544551763-46a013bb70d5?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="我们的团队">
                </div>
            </div>
        </div>
    </section>

    <!-- 联系我们 -->
    <section class="section contact" id="contact">
        <div class="container">
            <h2 class="section-title">联系我们</h2>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">姓名</label>
                        <input type="text" id="name" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="email">邮箱</label>
                        <input type="email" id="email" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">电话</label>
                        <input type="tel" id="phone" class="form-control">
                    </div>
                    <div class="form-group">
                        <label for="interest">感兴趣的服务</label>
                        <select id="interest" class="form-control">
                            <option value="">请选择</option>
                            <option value="custom">私人定制游</option>
                            <option value="group">精品小团游</option>
                            <option value="theme">主题特色游</option>
                            <option value="other">其他</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">留言</label>
                        <textarea id="message" class="form-control" placeholder="请告诉我们您的需求、预算和旅行时间等信息..."></textarea>
                    </div>
                    <button type="submit" class="btn">提交咨询</button>
                </form>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>九州之旅</h3>
                    <p>专业日本九州旅游服务提供商，致力于为客户提供独特、深入的旅行体验。</p>
                </div>
                <div class="footer-column">
                    <h3>快速链接</h3>
                    <ul class="footer-links">
                        <li><a href="#home">首页</a></li>
                        <li><a href="#services">服务项目</a></li>
                        <li><a href="#destinations">九州目的地</a></li>
                        <li><a href="#about">关于我们</a></li>
                        <li><a href="#contact">联系我们</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>联系信息</h3>
                    <ul class="footer-links">
                        <li class="contact-info">邮箱：dpjit80441@yahoo.co.jp</li>
                        <li class="contact-info">地址：日本福冈市中央区天神X-X-X</li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>关注我们</h3>
                    <ul class="footer-links">
                        <li><a href="#">微信：huazhendong88</a></li>
                        <li><a href="mailto:dpjit80441@yahoo.co.jp">邮箱联系</a></li>
                        <li><a href="#">小红书：9647159871</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 九州之旅旅游服务公司 版权所有</p>
            </div>
        </div>
    </footer>

    <!-- 返回顶部按钮 -->
    <div class="back-to-top" id="backToTop">↑</div>

    <script>
        // 移动端菜单切换
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });
        
        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // 关闭移动端菜单
                    document.querySelector('.nav-links').classList.remove('active');
                }
            });
        });
        
        // 表单提交
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // 获取表单数据
            const formData = {
                name: document.getElementById('name').value,
                email: document.getElementById('email').value,
                phone: document.getElementById('phone').value,
                interest: document.getElementById('interest').value,
                message: document.getElementById('message').value
            };
            
            // 这里可以添加表单提交到服务器的代码
            console.log('表单数据:', formData);
            
            alert('感谢您的咨询！我们会尽快与您联系。');
            this.reset();
        });
        
        // 导航栏滚动效果
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if(window.scrollY > 100) {
                header.style.backgroundColor = 'rgba(255, 255, 255, 0.98)';
            } else {
                header.style.backgroundColor = 'rgba(255, 255, 255, 0.95)';
            }
            
            // 显示/隐藏返回顶部按钮
            const backToTop = document.getElementById('backToTop');
            if (window.scrollY > 300) {
                backToTop.classList.add('show');
            } else {
                backToTop.classList.remove('show');
            }
        });
        
        // 返回顶部功能
        document.getElementById('backToTop').addEventListener('click', function() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // 图片懒加载
        document.addEventListener('DOMContentLoaded', function() {
            const lazyImages = document.querySelectorAll('.service-img, .destination-img');
            
            const imageObserver = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const img = entry.target;
                        // 这里可以添加实际的懒加载逻辑
                        // 例如从data-src属性加载图片
                        imageObserver.unobserve(img);
                    }
                });
            });
            
            lazyImages.forEach(img => imageObserver.observe(img));
        });
    </script>
</body>
</html>
