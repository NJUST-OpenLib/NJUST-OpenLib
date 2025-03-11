<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NJUST.WIKI - 南京理工大学开放知识库</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary-blue: #00467F;
            /* 南理工主题蓝 */
            --accent-orange: #FF6B35;
            /* 科技感强调色 */
            --text-dark: #2A3439;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, sans-serif;
        }

        /* 导航栏 */
        .navbar {
            background: var(--primary-blue);
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .logo {
            color: white;
            font-size: 1.8rem;
            font-weight: 700;
            letter-spacing: 1.5px;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            color: rgba(255, 255, 255, 0.9);
            text-decoration: none;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--accent-orange);
        }

        /* 移动端菜单 */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
        }

        /* 主内容区 */
        .hero {
            margin-top: 80px;
            padding: 4rem 5%;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            text-align: center;
        }

        h1 {
            color: var(--primary-blue);
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }

        .description {
            color: var(--text-dark);
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto 2rem;
            line-height: 1.6;
        }

        /* 分类卡片 */
        .card-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            padding: 2rem 5%;
        }

        .card {
            background: white;
            border-radius: 12px;
            padding: 2rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        /* GitHub链接 */
        .github-section {
            text-align: center;
            padding: 2rem;
            background: var(--text-dark);
            color: white;
        }

        .github-link {
            color: var(--accent-orange);
            text-decoration: none;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        /* 响应式设计 */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: var(--primary-blue);
                flex-direction: column;
                padding: 1rem;
            }

            .nav-links.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }
        }

        .placeholder-section {
            max-width: 800px;
            margin: 2rem auto;
            padding: 0 5%;
        }

        .construction-banner {
            background: #fff8e1;
            border-radius: 12px;
            padding: 1.5rem;
            text-align: center;
            margin-bottom: 2rem;
        }

        .progress-bar {
            height: 8px;
            background: #eee;
            border-radius: 4px;
            overflow: hidden;
            margin: 1rem 0;
        }

        .progress-fill {
            height: 100%;
            background: var(--primary-blue);
            transition: width 0.5s ease;
        }

        .callout-card {
            background: white;
            border: 2px dashed var(--primary-blue);
            border-radius: 12px;
            padding: 2rem;
            text-align: center;
        }

        .contribute-options {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .github-button {
            background: #333;
            color: white !important;
            padding: 0.8rem;
            border-radius: 6px;
            transition: 0.3s;
        }

        .project-link {
            color: var(--primary-blue);
            font-weight: bold;
            text-decoration: underline;
        }
    </style>
</head>

<body>
    <header class="navbar">
        <div class="logo">NJUST.WIKI</div>
        <nav class="nav-links">
            <a href="#home">首页</a>
            <a href="#wiki">维基目录</a>
            <a href="#contribute">参与贡献</a>
            <a href="#about">关于我们</a>
        </nav>
        <button class="menu-toggle" onclick="toggleMenu()"><i class="fas fa-bars"></i></button>
    </header>

    <main>
        <section class="hero">
            <h1>南京理工大学知识共享平台</h1>
            <p class="description">
                理工维基是由学生自主维护的开放式知识库，涵盖课程资料、实验指南、科研经验等多元化内容。
                我们致力于构建可持续的学术资源共享生态，目前已收录1篇高质量文档，日均访问量突破1次。
            </p>
            <div class="card-container">
                <div class="card">
                    <h3><i class="fas fa-book-open"></i> 课程百科</h3>
                    <p>覆盖30+专业核心课程知识体系</p>
                </div>
                <div class="card">
                    <h3><i class="fas fa-flask"></i> 实验指南</h3>
                    <p>200+实验室操作规范与设备说明</p>
                </div>
                <div class="card">
                    <h3><i class="fas fa-users"></i> 社区协作</h3>
                    <p>开放编辑权限，共建知识库</p>
                </div>
            </div>




            <section class="placeholder-section">
                <div class="construction-banner">
                    <i class="fas fa-hard-hat construction-icon"></i>
                    <h3>知识库建设中 <span class="progress-badge">完成度 1%</span></h3>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 1%"></div>
                    </div>
                </div>

                <div class="callout-card">
                    <div class="callout-header">
                        <i class="fas fa-hands-helping"></i>
                        <h4>共建计划进行中！</h4>
                    </div>
                    <p class="highlight-text">
                        我们正在集中建设 <a href="https://doc.njust.wiki" class="project-link">课程资料库</a> 项目，
                        目前已收录12个院系、300+门课程资料
                    </p>
                    <div class="contribute-options">
                        <a href="https://github.com/NJUST-OpenLib" class="github-button">
                            <i class="fab fa-github"></i> 查看GitHub项目
                        </a>
                        <div class="contact-info">
                            <i class="fas fa-envelope"></i>
                            合作联系：admin@njust.wiki
                        </div>
                    </div>
                </div>
            </section>
        </section>
    </main>

    <footer class="github-section">
        <h3>加入开源社区</h3>
        <a href="https://github.com/NJUST-OpenLib/NJUST-OpenLib" class="github-link" target="_blank">
            <i class="fab fa-github"></i>
            GitHub仓库
        </a>
    </footer>

    <script>
        // 移动端菜单切换
        function toggleMenu() {
            const navLinks = document.querySelector('.nav-links');
            navLinks.classList.toggle('active');
        }

        // 窗口调整时自动关闭菜单
        window.addEventListener('resize', () => {
            if (window.innerWidth > 768) {
                document.querySelector('.nav-links').classList.remove('active');
            }
        });
    </script>
</body>

</html>
