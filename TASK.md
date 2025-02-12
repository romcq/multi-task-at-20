# Параллелизм и асинхронность

## IO-bound. Проверяем ссылки на страницах Википедии

### Время синхронной проверки ссылок
Код работал 1138.186 сек (примерно 19 мин)

Время выполнения:

![pycharm64_Nxc8G5ntQc](https://user-images.githubusercontent.com/71966352/144597954-ba487f4e-ee09-4f61-be4d-b17398240559.png)

Диспечер задач:

![image](https://user-images.githubusercontent.com/71966352/144613993-ae72de29-e4b5-4999-8684-bb5becab40b8.png)


### Переписанный код с использованием ThreadPoolExecutor
*  5 воркеров: 


Время выполнения:


![pycharm64_gcxRgME96u](https://user-images.githubusercontent.com/71966352/144615412-3efdd4f3-a696-4ef6-94e4-74c6a939401b.png)

Диспечер задач:

![image](https://user-images.githubusercontent.com/71966352/144611122-a43283d6-00a0-4a72-9e7f-8724e5dfe242.png)

* 10 воркеров:


Время выполнения:

![pycharm64_1u4pexaSkf](https://user-images.githubusercontent.com/71966352/144616015-1e000a1b-887f-41e6-84e8-200bc3d21e01.png)

Диспечер задач:

![image](https://user-images.githubusercontent.com/71966352/144615896-83ed8dd4-07f0-4e5c-8413-1e82b0d96410.png)

* 100 воркеров:

Время выполнения:

![pycharm64_zGmQ2kco6C](https://user-images.githubusercontent.com/71966352/144616510-12d82dde-b222-442d-954c-ba6cc468a9fb.png)

Диспечер задач:

![image](https://user-images.githubusercontent.com/71966352/144616207-17ee7252-7143-41ed-8da3-bc6c44b8325f.png)

![image](https://user-images.githubusercontent.com/71966352/144616385-74d1c6b4-6047-4fb6-92a0-948f75afeb29.png)

### Итог
Незначительно возрастает использование памяти и процессора (хотя есть моменты, когда использование значительно возрастает). Сильно уменьшается время выполнения.

## CPU-bound. Генерируем монетки

* На 1 ядре:

Время выполнения:

![image](https://user-images.githubusercontent.com/71966352/144634084-e57d7454-0767-4318-9198-6b5b1ff3c9cc.png)

Диспечер задач:

![image](https://user-images.githubusercontent.com/71966352/144617966-950feb05-d238-4111-a021-9865e4da4a79.png)

* 2 воркера:

Время выполнения:

![pycharm64_d5fwwVYron](https://user-images.githubusercontent.com/71966352/144637790-9aa9f33f-9367-4222-947e-51870c0bf068.png)

Диспечер задач:

![image](https://user-images.githubusercontent.com/71966352/144636443-b485bec4-d4cf-4d45-8dde-68a586ffd7e7.png)

* 4 воркера:

Время выполнения:

![pycharm64_OhPOzNhdGw](https://user-images.githubusercontent.com/71966352/144638055-46eb16d5-0d05-445c-a003-eff103378587.png)

Диспечер задач:

![image](https://user-images.githubusercontent.com/71966352/144638089-f0eabf39-516b-4fe1-bcfa-13a5c829254a.png)

* 5 воркеров:

Время выполнения:

![pycharm64_cAoGwoVQO0](https://user-images.githubusercontent.com/71966352/144638915-6a9fe54c-e2b8-450c-b8b7-55ccf938f681.png)

Диспечер задач:

![image](https://user-images.githubusercontent.com/71966352/144638355-0a746f22-bb5d-45cf-807e-45063dc6dc6a.png)

* 10 воркеров:

Время выполнения:

![pycharm64_0f3SygPHWP](https://user-images.githubusercontent.com/71966352/144639238-0a03e0b9-599a-4d51-b205-2f4a0a3ab516.png)

Диспечер задач:

![image](https://user-images.githubusercontent.com/71966352/144639176-449f6c6a-9966-4c99-85e5-a4be4db0af9a.png)

* 100 воркеров:

![pycharm64_bdHU9J1ppN5](https://user-images.githubusercontent.com/71966352/144639547-e7c8add8-f8f7-4e0e-b6ee-df2d8b04d350.png)
