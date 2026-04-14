# Wrong Cases — Context-Dependent Questions
**Total:** 10 questions | 1.3% of all wrong cases. These questions only make sense within a conversation context.

---

## 1. faq_2689
- **Domain:** mobile
- **Categories:** tariff_info, archived_tariff, tariff_switching
- **Intent:** tariff_inquiry, technical_support
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question refers to a specific tariff plan without naming it, making the answer's warning about archiving relevant only if the user is already on a specific plan or if the context of which plan is being discussed is known.

### Question
Shu tarif rejasiga ótmoqchiman

### Expected Answer (Ground Truth)
Inobatga oling! Sizni tarifingiz arxiv boʻlib yopilgan, boshka tarifga oʻtsangiz amaldagi tarifga kaytib oʻtish imkoni boʻlmaydi.

### Retrieved Chunks
```
1. [FAQ] | Savol: Telefon raqamimni ozimni nomimga otkazmoqchi edim
Raqamni boshqa abonentga qayta rasmiylashtirish uchun shartnoma egasi va qabul qiluvchi shaxs shaxsini tasdiqlovchi hujjat (pasport, ID-karta va yangi turdagi haydovchilik guvohnomasi) bilan UZTELECOM sotuv va xizmat ko'rsatish ofisiga murojaat qilishi kerak. Bundan tashqari, abonentning barcha berilgan shaxsiy hisobvaraqlari bo'yicha qarzlari bo'lmasligi kerak. Agar qayta rasmiylashtiriladigan raqam pullik toifadagi raqam bo'lsa, u holda xizmat narxiga va raqamning toifasiga qarab to'lovni amalga oshirish kerak.
(manba: uztelecom_faq_v2)

2. [FAQ] | Savol: Telefon nomerim band bolgan paytda boshqa nomerga adresatsiya qilish kerak
Pereadresatsiya xizmati! Barcha qo`ngiroqlarni yo`naltirish: USSD *21*+998 kod telefon raqami# Band bo`lganda: USSD *67*+998 ko`d telefon raqami# Javob bolmaganda: USSD *61*+998 ko`d telefon raqami# O`chirish: USSD ##002#
(manba: uztelecom_faq_v2)

3. [FAQ] | Savol: Men onlayn telefon raqamini sotib olishni xoxlayman
Sotuvdagi raqamlar roʻyxati maʼlumoti Bizda mavjud emas. Bu masalada Bosh ofisga yoki xududiy sotuv va xizmat koʻrsatish ofislariga murojaat qilishingizni soʻraymiz. Yoki sayt orqali onlayn tarzda raqam tanlashingiz mumkin. Bunda Siz rakamni ush bu xavola orkali tanlashingiz mumkin https://uztelecom.uz/uz/jismoniy-shaxslarga/mobil-raqamlarni-onlayn-band-qilish/ Chiroyli raqamlar : https://uztelecom.uz/uz/jismoniy-shaxslarga/mobil-aloqa/gsm/foydali-axborot/chiroyli-raqamlar.
(manba: uztelecom_faq_v2)
```

### Why Wrong
The retrieved context discusses number transfer, call forwarding, and buying numbers, but contains no information about activating roaming in Kazakhstan or the specific USSD code *188*1*1*1# mentioned in the ground truth.

---

## 2. faq_1720
- **Domain:** wifi
- **Categories:** wifi_troubleshooting, speed_test, router_restart, diagnostics
- **Intent:** internet_issue
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question contains vague pronouns like 'shunga' (to this) and 'yana' (again) that require prior conversation context to be understood.

### Question
shunga yana bita restart berb yuborilar

### Expected Answer (Ground Truth)
Routerdan barcha qurilmalarni uzib qo'ying(telefon, kompyuter, televizor va h.k). Keyin routerni oldiga borib faqat bitta telefonda ulanib Internet.yandex.ru/fast.com saytiga kiring(ushbu sayt tezlikni tekshirib beradi). VPN dasturi telefoningizda bo'lsa o'chirib qo'ying, chunki VPN tezlikni pasaytiradi. Internet.yandex.ru/fast.com saytida tezlikni natijasini screenshot qilib menga yuboring.

### Retrieved Chunks
```
1. [FAQ] | Savol: Uztelecomda qanday qarz olib boladi
"Exrta balans" xizmati "Exrta balans" xizmati tezda hisobingizni toldirishga yordam beradi 1000 sum dan boshlab. Xizmatdan foydalanish uchun 150 ga sms orqali yoki *150# menu orqali foydalanishingiz mumkun. Batafsil malumot uchun.https://uztelecom.uz/uz/jismoniy-shaxslarga/mobil-aloqa/gsm-2/xizmatlar/extra-balans.
(manba: uztelecom_faq_v2)

