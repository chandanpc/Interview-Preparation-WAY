God Way
В этом примере интерфейс Logger определяет метод log(), который записывает сообщение лога. Классы ConsoleLogger и FileLogger реализуют этот интерфейс и предоставляют свои собственные реализации метода log(). Класс LogManager принимает объект логгера через конструктор и использует его для записи логов при выполнении определенных действий. Если вам нужно добавить новый способ записи логов, например, запись в базу данных, вы можете создать новый класс, реализующий интерфейс Logger, без изменения существующего кода.



Bad Way
В этом примере класс LogManager нарушает принцип OCP. Метод doSomething() прямо вызывает конкретные методы logToConsole() и logToFile(), что ограничивает возможность добавления новых способов логирования без изменения самого класса LogManager.