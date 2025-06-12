# talentghn-profile<!DOCTYPE html>
<html lang="vi" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bản Lĩnh Lãnh Đạo - Khám Phá Năng Lực Cốt Lõi Cùng GHN</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8f9fa;
        }
        .hero-bg {
            background-color: #1a1a1a;
            background-image: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1556761175-5973dc0f32e7?q=80&w=2832&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
        }
        .section-title {
            position: relative;
            padding-bottom: 15px;
            margin-bottom: 20px;
        }
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: #f97316;
            border-radius: 2px;
        }
        .competency-card {
            transition: all 0.3s ease-in-out;
        }
        .competency-card:hover {
            transform: translateY(-10px) scale(1.03);
            box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
        }
        .accordion-item-header {
            cursor: pointer;
        }
        .accordion-item-body {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease-out, padding 0.5s ease;
            padding-top: 0;
            padding-bottom: 0;
        }
        .accordion-item.active .accordion-item-body {
            max-height: 500px; /* Adjust as needed */
            padding-top: 1rem;
            padding-bottom: 1.5rem;
        }
        .accordion-item.active .accordion-icon {
            transform: rotate(180deg);
        }
        .accordion-icon {
            transition: transform 0.3s ease;
        }
        .fade-in-up {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .fade-in-up.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body class="text-gray-800 antialiased">

    <!-- Header -->
    <header id="header" class="bg-white shadow-md sticky top-0 z-50 transition-all duration-300">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <div class="flex-shrink-0">
                    <a href="#" class="flex items-center space-x-2">
                         <span class="text-3xl font-extrabold text-gray-900">GHN</span>
                         <span class="text-3xl font-light text-orange-500">Bản Lĩnh Lãnh Đạo</span>
                    </a>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <a href="#introduction" class="text-gray-600 hover:text-orange-500 px-3 py-2 rounded-md text-sm font-semibold">Giới Thiệu</a>
                        <a href="#competencies" class="text-gray-600 hover:text-orange-500 px-3 py-2 rounded-md text-sm font-semibold">5 Năng Lực</a>
                        <a href="#analysis" class="text-gray-600 hover:text-orange-500 px-3 py-2 rounded-md text-sm font-semibold">Phân Tích Sâu</a>
                        <a href="#action-plan" class="text-gray-600 hover:text-orange-500 px-3 py-2 rounded-md text-sm font-semibold">Kế Hoạch Hành Động</a>
                    </div>
                </div>
                 <div class="md:hidden">
                    <button id="mobile-menu-button" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-white hover:bg-orange-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-800 focus:ring-white">
                        <span class="sr-only">Open main menu</span>
                        <svg class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
                        </svg>
                    </button>
                </div>
            </div>
        </nav>
        <div id="mobile-menu" class="md:hidden hidden">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="#introduction" class="text-gray-600 hover:text-orange-500 block px-3 py-2 rounded-md text-base font-medium">Giới Thiệu</a>
                <a href="#competencies" class="text-gray-600 hover:text-orange-500 block px-3 py-2 rounded-md text-base font-medium">5 Năng Lực</a>
                <a href="#analysis" class="text-gray-600 hover:text-orange-500 block px-3 py-2 rounded-md text-base font-medium">Phân Tích Sâu</a>
                <a href="#action-plan" class="text-gray-600 hover:text-orange-500 block px-3 py-2 rounded-md text-base font-medium">Kế Hoạch Hành Động</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <main>
        <section class="hero-bg text-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-32 md:py-48 text-center">
                <h1 class="text-4xl md:text-6xl font-extrabold tracking-tight leading-tight mb-4 animate-fade-in-down">
                    HỒ SƠ NĂNG LỰC LÃNH ĐẠO GHN
                </h1>
                <p class="max-w-3xl mx-auto text-lg md:text-xl text-gray-200 mb-8 animate-fade-in-up">
                    Kim chỉ nam giúp bạn khám phá, thấu hiểu và phát huy tối đa tiềm năng lãnh đạo của mình trong hành trình chinh phục những tầm cao mới cùng Giao Hàng Nhanh.
                </p>
                <a href="#introduction" class="inline-block bg-orange-500 text-white font-bold text-lg px-8 py-4 rounded-full shadow-lg hover:bg-orange-600 transition duration-300 transform hover:scale-105 animate-bounce">
                    Khám Phá Ngay
                </a>
            </div>
        </section>

        <!-- Introduction Section -->
        <section id="introduction" class="py-20 md:py-28">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center">
                    <h2 class="section-title text-3xl md:text-4xl font-extrabold tracking-tight fade-in-up">Chào Mừng Nhà Lãnh Đạo Tương Lai</h2>
                    <p class="mt-4 max-w-4xl mx-auto text-lg text-gray-600 leading-relaxed fade-in-up">
                        Báo cáo này được thiết kế nhằm mục tiêu làm rõ vai trò và củng cố hiệu quả lãnh đạo của bạn. Hãy sử dụng nó để hiểu sâu hơn về những gì bạn làm tốt nhất một cách tự nhiên, sau đó triển khai các kế hoạch hành động vào trách nhiệm công việc của bạn - bắt đầu ngay hôm nay.
                    </p>
                </div>
            </div>
        </section>

        <!-- Competencies Section -->
        <section id="competencies" class="bg-white py-20 md:py-28">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="section-title text-3xl md:text-4xl font-extrabold tracking-tight fade-in-up">5 Năng Lực Lãnh Đạo Cốt Lõi</h2>
                    <p class="mt-4 max-w-3xl mx-auto text-lg text-gray-600 leading-relaxed fade-in-up">
                        Nền tảng để xây dựng nên một nhà lãnh đạo toàn diện, bản lĩnh và hiệu quả tại GHN.
                    </p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-8">
                    <!-- Card 1 -->
                    <div class="competency-card bg-gray-50 p-6 rounded-xl shadow-lg text-center fade-in-up">
                        <div class="text-5xl mb-4">🎯</div>
                        <h3 class="text-xl font-bold mb-2">Tư duy Chiến lược & Nhạy bén Kinh doanh</h3>
                        <p class="text-gray-600 text-sm">Xây dựng tầm nhìn và chiến lược dựa trên sự thấu hiểu sâu sắc về thị trường và dữ liệu.</p>
                    </div>
                    <!-- Card 2 -->
                    <div class="competency-card bg-gray-50 p-6 rounded-xl shadow-lg text-center fade-in-up" style="transition-delay: 0.1s;">
                         <div class="text-5xl mb-4">🚀</div>
                        <h3 class="text-xl font-bold mb-2">Quản trị Thực thi & Hướng tới Kết quả</h3>
                        <p class="text-gray-600 text-sm">Biến chiến lược thành hành động quyết liệt và luôn đặt kết quả cuối cùng làm trọng tâm.</p>
                    </div>
                    <!-- Card 3 -->
                    <div class="competency-card bg-gray-50 p-6 rounded-xl shadow-lg text-center fade-in-up" style="transition-delay: 0.2s;">
                        <div class="text-5xl mb-4">📊</div>
                        <h3 class="text-xl font-bold mb-2">Phân tích & Ra quyết định dựa trên Dữ liệu</h3>
                        <p class="text-gray-600 text-sm">Sử dụng tư duy logic và bằng chứng số liệu để đưa ra các quyết định nhanh chóng, dứt khoát.</p>
                    </div>
                    <!-- Card 4 -->
                    <div class="competency-card bg-gray-50 p-6 rounded-xl shadow-lg text-center fade-in-up" style="transition-delay: 0.3s;">
                        <div class="text-5xl mb-4">👥</div>
                        <h3 class="text-xl font-bold mb-2">Dẫn dắt & Tạo ảnh hưởng</h3>
                        <p class="text-gray-600 text-sm">Quy tụ, truyền cảm hứng và phát triển đội ngũ để cùng nhau đạt được mục tiêu chung.</p>
                    </div>
                    <!-- Card 5 -->
                    <div class="competency-card bg-gray-50 p-6 rounded-xl shadow-lg text-center fade-in-up" style="transition-delay: 0.4s;">
                        <div class="text-5xl mb-4">🛡️</div>
                        <h3 class="text-xl font-bold mb-2">Bản lĩnh, Kiên cường & Đổi mới</h3>
                        <p class="text-gray-600 text-sm">Kiên trì vượt qua áp lực, linh hoạt thích ứng và không ngừng tìm tòi các giải pháp sáng tạo.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Analysis Section -->
        <section id="analysis" class="py-20 md:py-28">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                 <div class="text-center mb-16">
                    <h2 class="section-title text-3xl md:text-4xl font-extrabold tracking-tight fade-in-up">Hồ Sơ Năng Lực Của Bạn</h2>
                     <p class="mt-4 max-w-3xl mx-auto text-lg text-gray-600 leading-relaxed fade-in-up">
                        Biểu đồ dưới đây trực quan hóa mức độ thể hiện của bạn qua 5 năng lực cốt lõi, giúp bạn có cái nhìn tổng quan về các điểm mạnh và lĩnh vực cần phát triển.
                    </p>
                </div>
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="fade-in-up">
                        <h3 class="text-2xl font-bold mb-4">Đầu tư vào phát triển năng lực</h3>
                        <p class="text-gray-600 leading-relaxed mb-4">
                            Lãnh đạo là một hành trình không ngừng học hỏi. Đó là trách nhiệm của bạn trong việc truyền đạt tầm nhìn, xây dựng văn hóa tích cực và trở thành phiên bản nhà lãnh đạo mạnh mẽ nhất. Trước khi dẫn dắt người khác, bạn phải biết cách dẫn dắt chính mình - và nơi tốt nhất để bắt đầu chính là từ những năng lực cốt lõi.
                        </p>
                        <p class="text-gray-600 leading-relaxed">
                            Báo cáo này sẽ phân tích sâu từng năng lực, giúp bạn khám phá:
                        </p>
                         <ul class="mt-4 space-y-2 text-gray-600">
                            <li class="flex items-start">
                                <span class="text-green-500 mr-2 mt-1">✔</span>
                                <span><strong>Đóng góp cho thành công:</strong> Cách năng lực này giúp bạn tỏa sáng trong vai trò của mình.</span>
                            </li>
                            <li class="flex items-start">
                                <span class="text-yellow-500 mr-2 mt-1">⚠️</span>
                                <span><strong>'Điểm mù' tiềm ẩn:</strong> Những thách thức có thể xảy ra khi một điểm mạnh được sử dụng quá mức hoặc không đúng ngữ cảnh.</span>
                            </li>
                             <li class="flex items-start">
                                <span class="text-blue-500 mr-2 mt-1">🎯</span>
                                <span><strong>Kế hoạch hành động:</strong> Những gợi ý cụ thể bạn có thể áp dụng ngay để phát triển và bứt phá.</span>
                            </li>
                        </ul>
                    </div>
                    <div class="chart-container fade-in-up" style="transition-delay: 0.2s;">
                        <canvas id="competencyRadarChart"></canvas>
                    </div>
                </div>
            </div>
        </section>

        <!-- Action Plan / Deep Dive Section -->
        <section id="action-plan" class="bg-white py-20 md:py-28">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="section-title text-3xl md:text-4xl font-extrabold tracking-tight fade-in-up">Phân Tích Sâu & Kế Hoạch Hành Động</h2>
                    <p class="mt-4 max-w-3xl mx-auto text-lg text-gray-600 leading-relaxed fade-in-up">
                        Nhấn vào từng năng lực để khám phá phân tích chi tiết về điểm mạnh, điểm mù tiềm ẩn và các gợi ý hành động để bạn có thể phát triển toàn diện.
                    </p>
                </div>
                <div id="accordion-container" class="space-y-4 fade-in-up">
                   <!-- Accordion items will be generated by JS -->
                </div>
            </div>
        </section>

    </main>
    
    <!-- Footer -->
    <footer class="bg-gray-900 text-white">
        <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-2xl font-bold">GIAO HÀNG NHANH</p>
            <p class="mt-2 text-gray-400">Chương trình Phát triển Tài năng Lãnh đạo "Bản Lĩnh Lãnh Đạo"</p>
            <p class="mt-4 text-sm text-gray-500">&copy; 2025 Giao Hàng Nhanh. All rights reserved.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            // Mobile menu toggle
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });

            // Radar Chart
            const ctx = document.getElementById('competencyRadarChart').getContext('2d');
            const competencyChart = new Chart(ctx, {
                type: 'radar',
                data: {
                    labels: [
                        'Tư duy Chiến lược', 
                        'Quản trị Thực thi', 
                        'Phân tích & Ra quyết định', 
                        'Dẫn dắt & Tạo ảnh hưởng', 
                        'Bản lĩnh & Đổi mới'
                    ],
                    datasets: [{
                        label: 'Kết quả đánh giá',
                        data: [4, 5, 3, 4, 3], // Sample data
                        backgroundColor: 'rgba(249, 115, 22, 0.2)',
                        borderColor: 'rgba(249, 115, 22, 1)',
                        pointBackgroundColor: 'rgba(249, 115, 22, 1)',
                        pointBorderColor: '#fff',
                        pointHoverBackgroundColor: '#fff',
                        pointHoverBorderColor: 'rgba(249, 115, 22, 1)',
                        borderWidth: 2
                    }]
                },
                options: {
                    scales: {
                        r: {
                            angleLines: { color: 'rgba(0, 0, 0, 0.1)' },
                            grid: { color: 'rgba(0, 0, 0, 0.1)' },
                            pointLabels: { 
                                font: { size: 12, weight: 'bold' },
                                color: '#333'
                            },
                            ticks: {
                                beginAtZero: true,
                                max: 5,
                                stepSize: 1,
                                backdropColor: 'rgba(255, 255, 255, 0.75)'
                            }
                        }
                    },
                    plugins: {
                        legend: {
                            display: false
                        }
                    },
                     maintainAspectRatio: false
                }
            });

            // Accordion Data
            const accordionData = [
                {
                    title: "1. Tư duy Chiến lược & Nhạy bén Kinh doanh",
                    success: "Nhờ có tư duy chiến lược, bạn không bị sa đà vào các vấn đề vận hành vụn vặt. Bạn có khả năng nhìn xa hơn, dự đoán được các xu hướng của thị trường và hành động của đối thủ, từ đó giúp đội ngũ của bạn luôn đi trước một bước. Bạn giỏi trong việc biến các mục tiêu lớn của công ty thành những chiến lược khả thi cho vùng của mình.",
                    blindspot: "Đôi khi, việc quá tập trung vào bức tranh toàn cảnh có thể khiến bạn bỏ qua các chi tiết quan trọng trong vận hành hàng ngày. Khi bạn đã tự tin vào một chiến lược, bạn có thể thiếu kiên nhẫn với những ý kiến trái chiều hoặc các phản hồi mang tính chi tiết.",
                    actions: [
                        "<strong>Chia sẻ tầm nhìn:</strong> Chủ động trao đổi với các lãnh đạo khác về nhận định thị trường của bạn.",
                        "<strong>Thúc đẩy tư duy chiến lược cho đội ngũ:</strong> Sử dụng các câu hỏi 'Tại sao?' trong các cuộc họp để liên kết công việc hàng ngày với mục tiêu lớn.",
                        "<strong>Lên kế hoạch cho thành tựu:</strong> Đảm bảo các mục tiêu bạn đặt ra phù hợp với tầm nhìn và sự khác biệt bạn muốn tạo ra.",
                        "<strong>Dành thời gian cho 'Reflection & Planning':</strong> Cuối mỗi tuần, hãy tự vấn về các quyết định và tác động của chúng."
                    ]
                },
                {
                    title: "2. Quản trị Thực thi & Hướng tới Kết quả",
                    success: "Bạn là người hành động. Bạn có khả năng biến những chiến lược phức tạp thành các kế hoạch chi tiết, có thể đo lường và theo đuổi mục tiêu một cách quyết liệt. Đội ngũ của bạn luôn biết rõ họ cần phải làm gì để đạt được thành công.",
                    blindspot: "Trong một số trường hợp, sự tập trung cao độ vào kết quả có thể khiến bạn thiếu linh hoạt khi có những thay đổi bất ngờ xảy ra. Bạn cũng có thể vô tình tạo áp lực lên đội ngũ nếu không cân bằng giữa việc thúc đẩy và ghi nhận.",
                    actions: [
                        "<strong>Xây dựng kế hoạch linh hoạt (Agile Planning):</strong> Chia nhỏ các dự án lớn thành các giai đoạn ngắn (sprints) để dễ dàng điều chỉnh.",
                        "<strong>Ghi nhận quá trình, không chỉ kết quả:</strong> Tổ chức các buổi vinh danh hàng tháng để công nhận cả nỗ lực và thành tích.",
                        "<strong>Phân quyền hiệu quả:</strong> Tin tưởng và giao cho các quản lý cấp dưới quyền tự quyết trong phạm vi của họ để tăng tính chủ động."
                    ]
                },
                {
                    title: "3. Năng lực Phân tích & Ra quyết định dựa trên Dữ liệu",
                    success: "Bạn không quyết định dựa trên cảm tính. Năng lực phân tích sắc bén cho phép bạn 'đọc vị' các bộ dữ liệu, tìm ra quy luật và đưa ra các quyết định có cơ sở vững chắc. Điều này mang lại sự tin tưởng và ổn định cho đội ngũ.",
                    blindspot: "Việc quá phụ thuộc vào dữ liệu có thể làm chậm quá trình ra quyết định trong những tình huống khẩn cấp, nơi thông tin không đầy đủ. Đôi khi, bạn có thể đánh giá thấp các yếu tố con người hoặc trực giác mà dữ liệu không thể hiện hết.",
                     actions: [
                        "<strong>Thực hành '80/20 Rule' cho dữ liệu:</strong> Tập trung vào 20% dữ liệu quan trọng nhất mang lại 80% giá trị thông tin.",
                        "<strong>Kết hợp Dữ liệu và Trực giác:</strong> Sau khi phân tích, hãy tự hỏi: 'Trực giác của mình nói gì về điều này?'.",
                        "<strong>Phát triển kỹ năng kể chuyện bằng dữ liệu (Data Storytelling):</strong> Thay vì chỉ trình bày số liệu, hãy biến chúng thành một câu chuyện có ý nghĩa cho đội ngũ."
                    ]
                },
                {
                    title: "4. Năng lực Dẫn dắt & Tạo ảnh hưởng",
                    success: "Bạn là chất keo kết dính đội ngũ. Bạn giỏi trong việc lắng nghe, thấu hiểu và truyền cảm hứng, giúp mọi người cảm thấy được trân trọng và có động lực. Bạn có khả năng xây dựng các mối quan hệ bền vững và thuyết phục người khác đi theo tầm nhìn chung.",
                    blindspot: "Mong muốn duy trì sự hòa hợp có thể khiến bạn né tránh các cuộc đối thoại khó khăn hoặc quyết định không được lòng mọi người. Đôi khi, bạn có thể dành quá nhiều thời gian để đạt được sự đồng thuận thay vì đưa ra một quyết định nhanh chóng khi cần thiết.",
                     actions: [
                        "<strong>Thực hành 'Radical Candor' (Sự thẳng thắn cấp tiến):</strong> Học cách đưa ra phản hồi mang tính xây dựng nhưng trực diện.",
                        "<strong>Tìm kiếm một người 'phản biện' (Devil's Advocate):</strong> Nhờ một người bạn tin tưởng đóng vai trò phản biện các ý tưởng của bạn.",
                        "<strong>Phát triển người kế cận:</strong> Dành thời gian huấn luyện (coach) và trao quyền cho ít nhất 2 nhân sự tiềm năng trong đội ngũ của bạn."
                    ]
                },
                {
                    title: "5. Bản lĩnh, Kiên cường & Đổi mới",
                    success: "Bạn không ngại khó khăn. Áp lực càng cao, bạn càng thể hiện được sự bình tĩnh và khả năng giải quyết vấn đề. Bạn luôn cởi mở với những ý tưởng mới và không ngừng tìm tòi các giải pháp sáng tạo để cải thiện hiệu quả công việc.",
                    blindspot: "Sự kiên cường có thể đôi khi biến thành cứng đầu, khiến bạn khó từ bỏ một ý tưởng dù nó không còn hiệu quả. Việc luôn tìm kiếm sự đổi mới có thể gây ra sự mệt mỏi cho đội ngũ nếu các thay đổi diễn ra quá thường xuyên mà không có thời gian để ổn định.",
                    actions: [
                        "<strong>Xây dựng 'Văn hóa Thử nghiệm':</strong> Khuyến khích đội ngũ thử nghiệm các ý tưởng nhỏ với rủi ro thấp.",
                        "<strong>Lên lịch cho 'Thời gian suy ngẫm':</strong> Dành 30 phút mỗi tuần để đánh giá lại các dự án đang chạy và tự hỏi: 'Có cách nào tốt hơn không?'.",
                        "<strong>Học cách 'Kill your darlings':</strong> Dũng cảm dừng lại các dự án hoặc ý tưởng không còn mang lại hiệu quả, dù bạn đã đầu tư nhiều công sức."
                    ]
                }
            ];

            const accordionContainer = document.getElementById('accordion-container');
            accordionData.forEach((item, index) => {
                const itemDiv = document.createElement('div');
                itemDiv.className = 'accordion-item bg-gray-50 rounded-lg shadow-sm';
                itemDiv.innerHTML = `
                    <div class="accordion-item-header flex justify-between items-center p-5">
                        <h3 class="text-lg font-semibold text-gray-800">${item.title}</h3>
                        <span class="accordion-icon text-orange-500">
                            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                        </span>
                    </div>
                    <div class="accordion-item-body px-5">
                        <div class="border-t border-gray-200 pt-4">
                            <h4 class="font-bold text-green-600 mb-2">💡 Đóng góp cho thành công của bạn</h4>
                            <p class="text-gray-600 mb-4">${item.success}</p>
                            <h4 class="font-bold text-yellow-600 mb-2">⚠️ 'Điểm mù' tiềm ẩn</h4>
                            <p class="text-gray-600 mb-4">${item.blindspot}</p>
                            <h4 class="font-bold text-blue-600 mb-2">🎯 Kế hoạch hành động để bứt phá</h4>
                            <ul class="space-y-2 text-gray-600 list-disc list-inside">
                                ${item.actions.map(action => `<li>${action}</li>`).join('')}
                            </ul>
                        </div>
                    </div>
                `;
                accordionContainer.appendChild(itemDiv);
            });
            
            // Accordion functionality
            document.querySelectorAll('.accordion-item-header').forEach(header => {
                header.addEventListener('click', () => {
                    const activeItem = document.querySelector('.accordion-item.active');
                    const clickedItem = header.parentElement;

                    if (activeItem && activeItem !== clickedItem) {
                        activeItem.classList.remove('active');
                    }
                    
                    clickedItem.classList.toggle('active');
                });
            });

            // Scroll animations
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                    }
                });
            }, { threshold: 0.1 });

            document.querySelectorAll('.fade-in-up').forEach(el => {
                observer.observe(el);
            });
        });
    </script>

</body>
</html>