2. [FAQ] | Savol: Uztelecom ilovasiga qanday ulansam buladi
MyUZTELECOM ilovasi yordamida xizmatlarni boshqaring, toʻlovlar va pul oʻtkazmalarini amalga oshiring https://utc.uz/app.
(manba: uztelecom_faq_v2)

3. [FAQ] | Savol: belline raqamim bn uztelecomga otmiqchiman qanday otsam boladi
Ushbu xizmat MNP. Xizmat narxi 70 000 so'm. Buning uchun sizning raqamingiz faol holatda bo'lishi kerak, qarzlar yo'q va Aktsiyalar bo'yicha majburiyat bo'lmasligi kerak. Kompaniyamizga o'tish uchun veb-saytimiz orqali onlayn ariza qoldirishingiz mumkin https://uztelecom.uz/, savdo va xizmat ko'rsatish ofisi orqali shuningdek davlat xizmatlari agentligi orqali (Yagona darcha)
(manba: uztelecom_faq_v2)
```

### Why Wrong
The retrieved context discusses mobile balance, the mobile app, and number portability, but contains no information regarding the 'HAMMASI BIRGA' promotion or whether family members can benefit from it.

---

## 3. faq_3071
- **Domain:** mobile
- **Categories:** technical_settings, sms_center, phone_diagnostics, ussd_code
- **Intent:** technical_support
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question 'How is it configured' is too vague without context to determine if the answer about SMS center configuration is relevant.

### Question
Qanday sozlanadi

### Expected Answer (Ground Truth)
*#*#4636#*#* kodini terasiz va telefoningizda Informatsiya o telefone 1, Informatsiya o telefone 2 maʼlumoti chiqadi simkartangiz nechanchi simkratada toʻrgan boʻlsa shuni tanlab kirasiz va kirganingizda oxirida SMSC yozuvida boʻsh katak chiqadi shu erga +998991390102 raqamni yozib 2ta obnovit tugmasini bosasiz va telefoningizni oʻchirib yoqib qayta tekshirib koʻring sms yuborib boshqa raqamga.

### Retrieved Chunks
```
1. [FAQ] | Savol: Mening raqamimdagi ijtimoiy tarmoq obunalarini qanday o'chirish mumkin?
Xar xil norasmiy saytlar yokida ilovalar asosida yoqilib qoladigan xizmatlar bu. Yaʼni reklama asosida chiqadigan rasmlarni X qilib oʻchirtirmoqchi boʻlganingizda boshqa bir saytga oʻtib ketgan vaqtda ulanib qoladi , yoki notogʻri USSD kod yordamida, qisqa raqamiga sms tarzida javob yuborilganda. Ushbu xizmatlar boshqa saytga havola qilingan turli saytlar va ilovalar orqali avtomatik ravishda ulanadi va PUSH bildirishnomasi yuboriladi yoki siz *102# orqali notoʻgʻri USSD kodni terish orqali ulanasiz yoki qisqa raqamlarga SMS javob yuborish orqali ulanasiz. Bunday xizmatlarni xech qachon Kompaniya ulamaydi.Agar xech qanday viktorina, o'yinlarda ishtirok etmasangiz, barcha pullik obuna xizmatlarni *199*1*1*1# USSD kodi yordamida, "ko'ngilochar portallarni o'chirish"ni tanlab bekor qilishingiz mumkin. Xizmat o'chirilganda, barcha to'plangan ballar o'chadi. 24 soat ichida bekor boʻladi, kun davomida sms xabar keladi o'chganlik to'grisida.
(manba: uztelecom_faq_v2)

2. [FAQ] | Savol: Menga oyiga berilgan mb ishlamayapti
Abonent sizni sovolingiz nima boyicha Mobil aloka yoki WI-FI boyichami Siz xozirda Uzonlayn opratoriga tushdingiz.
(manba: uztelecom_faq_v2)

