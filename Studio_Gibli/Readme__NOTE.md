1. terminal(mac) >> npx create-remix@latest

2. terminal(VS) >> npm install -D concurrently tailwindcss

3. make a file >> tailwind.config.js
   /_
   module.exports = {
   content: ["./app/\*\*/_.{ts,tsx"], // where can find class, css property
   theme: {
   extend: {},
   },
   variants: {},
   plugins: [],
   };
   \*/

4. package.json file 수정 >> scrip update
   script 객체 내에
   "build:css" : "tailwindcss -o ./app/tailwind.css", 속성 추가
   "dec:css": "tailwindcss -o ./app/tailwind.css --watch", 속성 추가
   "build" 항목 수정 : "npm run build:css && remix build",
   "dev" 항목 수정 : "concurrently \"npm run dev:css\" \"remix dev\"",

5. npm run dev (디렉토리 확인 잘하자)

6. the "meta" export >> set meta tags for html document

7. 구조, 문법이 조금 다른 듯 ? 어떻게 다른 거지 ?
