# Use uma imagem base do Python
FROM python:3.8-slim

# Configuração de variáveis de ambiente (opcional)
ENV APP_HOME /app
ENV FLASK_APP app.py
ENV FLASK_RUN_HOST 0.0.0.0
ENV FLASK_RUN_PORT 5000

# Crie e defina o diretório de trabalho
WORKDIR $APP_HOME

# Copie os arquivos de código-fonte da aplicação para o contêiner
COPY . .

# Instale as dependências da aplicação
RUN pip install --no-cache-dir -r requirements.txt

# Expõe a porta em que a aplicação será executada
EXPOSE $FLASK_RUN_PORT

# Comando para iniciar a aplicação
CMD ["flask", "run"]