3. [FAQ] | Savol: Oylik tarifim uchgan lekin megabayt sotib olgan edi xozir ishlamay qoldi
Hurmatli abonent! Tarif rejangiz boʻyicha abonent toʻlovini echish muddati kelmagan boʻlsa, limitlar avtomatik ravishda yangilanmaydi. Limitlarni muddatidan oldin qayta faollashtirish uchun: Kelgusida toʻlovni amalga oshirishdan avval, limitlaringiz qoldigʻini va amal qilish muddatini *100*2# kodi yoki MyUZTELECOM ilovasi orqali tekshiring. Agar limitlarni vaqtidan avval yangilamoqchi boʻlsangiz, hisobingizni toʻldirib, *555*1# USSD kodi yordamida "Restart" xizmatini faollashtirishingiz kerak boʻladi. Izoh: "Restart" xizmati hisob-kitob davri kelgunga qadar tarif rejasiga muvofiq limitlarni yangidan taqdim etish imkonini beradi.
(manba: uztelecom_faq_v2)
```

### Why Wrong
The retrieved context discusses how to cancel subscriptions, general troubleshooting for internet not working, and tariff renewal issues, but it does not contain the specific explanation about daytime vs. nighttime internet packages mentioned in the ground truth.

---

## 4. faq_2547
- **Domain:** wifi
- **Categories:** billing, payment_overdue, wifi_service, activation
- **Intent:** internet_issue
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question uses vague pronouns ('shu xolat') that refer to a specific situation not defined in the text, making the answer's relevance dependent on prior conversation context.

### Question
Yana takror bulyapti shu xolat

### Expected Answer (Ground Truth)
Internet tarifingiz muddati tugagan ekan, oylik abonent to'lovini qilishingiz kerak, shu sababli internet ishlamay qolgan. To'lov qilsangiz taxminan 2 daqiqa ichida internet ishlab ketadi.

### Retrieved Chunks
```
1. [FAQ] | Savol: Menga oyiga berilgan mb ishlamayapti
Abonent sizni sovolingiz nima boyicha Mobil aloka yoki WI-FI boyichami Siz xozirda Uzonlayn opratoriga tushdingiz.
(manba: uztelecom_faq_v2)

2. [FAQ] | Savol: qizil chiroq yonib tutibdi ishlamayabdi
Asosiy qurilma va routeringiz oʻrtasida aloqa yoʻqligi koʻrsatilmoqda. Xozirda routerning qaysi chiroqchalari yonib turganligini tekshirib bera olasizmi ?
(manba: uztelecom_faq_v2)

3. [FAQ] | Savol: Raqamimga pul tashladim lekin yechib olmayapti
Xar xil norasmiy saytlar yokida ilovalar asosida yoqilib qoladigan xizmatlar bu. Yaʼni reklama asosida chiqadigan rasmlarni X qilib oʻchirtirmoqchi boʻlganingizda boshqa bir saytga oʻtib ketgan vaqtda ulanib qoladi , yoki notogʻri USSD kod yordamida, qisqa raqamiga sms tarzida javob yuborilganda. Ushbu xizmatlar boshqa saytga havola qilingan turli saytlar va ilovalar orqali avtomatik ravishda ulanadi va PUSH bildirishnomasi yuboriladi yoki siz *102# orqali notoʻgʻri USSD kodni terish orqali ulanasiz yoki qisqa raqamlarga SMS javob yuborish orqali ulanasiz. Bunday xizmatlarni xech qachon Kompaniya ulamaydi.Agar xech qanday viktorina, o'yinlarda ishtirok etmasangiz, barcha pullik obuna xizmatlarni *199*1*1*1# USSD kodi yordamida, "ko'ngilochar portallarni o'chirish"ni tanlab bekor qilishingiz mumkin. Xizmat o'chirilganda, barcha to'plangan ballar o'chadi. 24 soat ichida bekor boʻladi, kun davomida sms xabar keladi o'chganlik to'grisida.
(manba: uztelecom_faq_v2)
```

### Why Wrong
The retrieved context discusses unrelated issues like MB limits, router lights, and unauthorized subscriptions, while failing to address the specific problem of an expired internet tariff mentioned in the ground truth.

---

## 5. faq_3064
- **Domain:** mobile
- **Categories:** technical_settings, sms_center, phone_diagnostics, ussd_code
- **Intent:** technical_support
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question is too vague to determine the specific issue being reported, making it impossible to verify if the provided SMS configuration answer is relevant without further context.

### Question
Nomerni olganimdan beri shunaqa

### Expected Answer (Ground Truth)
*#*#4636#*#* kodini terasiz va telefoningizda Informatsiya o telefone 1, Informatsiya o telefone 2 maʼlumoti chiqadi simkartangiz nechanchi simkratada toʻrgan boʻlsa shuni tanlab kirasiz va kirganingizda oxirida SMSC yozuvida boʻsh katak chiqadi shu erga +998991390102 raqamni yozib 2ta obnovit tugmasini bosasiz va telefoningizni oʻchirib yoqib qayta tekshirib koʻring sms yuborib boshqa raqamga.

### Retrieved Chunks
```
1. [FAQ] | Savol: Shu nomerga telegram ochmoqchi edim lekin men ocholmayapman
Ijtimoiy tarmoqlar uchun kompaniya javob bermaydi. Quyidagi xavola orqali telegram qoʻllab quvvatlash markaziga bogʻlanishingiz mumkin: https://telegram.org/support?setln=ru.
(manba: uztelecom_faq_v2)

