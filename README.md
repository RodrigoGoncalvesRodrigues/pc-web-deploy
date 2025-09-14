
## ⚙️ Projeto pc-web-deploy 
Este é um projeto de deploy automatizado desenvolvido para uma aplicação web em PHP, utilizando GitHub Actions para integração e entrega contínua (CI/CD).
O sistema é publicado automaticamente em uma instância EC2 da AWS (Ubuntu Server), garantindo consistência, escalabilidade e agilidade no processo de deploy.
Além disso, o PuTTY foi utilizado para realizar conexões SSH manuais no servidor durante as etapas de configuração inicial.

## 🧩 Estrutura do Projeto

### 📁 Aplicação Web


A aplicação está localizada na pasta `app/`, contendo o código principal desenvolvido em PHP (com suporte a Blade templates e Composer).

### 📁 Workflow GitHub Actions

Na pasta `.github/workflows/` encontram-se os arquivos de configuração de CI/CD.
O workflow realiza as seguintes tarefas:

- Conexão via SSH com a instância EC2.

- Instalação de dependências (`composer install` e `npm install`).

- Deploy automático do código para `/var/www/html`.

- Configuração do Apache como servidor web.

- Automação de builds e atualizações.

## 🌐 Fluxo de Deploy (CI/CD)

🔹 Workflow CI/CD (`.github/workflows/deploy.yml`)


| Etapa            | Descrição                                                             |
| ---------------- | --------------------------------------------------------------------- |
| `Checkout`       | Faz o checkout do repositório no GitHub Actions                       |
| `Setup Node/PHP` | Prepara ambiente com Node.js, PHP e Composer                          |
| `Install Deps`   | Executa `npm install` e `composer install` no servidor remoto via SSH |
| `Deploy`         | Copia os arquivos para `/var/www/html` da instância EC2               |
| `Apache Reload`  | Reinicia o Apache para aplicar as mudanças                            |

## 🚀 Tecnologias do Projeto

- PHP (com Blade templates)

- Composer (gerenciador de dependências PHP)

- Node.js e npm (para assets do frontend)

- Apache (servidor web na instância EC2)

- GitHub Actions (para CI/CD)

- SSH (deploy remoto automatizado)

- AWS EC2 (Ubuntu Server) (ambiente de hospedagem em nuvem)

- PuTTY (cliente SSH utilizado para configuração manual no servidor)

## 🔑 Principais Competências Demonstradas

- Automação de deploy com GitHub Actions

- Deploy de aplicação em instância EC2 na AWS

- Conexão e configuração de servidor remoto com PuTTY (SSH)

- Integração de Composer e npm no fluxo de deploy

- Configuração e gerenciamento de Apache em servidores Linux

- Boas práticas em CI/CD e DevOps
