# ⚔️ KochBratanTeam — Minecraft Сервер & Донат-Сайт

Сайт для Minecraft сервера **KochBratanTeam**, выполненный в нежном стеклянном стиле (cherry/rose glassmorphism) с интерактивным магазином донат-привилегий, виджетом копирования IP, таймером скидок, вкладками правил и интеграцией с **DonationAlerts**.

---

## 🚀 Как открыть сайт

Просто дважды кликните по файлу **`index.html`** в этой папке. Он откроется в вашем браузере (Chrome, Edge, Opera, Яндекс и т.д.). Всё работает автономно без интернета и серверов.

---

## 💰 Как изменить цены на привилегии

Откройте `index.html` в любом текстовом редакторе (Блокнот, VS Code, Notepad++):
Найдите строчку `<section id="donate">`. У каждой карточки ранга указаны цены:

Пример для **VIP**:
```html
<div class="price">
  <b>79 ₽</b><em>навсегда</em>
  <s>149 ₽</s>
  <span class="off">−47%</span>
</div>
<button class="btn ghost donate-trigger" type="button" 
        data-rank="VIP" 
        data-price="79" 
        data-oldprice="149" 
        data-icon="⭐">
  Приобрести
</button>
```

Просто поменяйте числа `79` и `149` на ваши цены!

---

## 🌐 Ссылка на DonationAlerts

В файле `index.html` внизу в скрипте установлена ваша ссылка:
```javascript
const DONATE_URL = "https://www.donationalerts.com/r/httpsrootfirst";
```

### Как работает покупка:
1. Игрок нажимает **«Приобрести»** на нужной привилегии.
2. Вводит свой **Minecraft никнейм**.
3. Нажимает **«Перейти к оплате через DonationAlerts»**:
   - В буфер обмена копируется готовый текст: `Ник: Player | Донат: VIP (79₽)`.
   - В новой вкладке открывается страница DonationAlerts.
   - Игроку остаётся только вставить скопированный комментарий и оплатить.

---

## ⛏️ Как сменить IP адрес сервера

В файле `index.html`:
1. В строке `<code class="ip-code" id="server-ip">play.kochbratan.ru</code>`
2. В скрипте: `const SERVER_IP = "play.kochbratan.ru";`
Замените `play.kochbratan.ru` на IP или домен вашего сервера.