2. [Salom hammaga] | Narxi: 55 000 so'm/oy | Manba: https://uztelecom.uz/uz/salom-hammaga
Cheksiz qo'ng'iroq, 55 GB internet va 600 SMS o'z ichiga olgan mobil tarif.
Xususiyatlari: 51200 MB oyiga; 55 GB 1 oyga; 5; 55000 so'm/oy; Cheksiz; 55; 84 so'm/MB; 51200 megabayt oyiga
(manba: uztelecom_website_v2)

3. [Salom hammaga] | Narxi: 50 000 so'm/oy | Manba: https://uztelecom.uz/uz/salom-hammaga
Cheksiz qo'ng'iroq va 51200 MB internetli, oyiga 50 000 so'mlik Salom hammaga tarifi.
Xususiyatlari: 51200 MB oyiga; 51200 MB oyiga; 50000 so'm/oy; Cheksiz; 51200 megabayt oyiga; 84 so'm/MB; 51200 megabayt oyiga; 500
(manba: uztelecom_website_v2)
```

### Why Wrong
The retrieved context provides general tariff information and a link to Telegram support, but fails to address the specific issue of daytime internet being off while Telegram works, which is explained in the ground truth as a result of having only a night-time data package.

---

## 6. faq_2161
- **Domain:** mobile
- **Categories:** billing, restart_service, payment_cycle, limit_renewal
- **Intent:** technical_support
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question asks for general information about the current tariff, but the answer only addresses a specific scenario regarding automatic limit renewal and payment deadlines without providing the requested tariff details.

### Question
Ozim tarifim haqida malumot bersez

### Expected Answer (Ground Truth)
Hurmatli abonent! Tarif rejangiz boʻyicha abonent toʻlovini echish muddati kelmagan boʻlsa, limitlar avtomatik ravishda yangilanmaydi. Limitlarni muddatidan oldin qayta faollashtirish uchun: Kelgusida toʻlovni amalga oshirishdan avval, limitlaringiz qoldigʻini va amal qilish muddatini *100*2# kodi yoki MyUZTELECOM ilovasi orqali tekshiring. Agar limitlarni vaqtidan avval yangilamoqchi boʻlsangiz, hisobingizni toʻldirib, *555*1# USSD kodi yordamida "Restart" xizmatini faollashtirishingiz kerak boʻladi. Izoh: "Restart" xizmati hisob-kitob davri kelgunga qadar tarif rejasiga muvofiq limitlarni yangidan taqdim etish imkonini beradi.

### Retrieved Chunks
```
1. [FAQ] | Savol: Muammo boshlanvotti ancha vaqtdan beri
Ommaviy ofertaning 7.2-bandiga asosan, aloqa sifatining pasayishi yoki vaqtincha uzilishi tabiiy omillar va texnik xususiyatlarga bog'liq bo'lishi mumkin. Jumladan: Relef va qurilish: Tog'li joylar, baland binolar yaqinida yoki ichida (uy ichida yoki ko'p qavatli uylar atrofida); Inshootlar: Tonnellar, erto'lalar va boshqa er osti joylarida; Tabiiy sharoitlar: Meteorologik (ob-havo) sharoitlari va radio to'lqinlar tarqalishining tabiiy xususiyatlari. Bunday holatlarda xizmat sifati Operatorga bog'liq bo'lmasa ham sabablarga ko'ra o'zgarishi mumkin va buning uchun Operator javobgarlikni o'z zimmasiga olmaydi.
(manba: uztelecom_faq_v2)

