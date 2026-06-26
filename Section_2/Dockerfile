FROM node

WORKDIR /app
# 1. Copiamos PRIMERO el package.json
COPY package.json /app

# 2. Instalamos dependencias (Si el package.json no cambió, Docker usa la caché y salta este paso en 0.1s)
RUN npm install

# 3. Copiamos el resto de los archivos (server.js, carpetas public, etc.)
COPY . /app

EXPOSE 80

CMD ["node", "server.js"]