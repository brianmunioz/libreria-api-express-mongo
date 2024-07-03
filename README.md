### Introducción
Esta api es una api sencilla para sistema interno de ventas de libros, hecha para que pequeños vendedores puedan controlar ventas y stock.

### Arquitectura y Tecnologías Utilizadas
Esta API sigue la arquitectura en N capas. A continuación, se detallan las tecnologías utilizadas:
- **bcrypt**: ^5.1.1
- **dotenv**: ^16.4.5
- **express**: ^4.19.2
- **jsonwebtoken**: ^9.0.2
- **mongoose**: ^7.7.0
- **nodemon**: ^3.1.4

### Modelo de Entidad-Relación

[![entidad-relacion](https://raw.githubusercontent.com/brianmunioz/libreria-api-express-mongo/master/documentation/book-store.drawio.png "entidad-relacion")](https://raw.githubusercontent.com/brianmunioz/libreria-api-express-mongo/master/documentation/book-store.drawio.png "entidad-relacion")

### Rutas de api



#### Obtener todos los libros

```http
  GET /getBooks
```

| Parámetro | Tipo de dato     | Nota                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Requerido via headers** |

#### Obtener todos los libros en el carrito

```http
  GET /getCart
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Requerido via headers** |

#### Registro

```http
  POST /signup
```

| Parámetro | Tipo de dato     | Nota                |
| :-------- | :------- | :------------------------- |
| `username` | `string` | **Requerido** |
| `password` | `string` | **Requerido** |

#### Iniciar sesión

```http
  POST /login
```

| Parámetro | Tipo de dato     | Nota                |
| :-------- | :------- | :------------------------- |
| `username` | `string` | **Requerido** |
| `password` | `string` | **Requerido** |

#### Agregar libro al stock

```http
  POST /addBook
```

| Parámetro | Tipo de dato     | Nota                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Requerido via headers** |

#### Agregar libro al carrito

```http
  POST /addBookToCart
```

| Parámetro | Tipo de dato     | Nota                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Requerido via headers** |

#### Cerrar sesión

```http
  DELETE /logout
```

| Parámetro | Tipo de dato     | Nota                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Requerido via headers** |

#### Cerrar sesión

```http
  DELETE /removeCart/:cartId
```

| Parámetro | Tipo de dato     | Nota                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Requerido via headers** |
| `cartId` | `string` | **Requerido via parámetro** |








## Correrlo api en local

Instalar dependencias

```bash
  npm install
```

Configuren su acceso a mongo en local y corranlo con el siguiente comando (nodemon)

```bash
  npm run dev
```

