# DH Generator

**DH Generator** - класс для упрощения работы с [протоколом Диффи-Хеллмана](https://ru.wikipedia.org/wiki/Протокол_Диффи_—_Хеллмана) на **PHP**

### Установка (Qero)

```cmd
php Qero.phar install KRypt0nn/DH-Generator
```

### Использование

```php
<?php

namespace DHGenerator;

// g = 2348
// p = 24723847

// Если не указан третий параметр (a/b) - будет сгенерировано случайное число

# Создаём генераторы для Алисы и Боба (клиент А и клиент Б)
$A = new Generator (2348, 24723847);
$B = new Generator (2348, 24723847);

# Генерируем и выводим общие секретные ключи
echo 'A: '. $A->generate ($B->getAlpha ()) . PHP_EOL;
echo 'B: '. $B->generate ($A->getAlpha ());
```

Автор: [Подвирный Никита](https://vk.com/technomindlp). Специально для [Enfesto Studio Group](https://vk.com/hphp_convertation)