# Stage 1: Base build (if Node is needed)
FROM node:18 AS builder
WORKDIR /app
COPY . .
# RUN npm install && npm run build  # if you have frontend build
# For now, we just copy static HTML

# Stage 2: Serve with Nginx
FROM nginx:alpine
COPY --from=builder /app /usr/share/nginx/html
