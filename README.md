# Free Agile Light Plugin

## Instalação

Siga os passos abaixo para instalar o plugin no Redmine:

1. Acesse o diretório de plugins do seu Redmine:
   ```sh
   cd {RAILS_APP}/plugins
   ```
2. Clone o repositório do plugin:
   ```sh
   git clone https://github.com/igorscaglia/redmine_agile.git redmine_agile
   ```
3. Volte para o diretório principal do Redmine:
   ```sh
   cd {RAILS_APP}
   ```
4. Instale as dependências necessárias:
   ```sh
   bundle install --without development test RAILS_ENV=production
   ```
5. Execute a migração do plugin:
   ```sh
   bundle exec rake redmine:plugins:migrate NAME=redmine_agile RAILS_ENV=production
   ```
   Ou (Preferível):
   ```sh
   bundle exec rake redmine:plugins:migrate RAILS_ENV=production
   ```
7. Reinicie o Redmine para aplicar as alterações:
   ```sh
   touch tmp/restart.txt
   ```

## Desinstalação

Para remover o plugin, siga os passos abaixo:

1. Execute o comando para remover a migração do plugin:
   ```sh
   bundle exec rake redmine:plugins NAME=redmine_agile VERSION=0 RAILS_ENV=production
   ```
2. Remova o diretório do plugin:
   ```sh
   rm -r plugins/redmine_agile
   ```
3. Reinicie o Redmine para aplicar as alterações:
   ```sh
   touch tmp/restart.txt
   ```

Pronto! O plugin foi instalado ou removido conforme necessário.

