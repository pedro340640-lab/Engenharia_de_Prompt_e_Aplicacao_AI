Proposta do projeto: criar um site de lembretes com foco em compromisso com outras pessoas, onde o usuário cadastraria a pessoa(o cadastro sere pro usuário er um fácil acesso aos dados da pessoa caso prcise entrar em contato com ela para cancelar ou coisa do tipo, ninguém além d usuário teria acesso a esses dados, seria como a lista de contatos) e poderia criar um lembrete de por exemplo um passeio, então o usuario escolheria como quanto tempo de antecedencia gostaria de ser lembrado, além de eventos únicos o usuário poderia criar eventos recorentes, sejam eles diários, semanais ou mensais, e ele teria diversas opções de dados para o evento, como por exemplo a opção de selecionar o local.

Ferramenta escolhida:Bubble
Motivo da escolha:Foi o que eu achei mais fácil de usar

Vantagens identificadas:
1-A IA consegue fazer uma grande váriedades de coisa dentro de um só projeto.

2-Ela já usa imagens sem vc precisar upá-las.

3-A conversa com IA é bem simples e direta, ela consege fazer as edições rápidamente.



Limitações encontradas:
1-Ela acaba gerando certas coisas que não foram pedidas, o que pode acabar atrapalhando.

2-Ela acaba gerando erros de código que você precisa explicar e pedir para ela corrigir.

3-Dificuldade de interação com coisas pré criadas como imagens ou códigos



Reflexão critica:
A principal dificuldade que eu tive foi corrigir erros que a IA acabava gerando e tirar as coisas a mais que ela fez, para corrigir isso eu refiz o código com mais especificações.

​Role: You are an expert Bubble.io developer. Build a responsive, secure web application based on the following strict specifications, database architecture, and privacy rules.
​1. Core Concept & Value Proposition
​A personal commitment and reminder tracking system. The app allows users to manage upcoming events, meetings, or casual outings specifically tied to other people. It functions as a private CRM combined with an advanced, flexible reminder engine.
​2. Database Architecture (Data Types & Fields)
​You must create the following Data Types with these exact fields:
​User (Built-in)
​Email (Text)
​Password (Password)
​Contact
​Created By (User, automatic)
​Full Name (Text, Required)
​Phone Number (Text)
​Email Address (Text)
​Notes (Text)
​Note: This acts as a private contact list for the user.
​Event
​Created By (User, automatic)
​Title/Description (Text, Required)
​Associated Contact (Contact, Required)
​Event Date & Time (Date, Required)
​Location (Text)
​Is Recurring (Yes/No, Default: No)
​Recurrence Type (Option Set: Daily, Weekly, Monthly)
​Reminder Lead Time (Number, representing minutes/hours before the event)
​Reminder Unit (Option Set: Minutes, Hours, Days)
​3. Strict Security & Privacy Rules (Crucial)
​Mandatory Privacy Rule: Data isolation is absolute. No user must ever see contacts or events created by another user.
​Contact Privacy Rule: Current User is This Contact's Created By. Grant full find, view, and edit permissions only when this condition is true. Everyone else: No access.
​Event Privacy Rule: Current User is This Event's Created By. Grant full find, view, and edit permissions only when this condition is true. Everyone else: No access.
​4. UI/UX & Page Structure
​Page 1: Dashboard (index / dashboard)
​Header: User profile, logout button.
​Sidebar/Navigation: Links to "My Events" and "My Contacts".
​Main Panel - "Upcoming Commitments": A Repeating Group displaying the logged-in user's upcoming events, sorted by Event Date & Time (ascending).
​Quick Action Button: "New Event" (opens a popup) and "New Contact" (opens a popup).
​Popup 1: Create/Edit Contact
​Fields: Full Name (Input), Phone Number (Input), Email (Input), Notes (Multiline Input).
​Workflow: "Save" creates a new Contact bound to the current user and closes the popup.
​Popup 2: Create/Edit Event
​Fields:
​Title (Input)
​Contact (Dropdown: Choices source = Do a search for Contacts where Created By = Current User, Option caption = Current Contact's Full Name)
​Date & Time (Date/Time Picker)
​Location (SearchBox with geographic addresses or text input)
​Is Recurring? (Checkbox)
​Recurrence Type (Dropdown conditional: Only visible if "Is Recurring" is checked. Options: Daily, Weekly, Monthly)
​Reminder Lead Time (Integer Input, e.g., 30)
​Reminder Unit (Dropdown: Minutes, Hours, Days)
​5. Core Backend Workflows & Logic
​Reminder Trigger Engine
​Set up a Bubble Backend Workflow named send_reminder.
​When a new Event is created, trigger a scheduled API Workflow send_reminder.
​Scheduled Date Calculation: Event's Date & Time minus Reminder Lead Time (converted to hours/days/minutes based on Reminder Unit).
​Action: Send an email/notification to the Current User containing the event details, location, and the Associated Contact's phone/email for quick access in case of cancellation.
​Recurrence Logic
​If Is Recurring is Yes, when the scheduled Event Date & Time passes, a backend workflow must automatically generate the next occurrence based on the Recurrence Type (+1 Day for Daily, +1 Week for Weekly, +1 Month for Monthly).
​6. Limitations & Constraints
​No Public Pages: All pages except login/sign-up must redirect to the login page if the Current User is logged out.
​Data Validation: The "Save Event" button must remain unclickable until Title, Contact, and Date & Time are properly filled.





































































































                                









   
