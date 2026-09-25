## Hướng dẫn sử dụng git
Bước 1: ``git add .`` hoặc `` git add đường dẫn file`` 
Bước 2: `` git commit -m "Nội dung"`` mới commit file
Bước 3: `` git push`` đẩy file lên github

---

## Mã nhúng Chatbox Tuyển sinh (CSS thuần) vào website trường
Sao chép đoạn mã bên dưới và dán vào phần quản trị giao diện (Footer / Khối HTML tĩnh) của website:

```html
<style>
    /* ========================================================
    CHATBOX TUYỂN SINH - CSS THUẦN (100% KHÔNG BỊ XÓA CODE)
    ======================================================== */
    #ts-chat-toggle {
        display: none !important;
    }
    /* NÚT TRÒN CHAT GÓC PHẢI DƯỚI - 60px x 60px VỚI LOGO ROBOT AI */
    #ts-chat-btn {
        position: fixed !important;
        bottom: 20px !important;
        right: 20px !important;
        width: 60px !important;
        height: 60px !important;
        background: #4f46e5 !important;
        color: #ffffff !important;
        border-radius: 50% !important;
        display: flex !important;
        align-items: center !important;
        justify-content: center !important;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.35) !important;
        z-index: 999999 !important;
        cursor: pointer !important;
        transition: transform 0.2s ease, background 0.2s ease !important;
        -webkit-tap-highlight-color: transparent !important;
    }
    #ts-chat-btn:hover {
        transform: scale(1.08) !important;
    }
    /* Logo trong nút tròn */
    #ts-chat-btn .icon-open { 
        display: block !important; 
        width: 44px !important; 
        height: 44px !important; 
        object-fit: contain !important;
    }
    #ts-chat-btn .icon-close { 
        display: none !important; 
        width: 26px !important; 
        height: 26px !important; 
    }
    /* CỬA SỔ CHAT: MẶC ĐỊNH ẨN HOÀN TOÀN */
    #ts-chat-window {
        display: none !important;
        position: fixed !important;
        bottom: 90px !important;
        right: 20px !important;
        width: 380px !important;
        max-width: calc(100vw - 30px) !important;
        height: 540px !important;
        max-height: calc(100vh - 120px) !important;
        z-index: 999999 !important;
        border-radius: 18px !important;
        box-shadow: 0 10px 35px rgba(0, 0, 0, 0.3) !important;
        overflow: hidden !important;
        background: #ffffff !important;
        border: 1px solid #e5e7eb !important;
    }
    /* KHI BẤM NÚT TRÒN: BẬT KHUNG CHAT */
    #ts-chat-toggle:checked ~ #ts-chat-window {
        display: block !important;
    }
    /* Tối ưu toàn màn hình trên điện thoại di động */
    @media (max-width: 480px) {
        #ts-chat-window {
            bottom: 0 !important;
            right: 0 !important;
            width: 100vw !important;
            height: 100% !important;
            max-width: 100vw !important;
            max-height: 100% !important;
            border-radius: 0 !important;
        }
    }
    /* Khi đang mở: Nút tròn chuyển sang màu đỏ có dấu X */
    #ts-chat-toggle:checked ~ #ts-chat-btn {
        background: #ef4444 !important;
    }
    #ts-chat-toggle:checked ~ #ts-chat-btn .icon-open {
        display: none !important;
    }
    #ts-chat-toggle:checked ~ #ts-chat-btn .icon-close {
        display: block !important;
    }
    /* Nút X đóng ở góc trên bên phải thanh tiêu đề */
    #ts-close-header {
        position: absolute !important;
        top: 10px !important;
        right: 12px !important;
        color: #ffffff !important;
        font-size: 20px !important;
        font-weight: bold !important;
        cursor: pointer !important;
        z-index: 1000000 !important;
        width: 32px !important;
        height: 32px !important;
        display: flex !important;
        align-items: center !important;
        justify-content: center !important;
        background: rgba(0, 0, 0, 0.15) !important;
        border-radius: 50% !important;
        line-height: 1 !important;
        text-align: center !important;
    }
</style>

<!-- Checkbox ẩn để điều khiển bật/tắt bằng CSS thuần -->
<input type="checkbox" id="ts-chat-toggle" />

<!-- Nút tròn góc phải dưới màn hình -->
<label for="ts-chat-toggle" id="ts-chat-btn" title="Chatbot AI Tư vấn Tuyển sinh">
    <!-- Biểu tượng Logo Nhà Trường -->
    <img class="icon-open" src="https://chaupholy.github.io/test-git/logo.png" alt="Logo Trường" />
    <!-- Biểu tượng đóng ✕ -->
    <svg class="icon-close" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
    </svg>
</label>

<!-- Cửa sổ Chatbox hiển thị trực tiếp trên website của trường -->
<div id="ts-chat-window">
    <label for="ts-chat-toggle" id="ts-close-header" title="Đóng chat">✕</label>
    <iframe src="https://chaupholy.github.io/test-git/chatbox-tuyensinh.html" style="width: 100%; height: 100%; border: none;" allow="autoplay; microphone; clipboard-write;"></iframe>
</div>
```

<!-- Xác thực kết nối GitHub -->