# 00 · קלטים חיצוניים ורקע

עובדות שנאספו ממקורות ציבוריים **לפני** הניתוח. הן קובעות *היכן לחפש* בנתונים
(אילו דומיינים ופרמטרים של מעקב לצפות למצוא); הן **אינן** משמשות כתוצאות.


## רשתות affiliate לכל מותג

| מותג | רשת/רשתות | טביעת המעקב הצפויה ב-clickstream | מקור |
|---|---|---|---|
| **Saatva** | **Partnerize** (מאז Feb 2018), בניהול סוכנות JEBCommerce | הפניה (redirect) מסוג `prf.hn/click/camref:<id>` (מזהה הקמפיין בנתיב); ה-URL של הנחיתה נושא `?clickref=<id>` | רשת: [JEBCommerce](https://jebcommerce.com/now-managing-the-saatva-affiliate-program/), [מקרה בוחן של Partnerize](https://go.partnerize.com/case-study-saatva). פורמט מעקב: [מדריך קישורי המעקב של Partnerize](https://docs.partnerize.com/transferwise/Tracking_instructions_for_the_TransferWise_affiliate_program.pdf) (`prf.hn`, `camref`), [מאמר העזרה של Partnerize על S2S](https://help.phgsupport.com/hc/en-us/articles/360020395238-Tracking-Partnerize-Server-to-Server-S2S-Integration) (`clickref` בנחיתה) |
| Saatva (משנית) | **Sovrn//Commerce (VigLink): מאומת** - עמוד המרצ'נט מציג את saatva.com, saatvadreams.com, saatvamattress.com כפתוחים. Skimlinks: העמוד המצוטט לא מציג תוכן של Saatva, ולכן **לא מאומת**. Awin: אין מקור, ולכן **לא מאומת** | `redirect.viglink.com`, `go.skimresources.com`, `awin1.com` (דומיינים על סמך ידע כללי, לא מאומתים). יש לבדוק בנתונים גם את דומייני המותג הנוספים `saatvadreams.com`, `saatvamattress.com` | [עמוד המרצ'נט ב-VigLink](https://www.viglink.com/merchants/4994/saatva-inc-affiliate-program) |
| **Nectar** | Impact | הנחיתה נושאת `irclickid` (+ `irgwc`). דומיין ההפניה **לא מאומת**: `*.sjv.io` / `*.pxf.io` / `*.7eer.net` הם דומיינים נפוצים של Impact על סמך ידע כללי; Impact משתמשת גם בדומיינים ייעודיים לכל מותג (למשל `imp.i317572.net` בדוגמה אמיתית), ולכן רשימת הדומיינים חייבת להגיע מהנתונים | רשת: [עמוד ה-affiliates של Nectar](https://www.nectarsleep.com/l/affiliates). `irclickid` / `irgwc` ב-URL נחיתה אמיתי של Impact: [Brave issue #33952](https://github.com/brave/brave-browser/issues/33952) |
| **Helix** | Impact (ל-Helix יש עמוד מותג ב-marketplace של Impact; העמוד עצמו חוסם קריאה אוטומטית, ולכן התוכן לא נבדק) | כמו ב-Nectar | [עמוד המותג ב-Impact](https://app.impact.com/campaign-campaign-info-v2/Helix-Sleep.brand) |
| **DreamCloud** | אותה חברת אם כמו Nectar (Resident Home, שנרכשה על ידי Ashley, הודעה ב-March 2024), ולכן הרשת **לא מאומתת**, לאישור בנתונים | לאישור | [PR Newswire: Ashley ו-Resident מודיעות על הרכישה](https://www.prnewswire.com/news-releases/ashley-and-resident-announce-acquisition-302080558.html) |
| **Walmart** | Impact (מאז June 2019; לפני כן affiliates ב-Rakuten LinkShare); עוגייה של 72 שעות | צפויים פרמטרים של Impact. `goto.walmart.com`, `veh=aff`, `sourceid=imp_` **לא מאומתים** (ידע כללי) | [Geniuslink](https://geniuslink.com/blog/walmart-affiliate-program/) |

### השלכות על הניתוח
- **Saatva היא לקוחה של Partnerize.** הניתוח צריך לדבר בשפה של הרשת (publisher,
  EPC, שותפים מניבי הכנסה) ולהימנע מטענות שה-clickstream לא יכול לתמוך בהן.
- מקרה הבוחן הציבורי של Partnerize מדווח על צמיחת התוכנית של Saatva ב**הכנסות (+62% YoY)**,
  ב**שותפים מניבי הכנסה (+48%)** וב-**EPC (+27%)**. אלה מדדי KPI שימושיים למסגור: עץ
  הגורמים במסמך 01 (publishers × קליקים ל-publisher × המרה) ממופה ישירות אליהם.
- **ל-Nectar ול-DreamCloud יש חברת אם משותפת.** צפויה חפיפה ב-publishers ומבנה תוכנית
  דומה; כדאי להתייחס אליהן כזוג טבעי בהשוואה.
- **חלונות שיוך שונים לכל מותג** (Walmart 72 h לעומת חלונות DTC טיפוסיים של 30 יום) משמעם
  שחלון קבוע אחד הוא בחירת מידול, ולא כלל התשלום בפועל של המותגים.
- הרשתות שונות בין המותגים, ולכן נדרש מילון פרמטרים שנבנה **לכל מותג מתוך הנתונים**;
  רשימה קשיחה אחת הייתה מובילה לספירת חסר אצל מותגים שנמצאים ברשתות שלא צפינו.

## קלט להרחבה

| קלט | ערך | מקור | שימוש |
|---|---|---|---|
| משתמשי אינטרנט בארה"ב | ≈ 322 M (January 2025, 93.1% מתוך 346 M) | [DataReportal, Digital 2025: United States of America](https://datareportal.com/reports/digital-2025-united-states-of-america) | המכנה של מקדם ההרחבה לארה"ב (מסמך 07) |

הסתייגות: אוכלוסיית ה-panel קרובה יותר ל*משתמשי דפדפן בדסקטופ עם תוסף מותקן* מאשר
לכלל משתמשי האינטרנט בארה"ב. האומדנים המוחלטים לארה"ב יורשים את אי הוודאות הזו; ההשוואות והיחסים בין המותגים מושפעים הרבה פחות, כי ההטיה חלה על כל המותגים באותה מידה.
