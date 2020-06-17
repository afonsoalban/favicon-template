# Favicon Boilerplate
Para auxiliar na criação de um pacote de ícones.

## Referências
* [Favicons, Touch Icons, Tile Icons, etc. Which Do You Need?](https://css-tricks.com/favicon-quiz/)

## Arquivos
* ~~**favicon.ico**: 32 x 32px~~ (descontinuado)
* **favicon-16x16.png**: 16 x 16px (PNG sem fundo)
* **favicon.png**: 32 x 32px (ícone padrão, PNG sem fundo)
* **apple-touch-icon.png**: 180 x 180px (PNG com fundo, é o maior tamanho que o iOS vai procurar)
* **android-chrome-192x192.png**: 192 x 192px (PNG sem fundo)
* **android-chrome-512x512.png**: 512 x 512px (PNG sem fundo para telas de alta densidade)
* **manifest.json**
    * especifica os caminhos para os dois ícones
    * indica se o site deve rodar no Chrome ou como um APP `display: ['standalone', 'fullscreen', 'browser', 'minimal-ui']`
    * configura uma cor de fundo para a splash screen `theme_color` e `background_color`
* **mstile-150x150.png**: 270 x 270px (PNG sem fundo, com ícone branco)
* **browserconfig.xml**
    * define o caminho do arquivo `mstile`
    * define a cor de fundo para a tile do arquivo PNG
* **safari-pinned-tab.svg**: arquivo SVG com a máscara para a aba no Safari

## Tags no HTML
A definição do caminho é necessária apenas para alguns arquivos. Outros são definidos no `manifest.json` e `browserconfig.xml`.

É preciso definir uma cor para a aba do Safari, no `link[rel="mask-icon"]`. E uma cor para o "tema" do Chrome no Android (o padrão é branco) em `meta[name="theme-color"]`.

```HTML
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon.png">
<link rel="icon" type="image/png" sizes="192x192" href="/android-chrome-192x192.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<link rel="manifest" href="/manifest.json">
<link rel="mask-icon" href="/safari-pinned-tab.svg" color="#274894">
<meta name="theme-color" content="#ffffff">
```