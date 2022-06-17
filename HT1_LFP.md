# HOJA DE TRABAJO 1
* UNIVERSIDAD DE SAN CARLOS DE GUATEMALA 
* Laboratorio de Lenguajes Formales de Programación 
* Linda Madelin Fabiola Quelex Sep
* 201403745


# Código fuente

```
#HOJA DE TRABAJO 1
import re

class HojaTrabajo1_LFP():

    def __init__(self):
        pass
        # Email Facultad de Ingeniería
    def Email_ingenieria(self,entradas:str):
        input_email=entradas
        serch_email_ingenieria= re.findall(r"([0-9]{13}@ingenieria.usac.edu.gt)",input_email, flags=re.IGNORECASE)
        if len(serch_email_ingenieria)>0:
            print('Correo válido-------------->', serch_email_ingenieria)
        else:
            print('Correo no válido-------------->', input_email)

        #Un título de Marckdown
    def Título_markdown(self,entradas):
        input_titulo_markdown=entradas
        serch_titulo_markdown= re.findall(r"([#]{1,6}[a-zA-Z0-9-]+)",input_titulo_markdown, flags=re.IGNORECASE)
        if len(serch_titulo_markdown)>0:
            print('Título válido-------------->', serch_titulo_markdown)
        else:
            print('Título no válido-------------->', input_titulo_markdown)

        #Un URL
    def URL(self,entradas):
        input_url=entradas
        serch_url= re.findall(r"((http|https):\/\/(\w+:{0,1}\w*@)?(\S+)(:[0-9]+)?(\/|\/([\w#!:.?+=&%@!\-\/]))?)",input_url, flags=re.IGNORECASE)
        if len(serch_url)>0:
            print('URL válido-------------->', serch_url)
        else:
            print('URL no válido-------------->',  input_url)

        #Una oración de 5 palabras
    def Oracion(self,entradas):
        input_oracion=entradas
        serch_oracion= re.findall(r"(([\w]+[ ]){4}([\w]+[ ]*))",input_oracion, flags=re.IGNORECASE)
        if len(serch_oracion)>0:
            print('Oración válida-------------->', serch_oracion)
        else:
            print('ORación no válida-------------->', input_oracion)

prueba=HojaTrabajo1_LFP()

prueba_uno="1234567891236@ingenieria.usac.edu.gt"
prueba_dos="236@ingenieria.usac.edu.gt"
prueba_tres="1234567891236@ingenieria.usac"
prueba_cuatro="1111111111111@ingenieria.usac.edu.gt"
print('\n','PRUEBAS EMAIL INGENIERÍA')
print('**********************************************', '\n')
prueba.Email_ingenieria(prueba_uno)
prueba.Email_ingenieria(prueba_dos)
prueba.Email_ingenieria(prueba_tres)
prueba.Email_ingenieria(prueba_cuatro)
print('\n')

prueba_1="#TÍTULO1"
prueba_2="##TÍTULO 4"
prueba_3="123"
prueba_4="######OTRO"
print('\n','PRUEBAS TÍTULO MARKDOWN')
print('**********************************************', '\n')
prueba.Título_markdown(prueba_1)
prueba.Título_markdown(prueba_2)
prueba.Título_markdown(prueba_3)
prueba.Título_markdown(prueba_4)
print('\n')

prueba1="https://regex101.com/"
prueba2="##TÍTULO 4"
prueba3="123"
prueba4="https://uedi.ingenieria.usac.edu.gt/campus/mod/assign/view.php?id=282576"
print('\n','PRUEBAS URL')
print('**********************************************', '\n')
prueba.URL(prueba1)
prueba.URL(prueba2)
prueba.URL(prueba3)
prueba.URL(prueba4)
print('\n')

p1="uno dos tres cuatro cinco"
p2="cinco cuatro tres dos uno"
p3="789"
p4="había una vez"
print('\n','PRUEBAS ORACIONES')
print('**********************************************', '\n')
prueba.Oracion(p1)
prueba.Oracion(p2)
prueba.Oracion(p3)
prueba.Oracion(p4)
print('\n')

```

# Salidas 

 A continuación se presenta la salida de las pruebas del código.


<p>Detalle</p>
<p><img src="HT1_LFP\SALIDA1.png" /></p>
<p>Continuación</p>
<p><img src="HT1_LFP\SALIDA2.png" /></p>

