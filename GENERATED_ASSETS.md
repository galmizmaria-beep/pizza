# Новые ассеты для версии 1.1

Созданы встроенным инструментом **imagegen**. Прозрачный alpha-канал проверен; все результаты визуально просмотрены.

Рабочие изображения находятся в `assets/`, полные исходники генерации сохранены локально в `assets/generated/`. В опубликованном редакторе используются их встроенные копии из `starter-assets.js`, поэтому внешние ссылки не нужны.

| Файл | Назначение |
|---|---|
| topping-sauce.png | Тонкий слой томатного соуса без миски и ложки |
| topping-cheese.png | Тёртый сыр без чашки |
| topping-pepperoni.png | Отдельные кружочки пепперони без тарелки |
| topping-mushrooms.png | Ломтики грибов без чашки |
| topping-tomato.png | Отдельный ломтик помидора; в рецепте «Маргарита» используется пять настраиваемых копий |
| topping-basil.png | Листья базилика |
| topping-olives.png | Колечки оливок |
| pizza-margherita.png | Готовая «Маргарита» |
| pizza-pepperoni.png | Готовая «Пепперони» |
| pizza-mushroom.png | Готовая «Грибная» |
| pizza-combo.png | Готовая «Комбо» с пепперони, грибами и оливками |
| counter-empty.png | Первый вариант пустого стола; сохранён как дополнительный ассет |
| counter-deep.png | Основной пустой стол с широкой глубокой рабочей поверхностью |
| customer-plain.png | Клиент без нарисованной пиццы и облачка: изображение выбранного заказа теперь добавляется игрой |

## Промпты

Общее описание для семи слоёв продуктов и трёх первых пицц:

> Use case: stylized-concept. Asset type: separate transparent PNG sprite for an educational children’s pizzeria game. Style: polished warm 2D hand-painted cartoon illustration with soft outlines, matching the supplied cozy pizzeria assets. Golden warm lighting, readable shapes. Composition centered with comfortable transparent margins. No text, no letters, no watermark. Genuinely transparent alpha background, no checkerboard drawn into the image. Each output is ONE separate asset.

К нему добавлялись предметные инструкции:

- **Соус:** A thin round spread of rich tomato sauce, slightly oval seen from 30 degrees above, smoothly spread for a pizza layer. Sauce only, NO dough, no plate, no bowl, no spoon, no garnish.
- **Сыр:** Loose grated mozzarella cheese strands distributed in a thin wide round layer, slightly oval seen from 30 degrees above, to overlay a pizza. Cheese only, NO crust, no dough, no dish, no bowl. Transparent gaps between strands.
- **Пепперони:** Seven separate appetizing round pepperoni slices, distributed with generous transparent gaps in a wide round arrangement viewed from slightly above. Pepperoni only, no cheese, no crust, no dough, no plate, no bowl.
- **Грибы:** Seven separate sliced button mushrooms, distributed with generous transparent gaps in a wide round arrangement viewed from slightly above. Mushroom slices only, no crust, no dough, no plate, no bowl.
- **Помидоры:** Six separate red tomato slices, distributed with generous transparent gaps in a wide round arrangement viewed from slightly above. Tomato only, no crust, no dough, no plate, no bowl. Результат — один отдельный ломтик; для игрового слоя созданы пять экземпляров этого изображения.
- **Базилик:** Seven individual fresh green basil leaves, distributed with generous transparent gaps in a wide round arrangement viewed from slightly above. Basil only, no stems, no crust, no dough, no plate, no bowl.
- **Оливки:** Ten separate sliced black olive rings, distributed with generous transparent gaps in a wide round arrangement viewed from slightly above. Olive rings only, no crust, no dough, no plate, no bowl.
- **Маргарита:** One complete delicious Margherita pizza with golden crust, tomato sauce, melted mozzarella, red tomato slices and green basil leaves. Slightly oval seen from 30 degrees above. No mushrooms, no pepperoni, no olives. Entire pizza visible.
- **Пепперони:** One complete delicious Pepperoni pizza with golden crust, tomato sauce, melted mozzarella and evenly distributed pepperoni slices. Slightly oval seen from 30 degrees above. No mushrooms, no basil, no tomato slices, no olives. Entire pizza visible.
- **Грибная:** One complete delicious mushroom pizza with golden crust, tomato sauce, melted mozzarella and evenly distributed sliced button mushrooms. Slightly oval seen from 30 degrees above. No pepperoni, no tomato slices, no olives. Entire pizza visible.
- **Пустой стол:** One empty wide wooden pizzeria prep counter with teal green cabinet doors underneath, same cozy cartoon kitchen style. The entire wooden work surface is completely empty and clean: no bowls, no plates, no food, no herbs, no bottles, no utensils, no metal trays, no flour, no pizza. Front view from slightly above, wide horizontal composition. Entire piece of furniture visible.

