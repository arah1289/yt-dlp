

`yt-dlp` هو أداة قوية لتحميل الفيديوهات من مواقع الإنترنت المختلفة، وهو بديلاً محسنًا لبرنامج `youtube-dl`. في هذا الملف، ستجد قائمة شاملة من الأوامر التي يمكن استخدامها مع `yt-dlp` لتحميل الفيديوهات، قوائم التشغيل، الترجمة، وأكثر.

## الأوامر الأساسية

### 1. تنزيل فيديو من رابط
```bash
yt-dlp <رابط الفيديو>

على سبيل المثال:

yt-dlp https://www.youtube.com/watch?v=example
2. تنزيل قائمة تشغيل
yt-dlp <رابط قائمة التشغيل>

على سبيل المثال:

yt-dlp https://www.youtube.com/playlist?list=example
3. تنزيل عدة مقاطع فيديو من روابط متعددة
yt-dlp -a <اسم الملف الذي يحتوي على الروابط>

على سبيل المثال:

yt-dlp -a urls.txt

حيث يحتوي الملف urls.txt على قائمة من الروابط، واحد في كل سطر.

4. تنزيل الفيديو بجودة محددة
yt-dlp -f <كود الجودة>

على سبيل المثال:

yt-dlp -f 22 https://www.youtube.com/watch?v=example

للحصول على قائمة بجميع الخيارات المتاحة للجودة، يمكنك استخدام:

yt-dlp -F <رابط الفيديو>
الترجمة
1. تنزيل الترجمة
yt-dlp --write-srt <رابط الفيديو>

لتنزيل الترجمة مع الفيديو.

2. تنزيل الترجمة بلغة معينة
yt-dlp --write-srt --sub-lang <رمز اللغة> <رابط الفيديو>

على سبيل المثال:

yt-dlp --write-srt --sub-lang en https://www.youtube.com/watch?v=example
3. تنزيل الترجمة بدون تنزيل الفيديو
yt-dlp --skip-download --write-srt <رابط الفيديو>
4. تنزيل الترجمة بصيغة VTT
yt-dlp --write-vtt <رابط الفيديو>
5. تضمين الترجمة مع الفيديو
yt-dlp --embed-subs <رابط الفيديو>
الإعدادات المتقدمة
1. تغيير اسم الملف الذي يتم حفظه
yt-dlp -o "<مسار/اسم_الملف.EXT>"

على سبيل المثال:

yt-dlp -o "~/Downloads/%(title)s.%(ext)s" https://www.youtube.com/watch?v=example
2. تنزيل الفيديو بجودة صوت فقط
yt-dlp -f bestaudio <رابط الفيديو>
3. تحديد عدد المقاطع التي سيتم تنزيلها من قائمة تشغيل
yt-dlp --playlist-items <رقم_المقطع> <رابط قائمة التشغيل>

على سبيل المثال:

yt-dlp --playlist-items 1,2,3 https://www.youtube.com/playlist?list=example
4. تنزيل الملفات كـ Audio فقط
yt-dlp -x --audio-format mp3 <رابط الفيديو>
5. تحديد سرعة التنزيل
yt-dlp --limit-rate <الحد_الأقصى_للسرعة>

على سبيل المثال:

yt-dlp --limit-rate 500K https://www.youtube.com/watch?v=example
