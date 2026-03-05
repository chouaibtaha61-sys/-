<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>لوحة المفاتيح متاحة للجميع | Developer Tool</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Courier New', monospace;
        }

        body {
            background: #1e1e1e;
            padding: 20px;
            direction: rtl;
            color: #d4d4d4;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
        }

        /* Header */
        .header {
            background: #252526;
            padding: 15px 20px;
            border-radius: 8px;
            margin-bottom: 20px;
            border: 1px solid #3c3c3c;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .header h1 {
            color: #569cd6;
            font-size: 1.3rem;
        }

        .header .badge {
            background: #0e639c;
            color: white;
            padding: 5px 15px;
            border-radius: 4px;
            font-size: 0.8rem;
        }

        /* Text Area */
        .text-area {
            width: 100%;
            min-height: 200px;
            padding: 15px;
            border: 1px solid #3c3c3c;
            border-radius: 8px;
            font-size: 16px;
            font-family: 'Courier New', monospace;
            resize: vertical;
            background: #1e1e1e;
            color: #d4d4d4;
            margin-bottom: 20px;
            line-height: 1.5;
        }

        .text-area:focus {
            outline: none;
            border-color: #0e639c;
            box-shadow: 0 0 10px rgba(14, 99, 156, 0.3);
        }

        .text-area::placeholder {
            color: #6a9955;
        }

        /* Status Bar */
        .status-bar {
            background: #007acc;
            color: white;
            padding: 8px 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            display: flex;
            justify-content: space-between;
            font-size: 0.9rem;
        }

        /* Keyboard */
        .keyboard {
            background: #252526;
            padding: 20px;
            border-radius: 8px;
            border: 1px solid #3c3c3c;
        }

        .keyboard h2 {
            color: #4ec9b0;
            margin-bottom: 15px;
            text-align: center;
            font-size: 1.1rem;
        }

        .keyboard-row {
            display: flex;
            justify-content: center;
            gap: 5px;
            margin-bottom: 8px;
            flex-wrap: wrap;
        }

        .key {
            width: 45px;
            height: 45px;
            background: #3c3c3c;
            border: 1px solid #555;
            border-radius: 4px;
            color: #d4d4d4;
            font-size: 18px;
            cursor: pointer;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            user-select: none;
            font-weight: bold;
        }

        .key:hover {
            background: #4a4a4a;
            border-color: #0e639c;
        }

        .key:active {
            transform: scale(0.95);
            background: #0e639c;
        }

        .key.space {
            width: 350px;
        }

        .key.backspace {
            width: 80px;
        }

        /* Footer */
        .footer {
            margin-top: 20px;
            text-align: center;
            color: #6a9955;
            font-size: 0.8rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .key {
                width: 35px;
                height: 40px;
                font-size: 14px;
            }

            .key.space {
                width: 200px;
            }

            .key.backspace {
                width: 60px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>🔧 لوحة المفاتيح العربية</h1>
            <span class="badge">v1.0.0</span>
        </div>

        <!-- Status Bar -->
        <div class="status-bar">
            <span>📍 Arabic Keyboard Tool</span>
            <span id="charCount">0 characters</span>
        </div>

        <!-- Text Area -->
        <textarea class="text-area" id="outputText" placeholder="// اكتب الكود أو النص هنا..."></textarea>

        <!-- Keyboard -->
        <div class="keyboard">
            <h2>⌨️ Virtual Keyboard</h2>
            <div class="keyboard-row">
                <button class="key" onclick="typeChar('ض')">ض</button>
                <button class="key" onclick="typeChar('ص')">ص</button>
                <button class="key" onclick="typeChar('ث')">ث</button>
                <button class="key" onclick="typeChar('ق')">ق</button>
                <button class="key" onclick="typeChar('ف')">ف</button>
                <button class="key" onclick="typeChar('غ')">غ</button>
                <button class="key" onclick="typeChar('ع')">ع</button>
                <button class="key" onclick="typeChar('ه')">ه</button>
                <button class="key" onclick="typeChar('خ')">خ</button>
                <button class="key" onclick="typeChar('ح')">ح</button>
                <button class="key" onclick="typeChar('ج')">ج</button>
                <button class="key" onclick="typeChar('د')">د</button>
            </div>
            <div class="keyboard-row">
                <button class="key" onclick="typeChar('ش')">ش</button>
                <button class="key" onclick="typeChar('س')">س</button>
                <button class="key" onclick="typeChar('ي')">ي</button>
                <button class="key" onclick="typeChar('ب')">ب</button>
                <button class="key" onclick="typeChar('ل')">ل</button>
                <button class="key" onclick="typeChar('ا')">ا</button>
                <button class="key" onclick="typeChar('ت')">ت</button>
                <button class="key" onclick="typeChar('ن')">ن</button>
                <button class="key" onclick="typeChar('م')">م</button>
                <button class="key" onclick="typeChar('ك')">ك</button>
                <button class="key" onclick="typeChar('ط')">ط</button>
            </div>
            <div class="keyboard-row">
                <button class="key" onclick="typeChar('ئ')">ئ</button>
                <button class="key" onclick="typeChar('ء')">ء</button>
                <button class="key" onclick="typeChar('ؤ')">ؤ</button>
                <button class="key" onclick="typeChar('ر')">ر</button>
                <button class="key" onclick="typeChar('لا')">لا</button>
                <button class="key" onclick="typeChar('ى')">ى</button>
                <button class="key" onclick="typeChar('ة')">ة</button>
                <button class="key" onclick="typeChar('و')">و</button>
                <button class="key" onclick="typeChar('ز')">ز</button>
                <button class="key" onclick="typeChar('ظ')">ظ</button>
            </div>
            <div class="keyboard-row">
                <button class="key" onclick="typeChar('ذ')">ذ</button>
                <button class="key" onclick="typeChar('ء')">ء</button>
                <button class="key" onclick="typeChar('ئ')">ئ</button>
                <button class="key backspace" onclick="backspace()">⌫</button>
            </div>
            <div class="keyboard-row">
                <button class="key space" onclick="typeChar(' ')">Space</button>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            Developer Tool | Arabic Virtual Keyboard | v1.0.0
        </div>
    </div>

    <script>
        function typeChar(char) {
            const textarea = document.getElementById('outputText');
            const start = textarea.selectionStart;
            const end = textarea.selectionEnd;
            const text = textarea.value;
            
            textarea.value = text.substring(0, start) + char + text.substring(end);
            textarea.selectionStart = textarea.selectionEnd = start + char.length;
            textarea.focus();
            updateCharCount();
        }

        function backspace() {
            const textarea = document.getElementById('outputText');
            const start = textarea.selectionStart;
            const end = textarea.selectionEnd;
            const text = textarea.value;
            
            if (start > 0) {
                textarea.value = text.substring(0, start - 1) + text.substring(end);
                textarea.selectionStart = textarea.selectionEnd = start - 1;
            }
            textarea.focus();
            updateCharCount();
        }

        function updateCharCount() {
            const text = document.getElementById('outputText').value;
            document.getElementById('charCount').textContent = `${text.length} characters`;
        }

        // Auto-update character count
        document.getElementById('outputText').addEventListener('input', () => {
            updateCharCount();
        });
    </script>
</body>
</html>
