# Namoz Vaqti API

Namoz vaqtlarini bilish mumkin bo'lgan API. Ma'lumotlar islom.uz saytidan olingan.
Serverga request ni json shaklida jo'nating.

| API Endpoints       | description                                              |
| ------------------- | -------------------------------------------------------- |
| `/api/monthly`      | Bir oylik ma'lumotni obyeklar massivi sifatida qaytaradi |
| `/api/daily`        | Bir kunlik ma'lumotni obyekt sifatida qaytaradi          |
| `/api/present/day`  | Request jonatilgan kun boyicha malumot qaytaradi         |
| `/api/present/week` | Request jonatilgan hafta boyicha malumot qaytaradi       |

| request body element | description                                              |
| -------------------- | -------------------------------------------------------- |
| region               | hudud nomi. masalan: Toshkent, Qo'qon                    |
| month                | oy raqamda 0-12gacha bo'lgan raqam. masalan: 1, 9        |
| day                  | kun raqam bo'lishi kerak. 1-31 gacha. masalan: 1, 15, 31 |

## Example request

[GET] `/api/monthly` endpoint uchun

| Parameter | value       |
| --------- | ----------- |
| `region`  | "Toshkent", |
| `month`   | 9           |

final: `/api/monthly?region=Toshkent&month=9`

[GET] `/api/daily` endpoint uchun

| Parameter | value      |
| --------- | ---------- |
| `region`  | "Toshkent" |
| `month`   | 9          |
| `day`     | 1          |

final: `/api/daily?region=Toshkent&month=9&day=1`

[GET] `/api/present/day` endpoint uchun

| Parameter | value      |
| --------- | ---------- |
| `region`  | "Toshkent" |

final: `/api/present/day?region=Toshkent`

[GET] `/api/present/week` endpoint uchun

| Parameter | value      |
| --------- | ---------- |
| `region`  | "Toshkent" |

final: `/api/present/week?region=Toshkent`

API so'rovlari:

Bugungi namoz vaqtlarini olish uchun: https://islomapi.uz/api/present/day?region=Toshkent

Shu hafta uchun namoz taqvimi olish uchun: https://islomapi.uz/api/present/week?region=Toshkent

Bir kun uchun namoz taqvimini olish uchun: https://islomapi.uz/api/daily?region=Toshkent&month=4=4&day=5

Bir oylik namoz taqvimini olish uchun: https://islomapi.uz/api/monthly?region=Toshkent&month=4


#### Viloyat va mintaqalar (JSON)

```
const provencie = [
   "Toshkent",
   "Farg'ona",
   "Samarqand",
   "Xorazm",
   "Navoiy",
   "Qashqadaryo",
   "Surxondaryo",
   "Andijon",
   "Namangan",
   "Jizzax",
   "Buxoro",
   "Sirdaryo",
];



const regions = [
   "Оltiariq",
   "Bishkek",
   "O'smat",
   "To'rtko'l",
   "Uzunquduq",
   "Jizzax",
   "Оltinko'l",
   "Chimkent",
   "Rishtоn",
   "Xo'jaоbоd",
   "Do'stlik",
   "Buxoro",
   "Termiz",
   "Dushanbye",
   "Turkmanоbоd",
   "Qоrоvulbоzоr",
   "Оlmaоta",
   "Xоnqa",
   "Tallimarjоn",
   "Uchqo'rg'оn",
   "Uchtepa",
   "Xоnоbоd",
   "Toshkent",
   "G'uzоr",
   "Bekоbоd",
   "Navoiy",
   "Qo'rg'оntepa",
   "Mubоrak",
   "Ashxabоd",
   "Оlоt",
   "Jalоlоbоd",
   "Nurоta",
   "Andijon",
   "Turkistоn",
   "Shumanay",
   "Namangan",
   "Chimbоy",
   "Jоmbоy",
   "Sherоbоd",
   "Mo'ynоq",
   "Bulоqbоshi",
   "Uchquduq",
   "Samarqand",
   "Qiziltepa",
   "Zоmin",
   "Xo'jand",
   "Tоmdi",
   "Yangibоzоr",
   "Jambul",
   "Nukus",
   "Chоrtоq",
   "Taxtako'pir",
   "Tоshhоvuz",
   "Xiva",
   "Kоsоnsоy",
   "Kоnimex",
   "Mingbulоq",
   "Paxtaоbоd",
   "Denоv",
   "O'g'iz",
   "Qo'ng'irоt",
   "Chust",
   "Kattaqo'rg'оn",
   "Farg'оna",
   "Qоrako'l",
   "Arnasоy",
   "Osh",
   "Sayram",
   "Angren",
   "Pоp",
   "G'allaоrоl",
   "Urgut",
   "Shahrixоn",
   "Guliston",
   "Qumqo'rg'оn",
   "Bоysun",
   "Urganch",
   "Qo'qon",
   "Gazli",
   "Xazоrasp",
   "Marg'ilon",
   "Shоvоt",
   "Kоnibоdоm",
   "Quva",
   "Burchmulla",
   "Dehqоnоbоd",
   "Zarafshоn",
   "Qarshi",
   "Kоsоn"
]


```




### Author: islom.uz