2. [FAQ] | Savol: sms markaz mo'meri o'chib qolgan yonmayabdi
*#*#4636#*#* kodini terasiz va telefoningizda Informatsiya o telefone 1, Informatsiya o telefone 2 maʼlumoti chiqadi simkartangiz nechanchi simkratada toʻrgan boʻlsa shuni tanlab kirasiz va kirganingizda oxirida SMSC yozuvida boʻsh katak chiqadi shu erga +998991390102 raqamni yozib 2ta obnovit tugmasini bosasiz va telefoningizni oʻchirib yoqib qayta tekshirib koʻring sms yuborib boshqa raqamga.
(manba: uztelecom_faq_v2)

3. [FAQ] | Savol: Muammo hal qilinmadi
Respublika boicha antenadan uzilishlar kuzatilmoqda bu aloqa va internet sifatiga tasir qiladi elektr taminiti boicha muamolar bor ushbu muamolar tez orada bartaraf etiladi kutib turing yuzaga kelgan noqulayliklar uchun uzur sorimiz.
(manba: uztelecom_faq_v2)
```

### Why Wrong
The retrieved context discusses general network issues, SMS center codes, and outages, but does not contain the specific information about the SIM card not being registered with UZIMEI or the required contact details (1170 or uzimei.uz) mentioned in the ground truth.

---

## 7. faq_1443
- **Domain:** wifi
- **Categories:** wifi_troubleshooting, speed_test, router_restart, diagnostics
- **Intent:** internet_issue
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question states a situation ('I am sitting in a one-room apartment') without specifying a problem, making the troubleshooting answer relevant only if the implied context is about slow internet.

### Question
Bir xona narida otiripman

### Expected Answer (Ground Truth)
Routerdan barcha qurilmalarni uzib qo'ying(telefon, kompyuter, televizor va h.k). Keyin routerni oldiga borib faqat bitta telefonda ulanib Internet.yandex.ru/fast.com saytiga kiring(ushbu sayt tezlikni tekshirib beradi). VPN dasturi telefoningizda bo'lsa o'chirib qo'ying, chunki VPN tezlikni pasaytiradi. Internet.yandex.ru/fast.com saytida tezlikni natijasini screenshot qilib menga yuboring.

### Retrieved Chunks
```
1. [FAQ] | Savol: Qizil chiroq ochib yonyapti
Internet tarifingiz muddati tugagan ekan, oylik abonent to'lovini qilishingiz kerak, shu sababli internet ishlamay qolgan. To'lov qilsangiz taxminan 2 daqiqa ichida internet ishlab ketadi.
(manba: uztelecom_faq_v2)

2. ["Zamin Mobile" MCHJ] | Manba: https://uztelecom.uz/uz/-zamin-mobile-mchj
Zamin Mobile tomonidan hujjatlar muddati tugashidan oldin xabardor qilish xizmati.
(manba: uztelecom_website_v2)

