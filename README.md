Блок №1: AreaCalculator. Нарушен Принцип открытости/закрытости (OCP)
Нарушение заключается в том, что при добавлении новых форм (например, треугольник, эллипс и т.д.) вам нужно будет изменять существующий метод calculateArea. Это нарушает OCP, так как код не является закрытым для изменений и расширений.

Блок №2: Worker и Robot. Нарушен Принцип разделения интерфейса (ISP):
Интерфейс Worker требует, чтобы класс Robot реализовал метод eat(), который не нужен роботу. Это нарушает ISP, так как робот не должен реализовывать методы, которые ему не нужны.


Блок №3: Customer и Order. Нарушен Принцип единственной ответственности (SRP):
Класс Customer выполняет как размещение заказа, так и отправку уведомлений, что нарушает SRP, так как он отвечает за несколько различных задач.

Блок №4: Switch и LightBulb. Нарушен Принцип инверсии зависимостей (DIP):
Класс Switch зависит от конкретного класса LightBulb, что нарушает DIP. Switch должен зависеть от абстракции, а не от конкретной реализации лампочки.

Блок №5: Bird и Penguin. Нарушен Принцип подстановки Барбары Лисков (LSP):
Класс Penguin расширяет Bird и переопределяет метод fly, выбрасывая исключение. Это нарушает LSP, так как потомки класса Bird должны сохранять поведение, не изменяя логику базового класса.