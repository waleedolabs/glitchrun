<div align="center">

<img src="og.png" alt="GLITCHRUN" width="720">

# GLITCHRUN

**لعبة كتابة بالعربي: اكسر القواعد قبل ما تنرقّع.**
*A free-text Arabic browser game. Break the rules before they get patched.*

[![Play](https://img.shields.io/badge/▶_العب_هلأ-waleedolabs.github.io/glitchrun-F5B83D?style=for-the-badge&labelColor=0D0F17)](https://waleedolabs.github.io/glitchrun/)
[![Play in English](https://img.shields.io/badge/▶_Play_in_English-?lang=en-5AA9FF?style=for-the-badge&labelColor=0D0F17)](https://waleedolabs.github.io/glitchrun/?lang=en)

![status](https://img.shields.io/badge/status-MVP-F5B83D?labelColor=0D0F17)
![free](https://img.shields.io/badge/free-no_signup-3DDC97?labelColor=0D0F17)
![lang](https://img.shields.io/badge/العربية_%7C_English-5AA9FF?labelColor=0D0F17)
![license](https://img.shields.io/badge/license-MIT-888?labelColor=0D0F17)

<img src="demo.gif" alt="gameplay" width="270">

[🎬 شوف الفيديو](promo.mp4) · [🇬🇧 English](#english)

</div>

---

## شو هي اللعبة؟

بتكون محبوس بمرحلة (غرفة، طابور فرن، قصر، مركب…) وهدفك تطلع منها بأقل عدد حركات.
**ما في أزرار ولا خيارات.** بتكتب شو بدك تعمل بكلامك: فصحى، عامية، أو فرانكو (`kasser el baab`).

- **سارد ذكي** بيحكي شو صار بأسلوب عامي.
- **الكود هو الحكم.** السارد ما بيقرر مين ربح، قواعد ثابتة بالكود بتقرر. ما بتقدر تخدعه وتكتب "انتصرت".
- **كل ثغرة بتنكشف مرة وحدة.** لما تلاقي حيلة ذكية ما حدا فكر فيها، بتنكتب باسمك وبتنرقّع بالجولة الجاية، وبتاخد 💡.

## كيف تلعب (٣ خطوات)

1. **افتح** [الرابط](https://waleedolabs.github.io/glitchrun/). ما في تسجيل ولا تحميل.
2. **اكتب** شو بدك تعمل بالخانة تحت: `اطلع من الشباك`، `اشتري من جاري بسعر أعلى`، `خذ المفتاح وافتح الباب`.
3. **اربح** بأقل حركات. كل مرحلة بتعطيك نجوم (⭐⭐⭐ = بطل)، والمرحلة اللي بعدها بتنفتح.

### نصايح

| إذا علقت | جرّب |
|---|---|
| ما بعرف شو أعمل | زر **شو في بالغرفة؟** أو 💡 أول تلميح كل جولة ببلاش |
| الجواب غريب | اكتب أبسط وبجملة وحدة، فيك تكتب بالفرانكو |
| بدك نجمة زيادة | احفظ الحل وجرّب تعمله بحركات أقل |
| بدك تتحدى صاحبك | زر **شارك البطاقة** أو **واتساب**، الرابط بيحمل حيلتك |

## المراحل

الغرفة المقفلة · طابور الفرن · الملك · المركب · المكتبة · الفضاء · الامتحان
+ **تحدي يومي** جديد كل يوم وسلسلة أيام متتالية 🔥

المرحلتان الأولى والثانية مفتوحتان، والباقي بيفتح لما تحل اللي قبله.

## كيف بتشتغل؟ (للمطورين)

```
المتصفح (index.html)  ──►  Cloudflare Worker  ──►  نموذج لغوي (سارد + تقدير)
        │                      (توقيع الجولات، D1، حدود الاستخدام)
        └─ محرّك قواعد حتمي (deterministic) = الحكم النهائي
```

- ملف HTML واحد، بدون مكتبات. التقدّم محفوظ بـ`localStorage`.
- الـWorker بيوقّع الجولات (HMAC)، وبيحدّ الطلبات، وبيخزّن الأحكام بـD1.
- إذا الـAPI وقع، اللعبة بتكمّل بـ**وضع بسيط** محلي بدون سارد.

## الحالة

**MVP.** اللعبة شغالة وقابلة للعب بالكامل، لكن لسا بتتطور: تلميحات بالمشهد لكل ثغرة، مراحل جديدة، ولوحة متصدرين.
لقيت خطأ أو ثغرة؟ افتح [Issue](../../issues).

## English

**GLITCHRUN** is a free-text browser game. You're stuck in a scene (a locked room, a bakery line, a palace, a sinking boat...) and you type what you do, in your own words. An AI narrator describes what happens, but **fixed rules in code decide the outcome**, so you can't just type "I win". Find a hidden trick (a *glitch*) and you earn a lamp 💡, but every glitch gets **patched** after you use it.

- **Play in English:** <https://waleedolabs.github.io/glitchrun/?lang=en> (or use the `EN` / `ع` button in the game's top bar).
- 7 levels + a new daily challenge every day. Levels 1 and 2 are open; the rest unlock as you clear the previous one.
- No signup. Progress is saved in your browser.
- Status: **MVP**. Bugs or ideas? Open an [Issue](../../issues).

## شارك اللعبة

> لعبة عربية: اكتب بكلامك واكسر القواعد قبل ما تنرقّع 😈 جرّبها: https://waleedolabs.github.io/glitchrun/

<div align="center">

**GLITCHRUN** · العربية + English

</div>
