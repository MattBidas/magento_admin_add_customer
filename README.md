# Magento2 2.1.5 Backend Admin Add New Customer Invalid Date
Magento2 2.1.5 Solves Add New Customer in Admin/Backend
> This file is a override to solve problem to Add New Customer from Admin/Backend


## Sobre
Ao tentar adicionar um novo Cliente através do Painel de Administração do Magento (Admin/Backend) ocorre um erro de Invalid Date.
O objetivo desta feature é que o arquivo date.js sobrescreva o arquivo do CORE , para formatar a data do Calendário(datapicker.js)
para o padrão dia-Mês-Ano (dd/MM/YYYY) utilizado no idioma pt_BR.

## O que preciso

- Magento2 2.1.5
- PHP5 5.6 ou PHP7 >=
- Apache2.2 >=
- Baixar ou clonar este projeto para obter o arquivo.

## Instalação

Após obter o arquivo, você necessita copiar para seu projeto Magento2 para a pasta:
Criar o caminho caso não existir.
> <Magento2>/app/design/frontend/<Your_Vendor_Name><Theme_Name>/Magento_Ui/web/js/form/element/

### Requisitos para utilização 

Após copiar o o arquivo para o caminho do Módulo é preciso executar os comandos:
Certifique-se que está na raiz do seu projeto Magento2, exemplo: /var/www/html/

> Limpar o diretório dos arquivos usado pelos módulos e injeções de dependência
```
sudo rm -rf pub/static/adminhtml/*
```

> Criar os arquivos estáticos para o Backend
```
php bin/magento setup:static-content:deploy pt_BR --area=adminhtml
```
> Se o seu Magento2 Cache está habilitado , limpe através do comando :
```
php bin/magento cache:clean
```
# Problemas comuns

> Caso ainda não tenho o resultado esperado , gere novamente toda a compilação (Frontend e Backend)
```
php bin/magento setup:static-content:deploy pt_BR
```



### Duvidas, problemas, sugestões

* Abra uma Issue com seu questionamento/dúvida


