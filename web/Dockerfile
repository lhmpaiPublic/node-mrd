# 1. Node.js 공식 이미지 기반 (경량 alpine 사용 권장)
FROM node:20-alpine
# 2. 컨테이너 내 작업 디렉토리 생성
WORKDIR /app
# 3. package.json, package-lock.json 먼저 복사
COPY package*.json ./
# 4. 의존성 설치
RUN npm install --omit=dev
# 5. 나머지 코드 복사
COPY server.js ./
# 6. 서비스 포트 노출
EXPOSE 3000
# 7. 앱 실행 (기본 명령)
CMD ["npm", "start"]