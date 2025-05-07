# 📈 Android Crypto Monitor
![image](https://github.com/user-attachments/assets/9f37c649-8f45-4cec-800d-a1340f2bd471)
![image](https://github.com/user-attachments/assets/34a9c7d1-8d5a-458e-bd71-b5a18ca8724f)

Um app Android moderno, feito com Jetpack Compose + Kotlin, que consulta dados em tempo real do Mercado Bitcoin e exibe na tela com design elegante e responsivo.

---

## 🚀 Funcionalidades

🔹 Exibe as cotações de criptomoedas (ex: Bitcoin)  
🔹 Consumo de API REST com Retrofit  
🔹 Atualização com botão customizado  
🔹 Interface moderna com XML + componentes reutilizáveis  
🔹 Utiliza conceitos limpos: **MVC**, **fábricas de serviço**, **modelos bem definidos**

---

## 🧠 Arquitetura de Pastas
📁 app/
├── 📁 model/ # Representa os dados retornados pela API
│ └── TickerResponse.kt # Modelo principal de resposta
│
├── 📁 service/
│ ├── MercadoBitcoinService.kt # Interface Retrofit
│ └── MercadoBitcoinServiceFactory.kt # Fábrica de Retrofit com baseURL
│
├── 📁 ui/theme/ # Tema customizado do Compose
│ ├── Color.kt
│ ├── Theme.kt
│ └── Type.kt
│
├── 📁 res/layout/ # Componentes visuais XML
│ ├── activity_main.xml
│ ├── component_toolbar_main.xml
│ ├── component_quote_information.xml
│ └── component_button_refresh.xml
│
└── MainActivity.kt # Lógica principal da interface e requisições


## 🧪 Como Funciona

1. `MainActivity.kt` chama `makeRestCall()`, que usa a `MercadoBitcoinService`
2. O Retrofit busca os dados da moeda na URL definida
3. A resposta (`TickerResponse`) é usada para preencher os `TextView` com preço, variação etc.
4. O botão com o drawable `shape_button_refresh.xml` permite nova consulta manual

---

## 🖼️ Interface Visual

- Composição visual feita com componentes modulares
- Estilo definido nos arquivos de tema
- Ícones e backgrounds adaptáveis a diferentes densidades (`mipmap-*dpi`)

---

## 🛠️ Como Rodar

1. Clone este repositório
2. Abra no Android Studio
3. Rode no emulador ou dispositivo real com Android 8+

```bash
git clone https://github.com/SEU_USUARIO/android-crypto-monitor.git
