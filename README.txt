# Dragão Guerreiro — casca do aplicativo

Esta pasta é a versão estática para GitHub Pages.

- O ícone fica hospedado localmente no GitHub Pages.
- O aplicativo exibido dentro da página continua sendo o Web App do Google Apps Script:
  https://script.google.com/macros/s/AKfycby69WviyJNQkAk0VNfX0aYpaUztkWyzXKJGzyIpHwJcqh5rP5GMHqqa_PZM7gfonefX/exec

## Antes de publicar

No `Code.gs` do Apps Script, o `doGet()` deve permitir incorporação em iframe:

```javascript
function doGet() {
  return HtmlService.createHtmlOutputFromFile('Index')
      .setTitle('Dragão Guerreiro')
      .addMetaTag('viewport', 'width=device-width, initial-scale=1')
      .setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL);
}
```