3. ["DIT" MChJ] | Manba: https://uztelecom.uz/uz/-dit-mchj
Valyuta kurslari haqida kunlik SMS xabarlar yuboruvchi xizmat.
(manba: uztelecom_website_v2)
```

### Why Wrong
The retrieved context incorrectly attributes the red light issue to an expired tariff requiring payment, whereas the ground truth specifies a troubleshooting procedure involving disconnecting devices and testing speed.

---

## 8. faq_1554
- **Domain:** wifi
- **Categories:** wifi_troubleshooting, speed_test, router_restart, diagnostics
- **Intent:** internet_issue
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question is a general offer of help, while the answer provides specific technical troubleshooting steps without confirming the user's actual problem.

### Question
Mijozga yordam bera olasizmi?

### Expected Answer (Ground Truth)
Routerdan barcha qurilmalarni uzib qo'ying(telefon, kompyuter, televizor va h.k). Keyin routerni oldiga borib faqat bitta telefonda ulanib Internet.yandex.ru/fast.com saytiga kiring(ushbu sayt tezlikni tekshirib beradi). VPN dasturi telefoningizda bo'lsa o'chirib qo'ying, chunki VPN tezlikni pasaytiradi. Internet.yandex.ru/fast.com saytida tezlikni natijasini screenshot qilib menga yuboring.

### Retrieved Chunks
```
1. [FAQ] | Savol: TAS-IX 15GB ishlatilmiydi kamaymidi
TAS-IX — bu Oʻzbekiston ichidagi saytlarni oʻz ichiga olgan mahalliy internet tarmogʻi. Yaʼni, agar sizda TAS-IX uchun maxsus trafik boʻlsa, siz faqat shu tarmoqdagi saytlardan foydalana olasiz. Boshqa, xorijiy saytlarga kirishga harakat qilsangiz, asosiy balansingizdan pul echib olinishi yoki internet ishlamasligi mumkin. Ushbu tarmoq Oʻzbekistondagi internet tezligini oshirish va uning narxini pasaytirish maqsadida yaratilgan. www.uz sayti TAS-IX hududiga kiruvchi koʻplab resurslar haqida maʼlumot berishi mumkin.
(manba: uztelecom_faq_v2)

2. [FAQ] | Savol: Tezlik 5 mbit ga tushdi
Routerdan barcha qurilmalarni uzib qo'ying(telefon, kompyuter, televizor va h.k). Keyin routerni oldiga borib faqat bitta telefonda ulanib Internet.yandex.ru/fast.com saytiga kiring(ushbu sayt tezlikni tekshirib beradi). VPN dasturi telefoningizda bo'lsa o'chirib qo'ying, chunki VPN tezlikni pasaytiradi. Internet.yandex.ru/fast.com saytida tezlikni natijasini screenshot qilib menga yuboring.
(manba: uztelecom_faq_v2)

3. [“Sovremennie Texnologii” MCHJ] | Manba: https://uztelecom.uz/uz/-sovremennie-texnologii-mchj
Play Music xizmati kunlik obuna asosida ruscha, o'zbekcha va jahon xitlarini tinglash imkonini beradi.
(manba: uztelecom_website_v2)
```

### Why Wrong
The retrieved context discusses TAS-IX local traffic, internet speed troubleshooting, and a music service, but does not contain the USSD codes or instructions needed to clarify the 10 GB and 15 GB tariff options mentioned in the ground truth.

---

## 9. faq_1528
- **Domain:** wifi
- **Categories:** wifi_troubleshooting, speed_test, router_restart, diagnostics
- **Intent:** internet_issue
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question 'Ishlamayapti' (It's not working) is too vague without context to determine if the router troubleshooting steps in the answer are relevant.

### Question
Ishlamayapti

### Expected Answer (Ground Truth)
Routerdan barcha qurilmalarni uzib qo'ying(telefon, kompyuter, televizor va h.k). Keyin routerni oldiga borib faqat bitta telefonda ulanib Internet.yandex.ru/fast.com saytiga kiring(ushbu sayt tezlikni tekshirib beradi). VPN dasturi telefoningizda bo'lsa o'chirib qo'ying, chunki VPN tezlikni pasaytiradi. Internet.yandex.ru/fast.com saytida tezlikni natijasini screenshot qilib menga yuboring.

### Retrieved Chunks
```
1. [FAQ] | Savol: Nimaga ishlami qoldi
Routerdan barcha qurilmalarni uzib qo'ying(telefon, kompyuter, televizor va h.k). Keyin routerni oldiga borib faqat bitta telefonda ulanib Internet.yandex.ru/fast.com saytiga kiring(ushbu sayt tezlikni tekshirib beradi). VPN dasturi telefoningizda bo'lsa o'chirib qo'ying, chunki VPN tezlikni pasaytiradi. Internet.yandex.ru/fast.com saytida tezlikni natijasini screenshot qilib menga yuboring.
(manba: uztelecom_faq_v2)

