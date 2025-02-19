# 📌 API REST de Productos con ASP.NET Core

Este proyecto es una API REST desarrollada en *ASP.NET Core* que permite realizar operaciones CRUD sobre productos almacenados en una base de datos *SQL Server*.  

## 🚀 Características  
✅ CRUD de productos (Crear, Leer, Actualizar y Eliminar).  
✅ Uso de *Entity Framework Core* como ORM.  
✅ Implementación del *patrón Repository*.  
✅ Documentación interactiva con *Swagger*.  
✅ Arquitectura modular y escalable.  

---

## 🛠️ Tecnologías utilizadas  
- *ASP.NET Core 8*  
- *Entity Framework Core*  
- *SQL Server*  
- *Swagger (Swashbuckle)*  

---

## 📂 Estructura del Proyecto  


📦 WebApiProductos  
 ┣ 📂 Controllers  
 ┃ ┗ 📜 ProductosController.cs  
 ┣ 📂 Models  
 ┃ ┗ 📜 Producto.cs  
 ┣ 📂 Data  
 ┃ ┗ 📜 ApplicationDbContext.cs  
 ┣ 📂 Repositories  
 ┃ ┣ 📜 IProductoRepository.cs  
 ┃ ┗ 📜 ProductoRepository.cs  
 ┣ 📜 appsettings.json  
 ┣ 📜 Program.cs  
 ┗ 📜 README.md  


---

## ⚙️ Configuración e instalación  

### 1️⃣ *Clonar el repositorio*  
sh
git clone https://github.com/bryan-br0n/APIv2.git
cd WebApiProductos


### 2️⃣ *Configurar la base de datos*  
1. Instalar *SQL Server* y *SQL Server Management Studio (SSMS)*.  
2. Crear una base de datos llamada ProductosDB.  
3. Configurar la cadena de conexión en appsettings.json:  
   json
   "ConnectionStrings": {
     "DefaultConnection": "Server=TU_SERVIDOR;Database=ProductosDB;Trusted_Connection=True;TrustServerCertificate=True;"
   }
   
   📌 *Reemplaza TU_SERVIDOR por el nombre de tu servidor SQL Server*.

### 3️⃣ *Instalar dependencias*  
Ejecuta en la terminal:  
sh
dotnet restore


### 4️⃣ *Ejecutar migraciones y actualizar la base de datos*  
sh
dotnet ef migrations add InitialCreate
dotnet ef database update


### 5️⃣ *Ejecutar la API*  
sh
dotnet run


### 6️⃣ *Abrir Swagger y probar la API*  
Una vez ejecutado el proyecto, abre tu navegador en:  

https://localhost:5001/swagger


---

## 📝 Endpoints  

### 🔹 *Obtener todos los productos*  
GET /api/productos  
📌 *Respuesta*  
json
[
  {
    "id": 1,
    "nombre": "Laptop",
    "precio": 1500.99,
    "stock": 10
  }
]


### 🔹 *Obtener un producto por ID*  
GET /api/productos/{id}  

### 🔹 *Crear un nuevo producto*  
POST /api/productos  
📌 *Cuerpo de la solicitud*  
json
{
  "nombre": "Smartphone",
  "precio": 899.99,
  "stock": 5
}


### 🔹 *Actualizar un producto*  
PUT /api/productos/{id}  

### 🔹 *Eliminar un producto*  
DELETE /api/productos/{id}  

## Link del Drive para ver Video: https://drive.google.com/drive/folders/1kpW87g8Dl9WNlPxJYxAFERnjTdj31R0O?usp=sharing
