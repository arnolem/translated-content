---
title: DataView.prototype.setInt16()
slug: Web/JavaScript/Reference/Global_Objects/DataView/setInt16
---

{{JSRef}}Метод **`setInt16()`** содержит 16-битное целое (short) значение в байте, смещённым по указанному числу от начала {{jsxref("DataView")}}.

{{InteractiveExample("JavaScript Demo: DataView.setInt16()")}}

```js interactive-example
// Create an ArrayBuffer with a size in bytes
const buffer = new ArrayBuffer(16);

const view = new DataView(buffer);
view.setInt16(1, 32767); // Max signed 16-bit integer

console.log(view.getInt16(1));
// Expected output: 32767
```

## Синтаксис

```
dataview.setInt16(byteOffset, value [, littleEndian])
```

### Параметры

- byteOffset
  - : Смещение в байтах от старта до этого значения, где будут храниться данные.
- value
  - : Устанавливаемое значение.
- littleEndian
  - : {{optional_inline}} Указывает, сохранять ли 16-bit целое в {{Glossary("Endianness", "little- or big-endian")}} формате. Если значение false или undefined, записывает значение big-endian.

### Возвращаемое значение

{{jsxref("undefined")}}.

### Возвращаемые ошибки

- {{jsxref("RangeError")}}
  - : Выдана, если `byteOffset` установлен так, что целое бы хранилось после конца.

## Примеры

### Использование метода `setInt16`

```js
var buffer = new ArrayBuffer(8);
var dataview = new DataView(buffer);
dataview.setInt16(1, 3);
dataview.getInt16(1); // 3
```

## Спецификации

{{Specifications}}

## Совместимость с браузерами

{{Compat}}

## Смотрите также

- {{jsxref("DataView")}}
- {{jsxref("ArrayBuffer")}}