2. [FAQ] | Savol: nimaga manga kemagan sms ga harjat yozilvoti
Xar xil norasmiy saytlar yokida ilovalar asosida yoqilib qoladigan xizmatlar bu. Yaʼni reklama asosida chiqadigan rasmlarni X qilib oʻchirtirmoqchi boʻlganingizda boshqa bir saytga oʻtib ketgan vaqtda ulanib qoladi , yoki notogʻri USSD kod yordamida, qisqa raqamiga sms tarzida javob yuborilganda. Ushbu xizmatlar boshqa saytga havola qilingan turli saytlar va ilovalar orqali avtomatik ravishda ulanadi va PUSH bildirishnomasi yuboriladi yoki siz *102# orqali notoʻgʻri USSD kodni terish orqali ulanasiz yoki qisqa raqamlarga SMS javob yuborish orqali ulanasiz. Bunday xizmatlarni xech qachon Kompaniya ulamaydi.Agar xech qanday viktorina, o'yinlarda ishtirok etmasangiz, barcha pullik obuna xizmatlarni *199*1*1*1# USSD kodi yordamida, "ko'ngilochar portallarni o'chirish"ni tanlab bekor qilishingiz mumkin. Xizmat o'chirilganda, barcha to'plangan ballar o'chadi. 24 soat ichida bekor boʻladi, kun davomida sms xabar keladi o'chganlik to'grisida.
(manba: uztelecom_faq_v2)

3. ["Zamin Mobile" MCHJ] | Manba: https://uztelecom.uz/uz/-zamin-mobile-mchj
Zamin Mobile tomonidan hujjatlar muddati tugashidan oldin xabardor qilish xizmati.
(manba: uztelecom_website_v2)
```

### Why Wrong
The retrieved context discusses internet speed issues and unauthorized SMS charges, but does not contain any information explaining why a 465 GB data allowance was granted.

---

## 10. faq_1862
- **Domain:** mobile
- **Categories:** tariff_info, tariff_switching, pricing
- **Intent:** tariff_inquiry
- **Root cause:** CONTEXT-DEPENDENT — question needs conversation history
- **Q-A audit reason:** The question 'How is it done' lacks the necessary context to determine what specific action is being asked about, making the answer about tariff switching only relevant if the context was previously established.

### Question
Qanday o'tkaziladi

### Expected Answer (Ground Truth)
Narxi pasroq tarifdan balandroq tarifga otish tekin, narxi balandroq tarifda pasroq tarifga otish 15000 so'm boladi.

### Retrieved Chunks
```
1. [FAQ] | Savol: Internet yahshi ishlamayapti bitta obnovit qlib bering
Routerdan barcha qurilmalarni uzib qo'ying(telefon, kompyuter, televizor va h.k). Keyin routerni oldiga borib faqat bitta telefonda ulanib Internet.yandex.ru/fast.com saytiga kiring(ushbu sayt tezlikni tekshirib beradi). VPN dasturi telefoningizda bo'lsa o'chirib qo'ying, chunki VPN tezlikni pasaytiradi. Internet.yandex.ru/fast.com saytida tezlikni natijasini screenshot qilib menga yuboring.
(manba: uztelecom_faq_v2)

2. [FAQ] | Savol: Qanaqa qlib oylik tolovini yangilash mumkin
Hurmatli abonent! Tarif rejangiz boʻyicha abonent toʻlovini echish muddati kelmagan boʻlsa, limitlar avtomatik ravishda yangilanmaydi. Limitlarni muddatidan oldin qayta faollashtirish uchun: Kelgusida toʻlovni amalga oshirishdan avval, limitlaringiz qoldigʻini va amal qilish muddatini *100*2# kodi yoki MyUZTELECOM ilovasi orqali tekshiring. Agar limitlarni vaqtidan avval yangilamoqchi boʻlsangiz, hisobingizni toʻldirib, *555*1# USSD kodi yordamida "Restart" xizmatini faollashtirishingiz kerak boʻladi. Izoh: "Restart" xizmati hisob-kitob davri kelgunga qadar tarif rejasiga muvofiq limitlarni yangidan taqdim etish imkonini beradi.
(manba: uztelecom_faq_v2)

3. [FAQ] | Savol: shuni qanaqa qlb yoqishi etvoroliszmi
Paroli bizada bo'midi, lekin siz standart parollarni terib ko'rishingiz mumkun: 123456 12345678 123456789
(manba: uztelecom_faq_v2)
```

### Why Wrong
The retrieved context discusses router troubleshooting, billing limits, and default passwords, but does not contain the specific phone number (71) 200-77-97 or the procedure to call for a reset as stated in the ground truth.

---
