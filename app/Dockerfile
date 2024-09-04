##### -                           OS_IMAGE                         - #####
FROM node:12-alpine
##### -                    DIRETÓRIO DE TRABALHO                   - #####
WORKDIR /app
##### -         LINHA DE COMANDO DURANTE CRIAÇÃO DA IMAGEM         - #####
# RUN addgroup dev && adduser -S -G dev appmanager
##### - INDICA QUAL USUÁRIO IRÁ GERENCIAR A APLICAÇÃO NO CONTAINER - #####
# USER appmanager
##### -              ARQUIVOS NECESSÁRIOS DA APLICAÇÃO             - #####
COPY . .
##### -         LINHA DE COMANDO DURANTE CRIAÇÃO DA IMAGEM         - #####
RUN apk add --no-cache python2 g++ make && \
    yarn install --production 
##### -         EXPOSIÇÃO DE PORTAS PARA ACESSO A APLICAÇÃO         - #####
EXPOSE 3000
##### -       LINHA DE COMANDO DURANTE EXECUÇÃO DO CONTAINER        - #####
CMD [ "node", "src/index.js" ]