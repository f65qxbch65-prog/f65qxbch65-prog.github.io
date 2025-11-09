index.7e12aadd-0e1f-4b70-bffe-107bc0b57f5e
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Фотограф Артём Щукин | Воронеж</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f9f9f9; color: #333; }
    header { background: #111; color: #fff; padding: 40px 20px; text-align: center; }
    header h1 { margin: 0; font-size: 2.5em; }
    header p { margin: 10px 0 20px; font-size: 1.2em; }
    header a { background: #fff; color: #111; padding: 10px 20px; border-radius: 8px; text-decoration: none; font-weight: bold; }
    section { padding: 40px 20px; max-width: 900px; margin: auto; }
    h2 { margin-top: 0; }
    .portfolio a { display: inline-block; margin-top: 10px; color: #3366cc; text-decoration: none; font-weight: bold; }
    .contact a { color: #3366cc; text-decoration: none; }
    .gallery { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 20px; justify-content: center; }
    .gallery img { width: 100%; max-width: 280px; border-radius: 8px; object-fit: cover; }
    .form-wrapper { margin-top: 30px; }
    form { display: flex; flex-direction: column; gap: 10px; }
    input, textarea { padding: 10px; font-size: 1em; border-radius: 5px; border: 1px solid #ccc; }
    button { padding: 10px; background-color: #111; color: #fff; border: none; border-radius: 8px; cursor: pointer; }
    footer { background: #eee; padding: 20px; text-align: center; font-size: 0.9em; }
    .btn { display: inline-block; margin-top: 20px; padding: 10px 20px; background: #111; color: #fff; border-radius: 8px; text-decoration: none; }
    @media (max-width: 600px) {
      .gallery { flex-direction: column; align-items: center; }
    }
  </style>
</head>
<body>
  <header>
    <h1>Артём Щукин</h1>
    <p>Фотограф в Воронеже — репортаж, корпоративы, фотосессии</p>
    <a href="#portfolio">Посмотреть портфолио</a>
  </header>

  <section>
    <h2>Обо мне</h2>
    <p>Я — фотограф, для которого важны живые моменты. 3 года учёбы и практики дали мне главное — быть в тени событий и ловить подлинные эмоции. Работаю быстро, фото отдаю за 3–4 дня. Главное — чтобы вы чувствовали себя естественно и расслабленно.</p>
  </section>

  <section>
    <h2>Услуги</h2>
    <ul>
      <li>📸 Репортажные съёмки</li>
      <li>🏢 Корпоративные мероприятия</li>
      <li>🧍‍♂️ Индивидуальные фотосессии</li>
    </ul>
  </section>

  <section id="portfolio" class="portfolio">
    <h2>Портфолио</h2>
    <div class="gallery">
      <img src="data:image/jpeg;base64,..." alt="Свадебное фото" />
      <img src="data:image/jpeg;base64,..." alt="Девушка в окне" />
      <img src="data:image/jpeg;base64,..." alt="Соревнования" />
    </div>
    <p style="margin-top: 20px;">Полное портфолио вы можете посмотреть по ссылке:</p>
    <a href="https://disk.yandex.ru/d/jEEcL11gXAlYYg" target="_blank">Открыть портфолио в Яндекс.Диске</a>
  </section>

  <section class="contact">
    <h2>Контакты</h2>
    <p>📞 Телефон: <a href="tel:+79040825339">+7 904 082 53 39</a></p>
    <p>📧 Email: <a href="mailto:artyomshchukin000@gmail.com">artyomshchukin000@gmail.com</a></p>
    <p>🖇️ VK: <a href="https://vk.com/8artemy8" target="_blank">vk.com/8artemy8</a></p>
    <a href="https://vk.com/8artemy8" class="btn" target="_blank">Записаться на съёмку</a>

    <div class="form-wrapper">
      <h3>Оставить заявку</h3>
      <form id="tg-form">
        <input type="text" name="name" placeholder="Ваше имя" required />
        <input type="email" name="email" placeholder="Ваш email" required />
        <textarea name="message" rows="4" placeholder="Сообщение или вопрос"></textarea>
        <button type="submit">Отправить</button>
      </form>
    </div>
  </section>

  <footer>
    © 2025 Артём Щукин | Все права защищены
  </footer>

  <script>
    const form = document.getElementById('tg-form');
    form.addEventListener('submit', function (e) {
      e.preventDefault();
      const token = '8366358779:AAGa_UDCwS3ohAB1mMrI_oTHdIj_TnpsXFM';
      const chat_id = '822079479';
      const name = form.name.value;
      const email = form.email.value;
      const message = form.message.value;
      const text = `Новая заявка:\nИмя: ${name}\nEmail: ${email}\nСообщение: ${message}`;

      fetch(`https://api.telegram.org/bot${token}/sendMessage`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
          chat_id: chat_id,
          text: text
        })
      }).then(() => {
        alert('Заявка отправлена!');
        form.reset();
      }).catch(() => {
        alert('Ошибка отправки.');
      });
    });
  </script>
</body>
</html>





