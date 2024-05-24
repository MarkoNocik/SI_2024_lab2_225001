1. # Марко Ноциќ 225001

2. ![]

3. Цикломатската комплексност е 10. Таа е добиена бидејќи има 9 услови во функцијата(предикати) односно 7 if услови и два услови во for loop. На крај се додава 1 и се добива 10.

4. Според Every branch има 7 тест случаи.
- allItems е null (ќе се фрли исклучок).
- Item со null име и валиден баркод, без попуст  - allItems = [new Item(null, "123456", 50, 0)], payment = 100 
- Item со валидно име и без баркод - ([new Item("item1", null, 50, 0)], payment = 100) Излез: Исклучок RuntimeException("No barcode!")
- Item со валидно име и валиден баркод со невалиден карактер (allItems = [new Item("item1", "123a56", 50, 0)], payment = 100) ќе се фрли исклучок RuntimeException("Invalid character in item barcode!")
- Item со цена > 300, попуст > 0, баркод почнува со '0' (allItems = [new Item("item1", "0123456", 350, 0.1)], payment = 31)
- Вкупна сума поголема од плаќањето (allItems = [new Item("item1", "123456", 150, 0)], payment = 100)
- Вкупната сума е помала од плаќањето (sum > payment)
