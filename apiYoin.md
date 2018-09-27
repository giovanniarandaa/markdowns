# Units

## Units

Return units

### /getUnits

**Method:** GET

**Parameters** Empty

**Return**

```json
{
    "success" : true,
    "message" : "completed",
    "items":{
        {
            "id": "dshaoidh18724141",
            "builiding": "Nombre del edificio",
            "unit": "0001",
            "residents": {
                "name": "Nombre Apellido",
                "id": "120429041hjfkahsda",
                "image": "imagen.jpg"
            },
            "phone": "55 58 64 78 25",
            "propietario": "Nombre Apellido",
            "email": "example@mail.com",
            "pets": {
                "name": "Nombre",
                "image": "imagen.jpg",
                "id": "4920j1209re12"
            }
        },
        {
            "id": "dshaoidh18724141",
            "builiding": "Nombre del edificio",
            "unit": "0001",
            "residents": {
                "name": "Nombre Apellido",
                "id": "120429041hjfkahsda",
                "image": "imagen.jpg"
            },
            "phone": "55 58 64 78 25",
            "propietario": "Nombre Apellido",
            "email": "example@mail.com",
            "pets": {
                "name": "Nombre",
                "image": "imagen.jpg",
                "id": "4920j1209re12"
            }
        }
    }
}
```

## Add unit

Add unit

### /addUnit

**Method:** POST

**Parameters** 

```http
    building_name: String
    unit_name: String
    phone: String
    parking_place: String
    bici_place: String
    fields: Array

    fields => {
        name: String
        value: String (optional)
        required: Bool
        visible: Bool 
    }
````

**Return**
```json
{
    "success" : true,
    "message" : "completed"
}
```

## Edit unit

Edit unit

### /editUnit

**Method:** PUT

**Parameters** 

```http
    building_name: String
    unit_name: String
    phone: String
    parking_place: String
    bici_place: String
    fields: Array

    fields => {
        name: String
        value: String (optional)
        required: Bool
        visible: Bool 
    }
```
**Return**

```json
{
    "success" : true,
    "message" : "completed"
}
```

## Detail unit

Detail unit

### /detailUnit

**Method:** GET

**Parameters**

```http
    unit_id: String
```

**Return**

```json
{
    "success": true,
    "message": "completed",
    "item":{
        "id": "dshaoidh18724141",
        "builiding": "Nombre del edificio",
        "unit": "0001",
        "residents": {
            "name": "Nombre Apellido",
            "id": "120429041hjfkahsda",
            "image": "imagen.jpg"
        },
        "phone": "55 58 64 78 25",
        "propietario": "Nombre Apellido",
        "email": "example@mail.com",
        "pets": {
            "name": "Nombre",
            "image": "imagen.jpg",
            "id": "4920j1209re12"
        },
        "fields":{
            {
                "name": "Nombre",
                "value": "Valor",
                "required": true,
                "visible": false 
            },
            {
                "name": "Nombre",
                "value": "Valor",
                "required": true,
                "visible": false 
            },
            {
                "name": "Nombre",
                "value": "Valor",
                "required": true,
                "visible": false 
            }
            
        }
    }
}
```

## Add resident to unit

Add resident to unit

### /addResidentUnit

**Method:** POST

**Parameters:** 

```http
    unit_id: String
    rol_type: int (1 = Principal, 2 = Residente)
    image: Array (Format image)
    name: String
    lastname: String
    birthdate: date(YYYY/MM/DD)
    gender: int (1 = male, 2 = female) or string (male and female)
    email: String
    phone: String
    mobile: String
```

**Return** 

```json
{
    "success" : true,
    "message" : "completed"
}
```

## Add pet to unit

Add pet to unit

### /addPetUnit

**Method:** POST

**Parameters**

```http
    unit_id:String
    image: Array (Format Image)
    name: String
    pet_type: int (1 = cat, 2= dog, 3 = other)
```

**Return** 

```json
{
    "success" : true,
    "message" : "completed"
}
```
