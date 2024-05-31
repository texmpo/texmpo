---
comments: true
---

# SUDIAO SD 2128

Обрабатывающий центр для Нестинга (ЧПУ фрезер под нестинг со сверлильной головой)
  <style>
    *,
    *::before,
    *::after {
      -webkit-box-sizing: border-box;
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
      'Helvetica Neue', Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
      'Segoe UI Symbol';
    }
    .container {
      max-width: 700px;
      margin: 0 auto;
    }
    .itc-slider__items {
      counter-reset: slide;
    }
    .itc-slider__item {
      flex: 0 0 100%;
      max-width: 100%;
      counter-increment: slide;
      height: 500px;
      position: relative;
    }
</style>

<div class="container">

  <div class="itc-slider" data-slider="itc-slider" data-loop="false" data-autoplay="true">
    <div class="itc-slider__wrapper">
      <div class="itc-slider__items">
        <div class="itc-slider__item">
          <img loading=lazy src="../images/CNC3.jpg">
        </div>
        <div class="itc-slider__item">
          <img loading=lazy src="../images/6MB.jpg">
        </div>
        <div class="itc-slider__item">
          <img loading=lazy src="../images/60W-E.jpg">
        </div>
      </div>
    </div>
    <button class="itc-slider__btn itc-slider__btn_prev"></button>
    <button class="itc-slider__btn itc-slider__btn_next"></button>
  </div>

</div>

### Ограничения 

Имя файла УП должно быть <31 символа и не должно содержать кириллицу (6MB)

## Инструкции

  * [60W-E Wood Operation Manual](<60W-E Wood Operation Manual.pdf>)
  * [6MB инструкция по эксплуатации](<Syntec 6mb.pdf>)
  * [Mill Machine Program Manual](<Mill Machine Program Manual.pdf>)

## M-коды

??? abstract "Спойлер"

    {{ read_excel('SYNTEC M CODE.xlsx') }}

## G-коды (60W-E)

??? abstract "Спойлер"

    {{ read_excel('SYNTEC G CODE.xlsx') }}

## Подпрограммы
  * M98 P1008 - смена инструмента на фрезу :material-diameter-variant: 8 мм
  * M98 P2008 - смена инструмента на сверло :material-diameter-variant: 8 мм
  * M98 P0300 - обрезок M200, идет в конце перед M0 M200 и применяется когда изделие зафиксировано скобами

## Параметры
  * 3225 - Screen saver delay time
  <!-- * 401 - "Cutting acceleration time" (ms) Время Ускорения и торможения для рабочей подачи [0,60000] (Время разгона и торможения для G01, G02, G03, G33. Чем больше значение, тем плавнее движение)
  * 541~560 ускорение отдельно на каждую ось параметры  -->
## Файлы

  * [Постпроцессор для стойки Syntec 60W-E и 6MD под ArtCam 2018 со сменой инструмента](Syntec_postp.con)
    * [Postprocessor Configuration Guide](<Postprocessor Configuration Guide.pdf>)
  * [База инструмента ArtCAM 2018](<База инструмент ArtCAM 2018.tdb>)
  * Подпрограммы инструментов
    * [6MB](<Tools 6MD.rar>)
    * [60W-E](<Tools 60W-E.rar>)
  * [Macro](<Syntec MACRO.rar>)

## Ссылки

  * [Эксплуатация JINAN SUDIAO S2 // Syntec 6MB](<https://www.youtube.com/embed/lS1k_7Ozp2o?si=wtop_FCrCmOr6a6O>){target="_blank"}

  * [mir-cnc](http://mir-cnc.ru/forum/153-%D0%B2%D0%BE%D0%BF%D1%80%D0%BE%D1%81%D1%8B-%D0%BF%D0%BE-%D1%81%D1%82%D0%BE%D0%B9%D0%BA%D0%B5-syntec/){target="_blank"}

## Резервные копии [[alt]](https://disk.yandex.com/d/cLvS3bdstcgD0g){target="_blank"}
  * [Backup cnc1 6mb 2024](<backup/system backup cnc1 6mb.rar>)
  * [Backup cnc2 60we 2024](<backup/system backup cnc2 60we.rar>)
  * [Backup cnc2 60we 2024](<backup/system backup cnc3 60we.rar>)
<link href="../stylesheets/itc-slider.css" rel="stylesheet">
<script src="../javascripts/itc-slider.js" defer=""></script>