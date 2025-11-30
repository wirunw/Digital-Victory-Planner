# Digital Victory Planner - Pharm Connection Workshop

แอปพลิเคชันสำหรับนักศึกษาเภสัชศาสตร์ในการวางแผนการตลาดดิจิทัล พร้อม AI Assistant ที่ใช้ Typhoon Model

## 🚀 ฟีเจอร์หลัก

- **5-Step Workshop Process**: กระบวนการคิดแบบมีโครงสร้างสำหรับวางแผนการตลาด
- **AI Assistant**: Digital Victory Mentor ที่ช่วยให้คำแนะนำตามแต่ละขั้นตอน
- **B2C/B2B Tracks**: รองรับทั้ง Consumer และ Healthcare Professional
- **Compliance Integration**: แจ้งเตือนกฎระเบียบที่เกี่ยวข้อง
- **Export Functions**: บันทึกเป็น PDF และ TXT
- **Responsive Design**: ใช้งานได้บนทุกอุปกรณ์

## 🛠️ การติดตั้งและ Deploy

### 1. Clone Repository
```bash
git clone <repository-url>
cd DMKT2025
```

### 2. Install Dependencies
```bash
npm install
```

### 3. ตั้งค่า Environment Variables บน Netlify

ไปที่ Netlify Dashboard → Site Settings → Environment Variables และเพิ่ม:

```
TYPHOON_API_KEY=your_typhoon_api_key_here
TYPHOON_BASE_URL=https://api.opentyphoon.ai/v1
```

**หมายเหตุ**: ให้ใส่ Typhoon API Key ที่คุณมีอยู่ใน `TYPHOON_API_KEY`

### 4. Deploy ไปยัง Netlify

#### วิธีที่ 1: ผ่าน Netlify CLI
```bash
npm install -g netlify-cli
netlify login
netlify deploy --prod
```

#### วิธีที่ 2: ผ่าน Git
1. Push code ไปที่ GitHub/GitLab/Bitbucket
2. Connect repository กับ Netlify
3. Set environment variables ตามข้อ 3
4. Deploy อัตโนมัติ

## 📁 โครงสร้างไฟล์

```
DMKT2025/
├── index.html                 # Main application file
├── netlify/
│   └── functions/
│       └── ai-chat.js       # AI Chat backend
├── netlify.toml             # Netlify configuration
├── package.json             # Dependencies
├── README.md               # This file
├── detail.txt              # Project details
└── prompt.txt              # AI prompt examples
```

## 🤖 Enhanced AI Assistant Features

### Context-Aware Intelligence
- **Step-Specific Guidance**: AI adapts its advice based on current workshop step
- **Track Recognition**: Differentiates between B2C (Consumer) and B2B (HCP) strategies
- **Form Integration**: Can directly fill form fields with AI suggestions
- **Real-time Context**: Sees all form data and provides relevant recommendations

### Smart Suggestions System
- **Structured Format**: Uses `💡 **[Field Name]**: [Suggestion]` format
- **Accept/Reject**: One-click acceptance of AI recommendations
- **Field Mapping**: Automatically maps suggestions to correct form fields
- **Visual Feedback**: Shows accepted suggestions with checkmarks

### Workshop Step Support
- **Step 1**: แนะนำชื่อสินค้าและการเลือก Track
- **Step 2**: ช่วยกำหนด Persona และ Pain Points  
- **Step 3**: หา Sweet Spot Message ที่ balance
- **Step 4**: แนะนำ Funnel Activities
- **Step 5**: ตรวจสอบและปรับปรุงแผน

### Technical Features
- **CORS Support**: Full cross-origin request handling
- **Error Handling**: Graceful fallbacks for API failures
- **Context Memory**: Maintains conversation history
- **Responsive UI**: Works on all device sizes

## 🎯 การใช้งาน

1. **เริ่มต้น**: เลือก "Blueprint" เพื่อดู workflow หรือ "Workshop App" เพื่อเริ่มทำงาน
2. **Step 1**: กรอกชื่อทีมและเลือกประเภทสินค้า (B2C/B2B)
3. **Step 2**: กำหนด Persona และความต้องการ
4. **Step 3**: หาข้อความที่ balance ระหว่าง brand และ audience
5. **Step 4**: วางแผน Funnel และกิจกรรม
6. **Step 5**: ตรวจสอบและส่งออกแผน

## 🧪 การทดสอบ AI Integration

### Test File
มีไฟล์ `test-ai-integration.html` สำหรับทดสอบการทำงานของ AI:

1. **Context Awareness Test**: ทดสอบว่า AI เข้าใจ step ปัจจุบัน
2. **Suggestion Parsing**: ทดสอบการแปลคำแนะนำเป็น structured format
3. **Field Mapping**: ทดสอบการ map suggestions ไปยัง form fields
4. **Error Handling**: ทดสอบกรณีที่เกิดข้อผิดพลาด

### Test Checklist
- [ ] AI responds with context-aware suggestions
- [ ] Suggestions include field names and recommendations  
- [ ] Accept/Reject buttons work properly
- [ ] Form fields update when accepting suggestions
- [ ] Error handling works correctly
- [ ] CORS headers are properly configured

## 🔧 การพัฒนาภายใน

```bash
# รัน local development server
npm run dev

# หรือใช้ Python server
npm run serve

# ทดสอบ AI integration
# เปิด test-ai-integration.html ใน browser
```

## 📝 ข้อมูลอ้างอิง

- **Typhoon Model**: ใช้ `typhoon-v2.5-30b-a3b-instruct`
- **Temperature**: 0.85 (สร้างสรรค์แต่ยังโฟกัส)
- **Max Tokens**: 6003 (เพียงพอสำหรับคำตอบสั้นๆ)
- **Top P**: 0.95 (ความหลากหลายในการตอบ)

## 🛡️ ความปลอดภัย

- API Key ถูกเก็บไว้ใน Environment Variables
- CORS ถูกตั้งค่าให้ปลอดภัย
- Input validation ในทุก endpoint
- Security headers ใน netlify.toml

## 📞 ติดต่อ

Developed by **Wirun Wetsiri**
- Email: [your-email@example.com]
- GitHub: [your-github-username]

## 📄 License

MIT License
