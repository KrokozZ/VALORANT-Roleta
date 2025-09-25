# 🎯 Roleta de Agentes VALORANT

Uma aplicação web interativa para sortear agentes do VALORANT com interface temática oficial e sistema de categorização por funções.

## 📋 Índice

- [🎮 Sobre o Projeto](#-sobre-o-projeto)
- [✨ Funcionalidades](#-funcionalidades)
- [🎨 Interface e Tema](#-interface-e-tema)
- [🚀 Como Usar](#-como-usar)
- [⚙️ Tecnologias Utilizadas](#️-tecnologias-utilizadas)
- [📱 Responsividade](#-responsividade)
- [🔧 Recursos Técnicos](#-recursos-técnicos)
- [🎯 Categorias de Agentes](#-categorias-de-agentes)
- [📄 Estrutura do Código](#-estrutura-do-código)

## 🎮 Sobre o Projeto

A **Roleta de Agentes VALORANT** é uma ferramenta desenvolvida para auxiliar jogadores na escolha de agentes durante partidas. Com design inspirado na identidade visual oficial do VALORANT, oferece uma experiência imersiva e funcional.

### 🎪 Características Principais

- **Sistema de Roleta Animada**: Roleta horizontal com animação fluida
- **Categorização por Função**: Filtragem por Duelistas, Controladores, Iniciadores e Sentinelas
- **Tema Dinâmico**: Interface muda de cor baseada no agente selecionado
- **Seleção Manual**: Possibilidade de escolher agentes específicos
- **Design Responsivo**: Funciona perfeitamente em desktop e mobile

## ✨ Funcionalidades

### 🎲 Sistema de Sorteio

- **Sorteio Geral**: Sorteia entre todos os 27 agentes disponíveis
- **Sorteio por Categoria**: Sorteia apenas agentes da categoria selecionada
- **Animação da Roleta**: Efeito visual realista com desaceleração natural
- **Resultado Destacado**: Agente sorteado exibido com informações detalhadas

### 🎨 Personalização Visual

- **Cores Dinâmicas**: Interface adapta cores baseada no agente central/sorteado
- **Tema VALORANT Oficial**: Paleta de cores e tipografia autênticas
- **Efeitos Visuais**: Sombras, gradientes e animações suaves
- **Ícones Temáticos**: Font Awesome para representar cada categoria

### 🎯 Sistema de Categorias

| Categoria | Ícone | Cor | Agentes |
|-----------|-------|-----|---------|
| **Todos** | 👥 | Laranja | 27 agentes |
| **Duelistas** | 🎯 | Vermelho | 8 agentes |
| **Controladores** | 🛡️ | Verde | 6 agentes |
| **Iniciadores** | ⚡ | Amarelo | 7 agentes |
| **Sentinelas** | 🛡️ | Azul | 6 agentes |

## 🚀 Como Usar

### 1. **Seleção de Categoria**
```
┌─────────────────────────────────────────────┐
│ [🎯 Todos] [Duelistas] [Controladores] ... │
└─────────────────────────────────────────────┘
```
- Clique na categoria desejada
- Contador atualiza automaticamente
- Interface adapta às cores da categoria

### 2. **Escolha de Agentes**
```
┌─────────────────────────────────────────────┐
│ ESCOLHA OS AGENTES                          │
│ ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐            │
│ │JETT │ │REYNA│ │SAGE │ │SOVA │ ...        │
│ │  ✓  │ │     │ │  ✓  │ │     │            │
│ └─────┘ └─────┘ └─────┘ └─────┘            │
└─────────────────────────────────────────────┘
```
- **Todos selecionados**: Padrão inicial
- **Seleção manual**: Clique para marcar/desmarcar agentes
- **Ações rápidas**: Botões "TODOS" e "NENHUM"

### 3. **Sorteio**
```
┌─────────────────────────────────────────────┐
│            [🎲 SORTEAR AGENTES]             │
└─────────────────────────────────────────────┘
```
- Clique no botão principal
- Animação da roleta por 7 segundos
- Resultado exibido com detalhes do agente

## ⚙️ Tecnologias Utilizadas

### 🎨 Frontend
- **HTML5**: Estrutura semântica moderna
- **CSS3**: Animações, gradientes e responsividade
- **JavaScript ES6+**: Lógica interativa e manipulação DOM
- **Tailwind CSS**: Framework de utilidades CSS
- **Font Awesome**: Biblioteca de ícones

### 🌐 APIs e Recursos
- **VALORANT API**: `https://valorant-api.com/v1/agents?language=pt-BR`
- **Google Fonts**: Oswald (títulos) e Inter (texto)
- **LocalStorage**: Cache de dados dos agentes

### 🛠️ Recursos Técnicos
- **Cache Inteligente**: Dados armazenados por 24h
- **Lazy Loading**: Carregamento otimizado de imagens
- **Debouncing**: Prevenção de múltiplos cliques
- **Error Handling**: Tratamento de erros e fallbacks

## 📱 Responsividade

### 📱 Mobile (< 640px)
- Layout adaptado para telas pequenas
- Botões otimizados para toque
- Grid de agentes responsivo
- Texto e imagens redimensionados

### 💻 Desktop (> 640px)
- Interface completa
- Animações mais elaboradas
- Hover effects
- Layout horizontal otimizado

## 🔧 Recursos Técnicos

### 🎪 Sistema de Animação da Roleta

```javascript
// Animação com cubic-bezier para desaceleração realista
rouletteTrack.style.transition = 'transform 7s cubic-bezier(0.25, 0.1, 0.25, 1)';
rouletteTrack.style.transform = `translateX(${finalPosition}px)`;
```

### 🎨 Sistema de Cores Dinâmicas

```javascript
// Cada agente possui cores específicas da API
function updateTheme(agent) {
    const colors = agent.backgroundGradientColors;
    root.style.setProperty('--theme-primary', colors[0]);
    root.style.setProperty('--theme-secondary', colors[1]);
}
```

### ⚡ Otimizações de Performance

- **DocumentFragment**: Renderização eficiente do DOM
- **RequestAnimationFrame**: Animações suaves
- **Throttling**: Limitação de eventos de clique
- **Lazy Loading**: Carregamento progressivo de imagens

## 🎯 Categorias de Agentes

### 🔥 Duelistas (8 agentes)
Agentes focados em entrada e eliminação
- Jett, Reyna, Phoenix, Raze, Yoru, Neon, Iso, Clove

### 🛡️ Controladores (6 agentes) 
Agentes de controle de mapa e bloqueio
- Brimstone, Omen, Viper, Astra, Harbor, Clove

### ⚡ Iniciadores (7 agentes)
Agentes de reconhecimento e suporte
- Sova, Breach, Skye, KAY/O, Fade, Gekko, Deadlock

### 🛡️ Sentinelas (6 agentes)
Agentes defensivos e de suporte
- Killjoy, Cypher, Sage, Chamber, Deadlock, Vyse

## 📄 Estrutura do Código

```
📁 Scripts/
├── 📄 ROLETA VALORANT.html     # Aplicação completa (HTML + CSS + JS)
├── 📄 README.md                # Este arquivo
└── ...
```

### 🏗️ Arquitetura do HTML

```html
<!DOCTYPE html>
<html>
├── <head>                      # Meta tags, fonts, estilos
├── <body>
│   ├── <header>               # Título principal
│   ├── <main>                 # Área da roleta e resultado
│   ├── <section>              # Seleção de agentes
│   └── <footer>               # Informações adicionais
└── <script>                   # Lógica JavaScript
```

### 🎨 Organização do CSS

```css
/* Variáveis de tema VALORANT */
:root { --valorant-red, --valorant-cyan, ... }

/* Componentes principais */
.roulette-container { ... }
.agent-selector-grid { ... }
.category-tabs { ... }

/* Animações e efeitos */
@keyframes spin { ... }
@keyframes fadeIn { ... }
```

### ⚙️ Estrutura do JavaScript

```javascript
// 1. Configurações e variáveis globais
const API_URL = '...';
let allAgents = [];

// 2. Funções utilitárias
function toPureHex() { ... }
function debounce() { ... }

// 3. Funções principais
async function fetchAgents() { ... }
function spinRoulette() { ... }
function updateTheme() { ... }

// 4. Event listeners
document.addEventListener('DOMContentLoaded', init);
```

## 🚀 Instalação e Uso

### 📥 Baixar
1. Baixe o arquivo `ROLETA VALORANT.html`
2. Abra em qualquer navegador moderno
3. Conexão com internet necessária (APIs e fonts)

### 🌐 Hospedagem
- Compatible com qualquer servidor web
- Sem dependências server-side
- Funciona localmente (file://) com limitações de cache

## 🎮 Dicas de Uso

### 🎯 Para Jogadores Competitivos
- Use categories específicas para balanceamento de equipe
- Experimente diferentes combinações de agentes
- Ótimo para treinos de adaptabilidade

### 🎪 Para Streamers
- Visual atrativo para transmissões
- Interação com chat através de categorias
- Sistema de cores dinâmico chama atenção

### 👥 Para Grupos
- Cada jogador pode usar uma categoria diferente
- Sistema justo de sorteio
- Interface clara para todos acompanharem

---

## 🏆 Créditos

- **VALORANT**: Riot Games
- **API de Dados**: valorant-api.com
- **Ícones**: Font Awesome
- **Fonts**: Google Fonts

### 💡 Desenvolvido com foco em:
- 🎨 **Design autêntico** inspirado no VALORANT
- ⚡ **Performance otimizada** para todos os dispositivos  
- 🎮 **Experiência de usuário** intuitiva e envolvente
- 🔧 **Código limpo** e bem estruturado

---

**🎯 Divirta-se sorteando seus agentes e dominando o campo de batalha!**
