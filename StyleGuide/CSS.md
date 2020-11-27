## Порядок объявления
Объявления логически связанных свойств должны быть сгруппированы в следующем порядке:

1. Позиционирование
2. Блочная модель
3. Типографика
4. Отображение
   
Позиционирование следует первым потому, что оно может удалить элемент из нормального потока документа и переопределить блочную модель связанных стилей. Блочная модель идет следующей, так как она диктует размеры и расположение компонента.

Все остальные объявления, выполняющиеся внутри компонента или не оказывающие влияния на предыдущие два раздела, следуют в последнюю очередь.

```css
.declaration-order {
  /* Позиционирование */
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 100;

  /* Блочная модель */
  display: block;
  float: right;
  width: 100px;
  height: 100px;

  /* Типографика */
  font: normal 13px "Helvetica Neue", sans-serif;
  line-height: 1.5;
  color: #333;
  text-align: center;

  /* Отображение */
  background-color: #f5f5f5;
  border: 1px solid #e5e5e5;
  border-radius: 3px;

  /* Прочее */
  opacity: 1;
}
```