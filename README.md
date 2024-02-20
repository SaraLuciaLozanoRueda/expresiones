# EXPRESIONES REGULARES

**1.**

```
const PATRON=/^\d{1,2}\.\d{3}\.\d{3}-\d{1}$/;
nit=prompt('Ingrese el nit para su empresa')
if (PATRON.test(nit)){
    console.log('El nit es valido');
}else{
    console.log('Nit invalido...');
}
```

La d significa que dentro de la cadena hay dígitos,luego hay dos \ (que representa un espacio) divididos por un punto .

**2.**

```
const PATRON=/^\d{5}$/;
correo=prompt('Ingresa tu correo postal');
if (PATRON.test(correo)){
    console.log('Correo postal valido')
}else{
    console.log('Formato de correo incorrecto')
}
```

Aquí significa que solo recibe dígitos y no mas de 5.

**3.**



```
let PATRONUS=/^[a-z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
let email=prompt('Ingrese su correo');
if (PATRONUS.test(email)){
    console.log('Correo electronico valido');
}else{
    console.log('Correo electronico invalido')
}
```

Con uso de ternario.

```
let PATRONUS=/^[a-z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
let email=prompt('Ingrese su correo');
console.log(PATRONUS.test(email)?'Correo electronico valido':'Correo electronico invalido')
```

le permite minúsculas,números,caracteres especiales y luego del @ mas mayúsculas,minúsculas,números,punto y guion y después un punto y la siguiente cadena debe contener mínimo dos números.

**4.**

```
let patron=/^\(\d{3}\) \d{3}-\d{4}$/;
numero=prompt('Ingrese su numero de telefono');
console.log(patron.test(numero)?'Numero de telefono verificado correctamente':'El formato no coincide')
```

**5.**

```
let patronus=/^https?:\/\/.*/;
let web=prompt('Ingrese el navegador al que quiere ingresar');
console.log(patronus.test(web)? 'Buscando web':'Web no encotrada')
```

cuando le ponemos el ? significa que el s puede estar o no estar

**6.**

```
let us= /^[a-z0-9]{3,10}$/;
usuario=prompt('Ingrese su nombre de usuario');
console.log(us.test(usuario)? 'El nombre de usuario es valido':'Este nombre de usuario no es valido')
```

**7.**

```
let verificador=/^(\d{1,3}\.){3}\d{1,3}$/;
let ip=prompt('Ingresa la direccion IP');
console.log(verificador.test(ip)?'IP valida':'IP invalida')
```

**8.**

```
let ejemplo=/^((0[1-9]|1[0-2])\/(0[1-9]|[1-2][0-9]|3[0-1])\/\d{4})$/;
let fecha=prompt('Ingresa la fecha');
console.log(ejemplo.test(fecha)?'Formato correcto':'Formato incorrecto')
```

**9.**

```
let con = /^(?=.[a-z])(?=.[A-Z])(?=.\d)(?=.[!@#$%^&*()_+.]).{8,}$/;
let password =prompt('Ingresa tu contraseña para verificar si es:');
console.log(con.test(password) ? "Contraseña segura" : "Contraseña insegura");
```