**Комбо:** Use case: stylized-concept. One separate transparent PNG sprite for a cozy educational children’s pizzeria game. A complete delicious COMBO pizza with golden crust, tomato sauce, melted mozzarella, evenly scattered pepperoni slices, button mushroom slices and black olive rings. ALL three toppings must be clearly visible. Slightly oval pizza seen from 30 degrees above. Polished warm 2D hand-painted cartoon illustration with soft outlines, golden warm lighting, matching the existing pizzeria sprites. Entire pizza centered, comfortable transparent margins. No plate, no bowl, no text, no watermark, genuinely transparent alpha background.

**Глубокий стол, редактирование первого варианта:** Use case: precise-object-edit. This image is the edit target. Create a sibling empty pizzeria prep counter sprite in exactly the same warm polished cartoon style, wood color, teal cabinet color. Change ONLY its perspective and proportions: view it from much higher above, so the broad deep EMPTY wooden work surface occupies approximately the upper 65 percent of the visible furniture, and the cabinet front occupies only the lower 35 percent. The table needs enough apparent depth to place a whole large pizza fully ON the wooden work surface rather than over the cabinet doors. Make the entire furniture large and fill the canvas with very small transparent margins. Keep the entire work surface absolutely empty and clean, without any bowls, utensils, plants, ingredients, flour or other objects. No text. Transparent alpha background. Wide horizontal isolated sprite.

**Клиент без статичного заказа:** Use case: precise-object-edit / identity-preserve. Edit target: the supplied cute cartoon boy customer sprite. Remove ONLY the entire speech bubble, the pizza inside the bubble, its tail and the yellow emphasis strokes. Replace those removed parts with genuinely transparent alpha. Preserve the boy exactly: same face and identity, brown hair, expression, pose, pointing finger, green jacket, cream hoodie, blue backpack, scale, placement, colors, warm 2D cartoon shading, and bottom crop. Do not add any objects, feet, text, new bubble or pizza. This separate transparent customer sprite will stand behind a counter; the game will render a dynamic order bubble showing the selected pizza instead of the fixed baked-in one. Preserve the original boy cleanly with no changes.

## Дополнения 1.2

Созданы встроенным ImageGen, каждый PNG отдельным вызовом. Исходники: `assets/generated/`; готовые копии до 700 px: `assets/`.

### topping-ham

Файл: `assets/topping-ham.png`

Промпт: Use case: stylized-concept. A separate transparent PNG sprite for a cozy educational children’s pizzeria game. Several separate thin pink cooked ham strips scattered with transparent gaps in a wide round pizza topping arrangement. Ham only, no bowl, no dish, no dough or cheese. Match the existing polished warm hand-painted 2D cartoon food art, soft outlines, golden lighting, readable clean shapes. View from 30 degrees above, slightly oval composition. Centered, whole subject visible, transparent margins. Genuine transparent alpha background. No text, no letters, no watermark, no kitchen furniture. One separate asset only.

### topping-chicken

Файл: `assets/topping-chicken.png`

Промпт: Use case: stylized-concept. A separate transparent PNG sprite for a cozy educational children’s pizzeria game. Several separate bite-size pieces of cooked tender golden chicken scattered with transparent gaps in a wide round pizza topping arrangement. Chicken only, no bowl, no dish, no dough or cheese. Match the existing polished warm hand-painted 2D cartoon food art, soft outlines, golden lighting, readable clean shapes. View from 30 degrees above, slightly oval composition. Centered, whole subject visible, transparent margins. Genuine transparent alpha background. No text, no letters, no watermark, no kitchen furniture. One separate asset only.

### topping-pepper

