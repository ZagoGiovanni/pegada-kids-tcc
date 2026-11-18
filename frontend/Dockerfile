
FROM node:22-bookworm-slim

WORKDIR /app

COPY package*.json ./
RUN npm install --no-audit --no-fund

COPY . .

ARG NEXT_PUBLIC_API_URL
ENV NEXT_PUBLIC_API_URL=$NEXT_PUBLIC_API_URL

ARG NEXT_PUBLIC_TCC_DEMO_MODE=false
ENV NEXT_PUBLIC_TCC_DEMO_MODE=$NEXT_PUBLIC_TCC_DEMO_MODE

RUN npm run build

EXPOSE 3000

CMD ["npm", "run", "start"]
