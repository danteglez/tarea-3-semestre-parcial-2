# NOTAS DE CLASES DE LA SEGUNDA PARCIAL  
---
#### ALUMNO: DANTE GONZALEZ 
---
#### MAESTRO: WALTER MATA
---
###### CARRERA: COMPUTACION INTELIGENTE (ICI)
---
Primer nota de clases que tuve fue la introduccion de guizero de python.
Guizero es una libreria de python que ayuda al desarroyo de aplicaciones.
En el salon solo hicimos una aplicacion paso a paso.
---
Esta es la primera nota, es algo demaciado basico pues solo creamos la ventana y con el nombre de "ICI app ",
el app.display() es muy importante por que sin el no se podria ver el programa
```python
from guizero import App

app= App(title="ICI app")
app.display()
```
---
Este es el segundo programa, lo unico nuevo con diferencia al primero es que solo agregamos una linea de texto con el nombre de "Welcome to ICI app" y tambien un boton pero sin ninguna funcion
```python
from guizero import App, Text, PushButton

app= App(title="ICI App")
message= Text(app, text="Welcome to ICI App!")
button= PushButton(app, text="click me")
app.display()
``` 
---
En esta siguiente solo agregamos una funcion al boton con la palabra reservada "def", cada que es precionado pone el siguiente mensaje "ICI Rocks"

``` python
from guizero import App, Text, PushButton

def say_hello():
    message2.value = "ICI Rocks"  # con .value le damos la Propiedad del widget
```
---
En el siguiente creamos un programa muy sencillo que solo pregunta tu nombre y cuando precionas el boton te responde con un "hola (tu nombre)", tambien podemos modificar el tamaño de los cuadrados de texto que aparecen y modificar sus colores y tamaños
``` python
from guizero import App, Text, PushButton, TextBox

def say_hello():
    mensaje_2.value = 'hola ' + nombre.value

app = App(title= 'ICI app')
mensaje=Text(app,text='Como te llamas?',color="red")
nombre=TextBox(app, width=10, height=5,multiline=True)
boton=PushButton(app,text='preciona aqui c:',command=say_hello)
mensaje_2=Text(app)
app.display()
```
---
Y por ultimo, es casi el mismo que el otro solo que este es una calculadora que solo suma, solo cambie pocas cosas para que funcionara
``` python
from guizero import App, Text, PushButton, TextBox

def resultado():
   mensaje_2.value= int(num_1.value) + int(num_2.value)
    
app = App(title="Suma")
mensaje = Text(app, text="ingrese dos numeros ")
num_1=TextBox(app)
num_2=TextBox(app)
boton= PushButton(app,text="preciona para ver el resultado",command=resultado)
mensaje_2=Text(app)
app.display() 
```
---
Y uno extra para mi si luego reviso esto:
para agregar una imagen debemos de usar la palabra picture, debemos tener descargado la imagen y para ponerla debemos de poner "image=r()la ubicacion de la imagen", la letra r es muy importante no se por que pero lo es
``` python
from guizero import App, picture
foto = Picture(app, image=r"c:\Users\dante\OneDrive\Escritorio\gallo.gif",width=50,height=50)
app.display()
```
