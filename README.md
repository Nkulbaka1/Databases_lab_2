# LAB_2
1. Дана схема базы данных в виде следующих отношений. С помощью операторов SQL создать
логическую структуру соответствующих таблиц для хранения в СУБД, используя известные средства
поддержания целостности (NOT NULL, UNIQUE, и т.д.). Обосновать выбор типов данных и
используемые средства поддержания целостности. При выборе подходящих типов данных
использовать информацию о конкретных значениях полей БД (см. прил.1)
~~~SQL
CREATE TABLE АВТОМОБИЛЬ
(
	ИДЕНТИФИКАТОР SERIAL PRIMARY KEY,
	МАРКА VARCHAR(50) NOT NULL,
	"АТП-ВЛАДЕЛЕЦ" VARCHAR(50) NOT NULL,
	СКИДКА SMALLINT NOT NULL
);

CREATE TABLE ГАРАЖ
(
	ИДЕНТИФИКАТОР SERIAL PRIMARY KEY,
	НОМЕР INT NOT NULL,
	РАСПОЛОЖЕНИЕ VARCHAR(50) NOT NULL,
	КОМИССИОННЫЕ SMALLINT NOT NULL
);

CREATE TABLE ДЕТАЛИ
(
	ИДЕНТИФИКАТОР SERIAL PRIMARY KEY,
	ДЕТАЛЬ VARCHAR(50) NOT NULL,
	ПРОДАВЕЦ VARCHAR(50) NOT NULL,
	"СТОИМОСТЬ, РУБ" INT NOT NULL,
	"МАКС. КОЛ-ВО" INT NOT NULL
);

CREATE TABLE РЕМОНТ
(
	ИДЕНТИФИКАТОР SERIAL PRIMARY KEY,
	ДЕТАЛЬ VARCHAR(50) NOT NULL,
	ПРОДАВЕЦ VARCHAR(50) NOT NULL,
	"СТОИМОСТЬ, РУБ" INT NOT NULL,
	"МАКС. КОЛ-ВО" INT NOT NULL
);
~~~
