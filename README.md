# buterbrodkap-open-case-script
ВОТ ЭТО ДА!!!!

## Процесс создания кейсов (Я делал все в хроме и вам советую)

* Открываем https://convars.com/ru (я нажал кнопку логина у меня все крашнулось нахуй, не рекомендую)

* Тык на *CS:GO Симулятор* вкладку 

* Открываем Custom case

![custom case](https://i.imgur.com/Vz0byM2.png)

* Тык на *Открыть Редактор*

* Тык на *Редактировать список предметов* 

* Тык на *Кастомные предметы* 

![custom items](https://i.imgur.com/o2MjDl8.png)

* Если у вас уже есть какие то предметы, то во-первых какого хуя??? во-вторых надо будет очистить кукисы

* Открываем код элемента на кнопку F12, затем вкладку Console

* Открываем файл ids_players.txt и через cntrl + a копируем все его содержимое

* Прописываем команду и жмем энтер

```js
const raw_ids = *ставим двойные ковычки и туда пастим айдишники из буфера обмена*;
```

![raw_ids](https://i.imgur.com/LzvUJ9b.png)

* Открываем файл nicks_players.txt и через cntrl + a копируем все его содержимое

* Прописываем команду и жмем энтер

```js
const raw_nicks = *ставим двойные ковычки и туда пастим айдишники из буфера обмена*;
```

* Копируем штуку что я написал снизу и вставляем, жмем энтер

```js
const ids = raw_ids.split(",");
const player_nicks = raw_nicks.split(",");
function add_players_to_case(players){
    players.map((player, index) => {
        customCaseEditCustomItems();
        document.getElementById("textarea_customitems1").value=player;
        document.getElementById("textarea_customitems3").value = `https://a.ppy.sh/${ids[index]}`;
        updateCustomItem(true);
        customCaseImportCustomItemButton("")
    });
};
add_players_to_case(player_nicks);
```

* Сейчас надо будет подождать

* Дождались? Теперь пишем

```js
function load_players_to_case(players){
    players.map(player => {
        customCaseAddItem(player.toLowerCase());
    });
};
load_players_to_case(player_nicks);
```

* Ждем еще дольше

* Долго? Ждите больше!

* Жмем "Сохранить предметы и выйти"

* Теперь "Выйти из Редактора"

* Жмем "Открыть контейнер" (консоль можно закрыть)

* Если вы хотите сделать все снова то чистим кукисы по картинкам снизу

![1](https://i.imgur.com/jX3q32S.png)

![2](https://i.imgur.com/DaPvwCo.png)

![3](https://i.imgur.com/1mic9Pv.png)