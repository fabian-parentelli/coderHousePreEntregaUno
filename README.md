// ****** productos ******* ///

Existen 4 tipos de productos con los siguentes ID 1 -2 - 3 - 6.

get => Lista todos los productos o o la cantidad de productos deceados.
    Ejemplo con 2 productos.
    localhost:8080/api/products?limit=2

get/:pid => trae el prúdcto con el Id seleccionado.
    Ejemplo producto con Id 1.
    localhost:8080/api/products/1

Post => Agrega productos con distintos campos. 
    Ejemplo producto de prueba. (price es un string para que posteriormente se tranforme en un number.)
    localhost:8080/api/products
    {
        "title": "Bolígrafo",
        "description": "Azul y Rojo",
        "code": "ab53568",
        "price": "100",
        "stock": 30,
        "category": "Secundaria",
        "thumbnails": "http//:imagen-Boligrafo",
    }

Put/:pid => Actualizar un producto. 
    Ejemplo con el producto numero 2 (le agrego un id aunque que no se pueda modificar)
    localhost:8080/api/products/2
    {
		"title": "Hojas A4 700gr",
		"id": 38
	}

Delete/:pid => Eliminar u n producto por su ID
    Ejemplo producto numer 3
    localhost:8080/api/products/3


// ****** Carrito ******* ///

Post => Agregar un carrito con un arrau de productos en su interior y un id autogenerado.
    Dejo uno creado para que gitHub lo suba, tengo entendio que si lo mando vacío gitHub no lo sube.
    localhost:8080/api/carts

GET/:cid => lista los productos que pertenezcan al carrito con el parámetro cid proporcionados.
    Ejemplo el carrito numero 1
    localhost:8080/api/carts/1

POST/:cid/product/:pid => Agrega el producto al arreglo “products” del carrito seleccionado, 
agregándose como un objeto.
    Ejemplo carrito 1 producto 1.
    localhost:8080/api/carts/1/product/1