Файл: `assets/topping-pepper.png`

Промпт: Use case: stylized-concept. A separate transparent PNG sprite for a cozy educational children’s pizzeria game. Separate curved red, yellow and green sweet bell pepper strips scattered with transparent gaps in a wide round pizza topping arrangement. Pepper only, no bowl, no dish, no dough or cheese. Match the existing polished warm hand-painted 2D cartoon food art, soft outlines, golden lighting, readable clean shapes. View from 30 degrees above, slightly oval composition. Centered, whole subject visible, transparent margins. Genuine transparent alpha background. No text, no letters, no watermark, no kitchen furniture. One separate asset only.

### topping-corn

Файл: `assets/topping-corn.png`

Промпт: Use case: stylized-concept. A separate transparent PNG sprite for a cozy educational children’s pizzeria game. Many separate shiny golden sweet corn kernels scattered with transparent gaps in a wide round pizza topping arrangement. Corn only, no bowl, no dish, no dough or cheese. Match the existing polished warm hand-painted 2D cartoon food art, soft outlines, golden lighting, readable clean shapes. View from 30 degrees above, slightly oval composition. Centered, whole subject visible, transparent margins. Genuine transparent alpha background. No text, no letters, no watermark, no kitchen furniture. One separate asset only.

### topping-pineapple

Файл: `assets/topping-pineapple.png`

Промпт: Use case: stylized-concept. A separate transparent PNG sprite for a cozy educational children’s pizzeria game. Several separate juicy yellow pineapple chunks scattered with transparent gaps in a wide round pizza topping arrangement. Pineapple only, no bowl, no dish, no dough or cheese. Match the existing polished warm hand-painted 2D cartoon food art, soft outlines, golden lighting, readable clean shapes. View from 30 degrees above, slightly oval composition. Centered, whole subject visible, transparent margins. Genuine transparent alpha background. No text, no letters, no watermark, no kitchen furniture. One separate asset only.

### topping-onion

Файл: `assets/topping-onion.png`

Промпт: Use case: stylized-concept. A separate transparent PNG sprite for a cozy educational children’s pizzeria game. Several separate thin purple red onion rings and half rings scattered with transparent gaps in a wide round pizza topping arrangement. Onion only, no bowl, no dish, no dough or cheese. Match the existing polished warm hand-painted 2D cartoon food art, soft outlines, golden lighting, readable clean shapes. View from 30 degrees above, slightly oval composition. Centered, whole subject visible, transparent margins. Genuine transparent alpha background. No text, no letters, no watermark, no kitchen furniture. One separate asset only.

### pizza-combo12

Файл: `assets/pizza-combo12.png`

Промпт: Use case: stylized-concept. A separate transparent PNG sprite for a cozy educational children’s pizzeria game. One complete baked deluxe pizza with golden crust, tomato sauce, melted mozzarella, pepperoni slices, mushroom slices, tomato slices, basil leaves, black olive rings, ham strips, chicken pieces, bell pepper strips and corn kernels. All eleven topping types recognizable, balanced arrangement and appetizing warm cartoon style. No pineapple, no onion, no plate. Match the existing polished warm hand-painted 2D cartoon food art, soft outlines, golden lighting, readable clean shapes. View from 30 degrees above, slightly oval composition. Centered, whole subject visible, transparent margins. Genuine transparent alpha background. No text, no letters, no watermark, no kitchen furniture. One separate asset only.

### pizza-combo14

Файл: `assets/pizza-combo14.png`

Промпт: Use case: stylized-concept. A separate transparent PNG sprite for a cozy educational children’s pizzeria game. One complete baked extra deluxe pizza with golden crust, tomato sauce, melted mozzarella, pepperoni slices, mushroom slices, tomato slices, basil leaves, black olive rings, ham strips, chicken pieces, bell pepper strips, corn kernels, pineapple chunks and purple onion rings. All thirteen topping types recognizable, balanced arrangement and appetizing warm cartoon style. No plate. Match the existing polished warm hand-painted 2D cartoon food art, soft outlines, golden lighting, readable clean shapes. View from 30 degrees above, slightly oval composition. Centered, whole subject visible, transparent margins. Genuine transparent alpha background. No text, no letters, no watermark, no kitchen furniture. One separate asset only.
