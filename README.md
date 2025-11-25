body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f2f5; /* لون خلفية خفيف */
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    direction: rtl; /* لضمان دعم اللغة العربية */
}

#app-container {
    display: flex;
    width: 90%;
    max-width: 1200px;
    height: 85vh;
    background-color: #ffffff;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    overflow: hidden;
}

/* 1. قائمة المجموعات الجانبية */
#sidebar {
    width: 300px;
    background-color: #f7f9fa;
    border-left: 1px solid #e0e0e0;
    padding: 20px;
    display: flex;
    flex-direction: column;
}

#sidebar h2 {
    color: #1e88e5;
    margin-top: 0;
    padding-bottom: 10px;
    border-bottom: 2px solid #1e88e5;
}

.group-item {
    padding: 15px;
    border-radius: 8px;
    margin-bottom: 10px;
    cursor: pointer;
    transition: background-color 0.3s;
    border: 1px solid #eee;
}

.group-item:hover, .group-item.active {
    background-color: #e3f2fd;
}

.group-item h3 {
    margin: 0 0 5px 0;
    font-size: 16px;
    color: #333;
}

.group-item p {
    margin: 0;
    font-size: 12px;
    color: #666;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}

.new-group-btn {
    margin-top: auto; /* يدفع الزر إلى الأسفل */
    padding: 10px;
    background-color: #4caf50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s;
}

.new-group-btn:hover {
    background-color: #43a047;
}

/* 2. نافذة الدردشة الرئيسية */
#chat-window {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    position: relative;
}

#chat-window header {
    padding: 15px;
    background-color: #1e88e5;
    color: white;
    border-bottom: 1px solid #ccc;
}

#chat-window header h1 {
    margin: 0;
    font-size: 20px;
}

#chat-window header .member-count {
    font-size: 12px;
    opacity: 0.8;
}

#messages-area {
    flex-grow: 1;
    padding: 20px;
    overflow-y: auto;
    background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20"><rect width="10" height="10" fill="%23e5e5e5"/><rect x="10" y="10" width="10" height="10" fill="%23e5e5e5"/><rect x="0" y="10" width="10" height="10" fill="%23f5f5f5"/><rect x="10" y="0" width="10" height="10" fill="%23f5f5f5"/></svg>');
    background-size: 40px 40px;
}

/* تصميم فقاعات الرسائل */
.message {
    display: flex;
    flex-direction: column;
    margin-bottom: 15px;
    max-width: 70%;
}

.message p {
    margin: 5px 0 0 0;
    padding: 10px 15px;
    border-radius: 18px;
    line-height: 1.4;
    word-wrap: break-word;
    box-shadow: 0 1px 1px rgba(0, 0, 0, 0.08);
}

.message .sender-name {
    font-size: 12px;
    margin-bottom: 3px;
    color: #555;
    font-weight: bold;
}

/* رسائل المستخدم (المنبثقة) */
.message.outgoing {
    align-self: flex-start;
}

.message.outgoing p {
    background-color: #dcf8c6; /* لون واتساب الأخضر */
    color: #000;
    border-top-left-radius: 2px;
}

/* رسائل الذكاء الاصطناعي (الواردة) */
.message.incoming {
    align-self: flex-end;
}

.message.incoming p {
    background-color: #fff;
    color: #000;
    border-top-right-radius: 2px;
}

/* تخصيص ألوان لأسماء شخصيات AI */
.ai-dad .sender-name { color: #8bc34a; } /* لون مختلف للأب */
.ai-mom .sender-name { color: #ff9800; } /* لون مختلف للأم */


/* منطقة الإدخال */
#input-area {
    display: flex;
    padding: 10px 20px;
    background-color: #f0f0f0;
    border-top: 1px solid #e0e0e0;
}

#input-area input {
    flex-grow: 1;
    padding: 10px 15px;
    border-radius: 20px;
    border: 1px solid #ccc;
    margin-left: 10px;
    font-size: 16px;
}

#input-area button {
    padding: 10px 15px;
    border: none;
    border-radius: 20px;
    background-color: #25d366; /* لون أخضر واتساب */
    color: white;
    cursor: pointer;
    transition: background-color 0.3s;
}

#input-area button:hover {
    background-color: #128c7e;
}
