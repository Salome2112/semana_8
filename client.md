![Captura de pantalla 2024-05-27 095520](https://github.com/Salome2112/semana_8/assets/146013347/69f9109c-e22c-4b9b-99eb-38d104ce351e)#Tarea en clase semana 8

##La funcion count

###Creacion de la tabla 
```
CREATE TABLA IF NOT EXIST client(
id SERIAL,
nui VARCHAR (10)NOT NULL,
fullname VARCHAR (100) NOT NULL
phone VARCHAR (10),
type_of_client VARCHAR (50) DEFAULT 'BASIC'
city VARCHAR(50),
credit_limit DECIMAL(7,2)
);
```


###Insercion de datos 
 
```
INSERT INTO client (nui, fullname, phone, type_of_client, city, credit_limit)
 VALUES
('1234567890', 'Juan Pérez', '5551234567', 'PREMIUM', 'Ciudad de México', 10000.00),
('0987654321', 'María López', '5557654321', 'BASIC', 'Guadalajara', 5000.00),
('1122334455', 'Carlos Hernández', '5558765432', 'GOLD', 'Monterrey', 15000.00),
('2233445566', 'Ana González', '5552345678', 'BASIC', 'Puebla', 3000.00),
('3344556677', 'Luis Martínez', '5553456789', 'SILVER', 'Cancún', 7000.00),
('4455667788', 'Marta Sánchez', '5554567890', 'PREMIUM', 'Mérida', 20000.00),
('5566778899', 'José Ramírez', '5555678901', 'BASIC', 'Toluca', 4000.00),
('6677889900', 'Elena Torres', '5556789012', 'GOLD', 'Querétaro', 12000.00),
('7788990011', 'Rafael Castillo', '5557890123', 'BASIC', 'Tijuana', 6000.00),
('8899001122', 'Lucía Romero', '5558901234', 'SILVER', 'León', 8000.00);
```
```
INSERT INTO client (nui, fullname, phone, type_of_client, city, credit_limit) 
VALUES
('9988776655', 'Pedro González', NULL, 'BASIC', 'Chihuahua', 5000.00),
('8877665544', 'Laura Fernández', NULL, 'PREMIUM', 'Zacatecas', 12000.00),
('7766554433', 'Sofía Morales', NULL, 'GOLD', 'Aguascalientes', 10000.00),
('6655443322', 'Miguel Rojas', NULL, 'BASIC', 'Hermosillo', 4500.00),
('5544332211', 'Paula Vega', NULL, 'SILVER', 'Oaxaca', 7500.00);
```
### Mostrar el nombre de los datos.
Para mostrar el total de nombres la funcion COUNT () ** pasalandolole como parametro  el campo en este caos "fullname"
```
SELECT COUNT(fullname) AS total_nombres 
FROM client;
```
###Mostrar capturas 
![Captura de pantalla 2024-05-27 094757](https://github.com/Salome2112/semana_8/assets/146013347/a14b33f8-25dc-4850-8795-e0eeb0ed6d20)

### Mostrar el total phone
Para mostrar el total de phone utilizamos  la funcion COUNT **  (phone)
```
SELECT COUNT(phone) AS total_phones
 FROM client;
```
###Mostrar capturas
![Captura de pantalla 2024-05-27 095111](https://github.com/Salome2112/semana_8/assets/146013347/cdc12eb6-47db-42c7-8226-5a636b56fc15)

### Mostrar el total de name y phone.
Para mostrar el total de nombres y phones utilizamos la funcion COUNT ** (phone) (names)
```
SELECT COUNT(fullname) AS total_names, COUNT(phone) AS total_phones
FROM client;
```
###Mostrar capturas 
![Captura de pantalla 2024-05-27 095258](https://github.com/Salome2112/semana_8/assets/146013347/8a334cfe-f05a-4ca2-b483-fb06d054eab1)

### Mostrar el total.
Para mostrar el total  utilizamos la funcion COUNT ** (total)
```
SELECT COUNT(*) AS total
FROM client;
```
###Mostrar capturas 
![Captura de pantalla 2024-05-27 095520](https://github.com/Salome2112/semana_8/assets/146013347/9567e073-debc-4b7d-b7f9-aabbfe21bba2)
### Mostrar el total de cities.
Para mostrar el total  utilizamos la funcion COUNT ** (city)
```
SELECT COUNT(city) AS total_cities
FROM client;
```
###Mostrar capturas 
![Captura de pantalla 2024-05-27 095756](https://github.com/Salome2112/semana_8/assets/146013347/97e2dbfd-6b92-4d60-abef-aafc0ba81fea)

### Mostrar el total de DISTINCT (cities).
Para mostrar el total  utilizamos la funcion DISTINCT (cities).
```
SELECT COUNT(DISTINCT city) AS total_distinct_cities
 FROM client;

```
###Mostrar capturas 
![Captura de pantalla 2024-05-27 100021](https://github.com/Salome2112/semana_8/assets/146013347/1ed48ab9-fb02-42c5-94b5-8bbacba82072)











