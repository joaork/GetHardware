<div align="center">
  <img src="https://raw.githubusercontent.com/joaork/GetHardware/main/logo.png" alt="GetHardware Logo" width="300"/>

  #
  **Sistema de Monitorização de Computadores**

  ![Project Status](https://img.shields.io/badge/status-concluido-brightgreen) ![Project Type](https://img.shields.io/badge/type-freelance-blue)

  [![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
  [![PHP](https://img.shields.io/badge/PHP-8.x-777BB4?style=for-the-badge&logo=php&logoColor=white)](https://www.php.net/)
  [![HTML5 & CSS3](https://img.shields.io/badge/HTML5_&_CSS3-E34F26?style=for-the-badge&logo=html5&logoColor=white)]()
  [![CustomTkinter](https://img.shields.io/badge/CustomTkinter-UI-10b981?style=for-the-badge)]()
  [![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white)]()
</div>

<br>

## 📌 Sobre o Projeto

O **GetHardware** é uma solução completa com o objetivo de transformar o suporte técnico de TI de um modelo *reativo* (esperar que a falha ocorra) para um modelo **proativo**. 

A arquitetura divide-se num **Programa Executável** (instalado nas máquinas dos clientes) que recolhe dados profundos de hardware e um **Painel Web**, onde a equipe pode acompanhar o estado de saúde de todos os computadores em tempo real, prever falhas de componentes (como sobreaquecimento) e agir antecipadamente.

---

## 📸 Demonstração Visual

![1](https://raw.githubusercontent.com/joaork/GetHardware/main/1.png)
![2](https://raw.githubusercontent.com/joaork/GetHardware/main/2.png)
![33](https://raw.githubusercontent.com/joaork/GetHardware/main/33.png)
![4](https://raw.githubusercontent.com/joaork/GetHardware/main/4.png)
![5](https://raw.githubusercontent.com/joaork/GetHardware/main/5.png)
![6](https://raw.githubusercontent.com/joaork/GetHardware/main/6.png)
![Video](https://raw.githubusercontent.com/joaork/GetHardware/main/video.mp4)

---


## 🚀 Funcionalidades Principais

### 🖥️ Programa Executável
- **Recolha Profunda de Dados:** Leitura de sensores via WMI, ACPI e integração com *LibreHardwareMonitorLib* para precisão cirúrgica em temperaturas, tensões e frequências.
- **Serviço Silencioso:** Executa em segundo plano como um Serviço do Windows, sem interromper o utilizador final.
- **Túnel Seguro:** Os dados (TXT) e os ficheiros de histórico são encriptados e enviados para um servidor remoto via protocolo **SFTP (SSH)**.
- **Instalador Premium:** Interface de instalação e desinstalação desenvolvida do zero com **CustomTkinter**, incluindo suporte nativo a *Dark/Light Mode*, animações fluidas a 60fps e design moderno com gradientes.

### 🌐 Painel Web
- **Tempo Real & Histórico:** Visualização instantânea de CPU, RAM e armazenamento, com gráficos interativos de desempenho temporal.
- **Interface Dinâmica:** Cartões de informação arrastáveis (Drag & Drop), adaptáveis às necessidades do técnico.
- **Inventário Detalhado:** Registro de endereços MAC, IPs, motherboards, sistemas de ficheiros e tráfego de rede (RX/TX).

---

## 🏗️ Arquitetura do Sistema

O fluxo de dados do sistema funciona da seguinte forma:

1. O **Executável (`gethardware.exe`)** recolhe a telemetria do SO e da placa-mãe.
2. Formata os dados num ficheiro `TXT` estruturado.
3. O módulo de rede (Paramiko) abre uma ligação segura e envia o ficheiro para o diretório remoto do servidor Linux.
4. O **Servidor Web** descodifica o ficheiro TXT de cada cliente específico mediante a chamada na URL (`?pc=NOME-DO-CLIENTE`).
5. O **Front-end** renderiza as métricas e desenha os componentes visuais e gráficos interativos no ecrã.

---

## 🛠️ Tecnologias Utilizadas

**Back-end & Agente (Desktop):**
* Python 
* `psutil`, `cpuinfo`, `paramiko`
* LibreHardwareMonitor (C#/.NET DLL Wrapper)
* PyInstaller (Compilação e blindagem de executáveis)
* CustomTkinter & PIL (Interface Gráfica)

**Front-end & Servidor:**
* HTML, CSS, JavaScript
* Chart.js (Data Visualization)
* PHP (Processamento de ficheiros remotos)
* Servidor Linux (SFTP)
  
---

## 💼 Aquisição e Licenciamento

O **GetHardware** é um software comercial e não possui código aberto. Ele está disponível para implantação em empresas de T.I. que desejam gerenciar seus clientes, ou empresas que desejam monitorar sua própria rede local.

Para agendar uma demonstração, solicitar orçamentos ou adquirir o sistema completo, entre em contato:

**João V.** Desenvolvedor e Engenheiro de Computação  

📧 Email: [joaovictorscr1@gmail.com]  
💼 LinkedIn: [https://www.linkedin.com/in/jl-profile/](https://linkedin.com)
