# Authentication Project

Este proyecto es una aplicación creada con Ionic y Firebase que permite a los usuarios registrarse, autenticarse y subir imágenes de perfil a Firebase Storage. La guía cubre desde la configuración inicial hasta la compilación de una APK para Android.

## Características
- Registro y autenticación de usuarios utilizando Firebase Authentication (correo y contraseña).
- Carga de imágenes a Firebase Storage con previsualización de la imagen de perfil.
- Generación de APK para distribución en dispositivos Android.

## Requisitos
- Node.js
- Ionic
- Firebase Console para la configuracióin de Firebase
- JDK (para crear el APK en Android)
- Android Studio (para compilar el APK)

## Creación de la aplicación
#### 1. Creación del Proyecto Ionic
Ejecuta el siguiente comando para crear un nuevo proyecto ionic: 
- `ionic start firebase-auth-upload blank --type=angular`
- `cd firebase-auth-upload`

#### 2. Configurar Firebase
- Ve a la Consola de Firebase y crea un nuevo proyecto. 
- Agrega una aplicación web en la sección de "Project Settings" para obtener el archivo de configuración. 
- Activa Firebase Authentication (correo y contraseña). 
- Crea un Bucket de almacenamiento en Firebase Storage y configura las reglas para permitir la carga de archivos autenticados. 

#### 3. Configuración de Firebase a Ionic
Instala Firebase y AngularFire:
`npm install firebase @angular/fire`

En `src/environments/environment.ts`, agrega tu configuración de Firebase

#### 4. Implementar Registro y autenticación
- Crea un servicio de autenticación `auth.service.ts` para manejar el registro, inicio de sesión y cierre de sesión utilizando Firebase Authentication.
- Agrega métodos en el servicio para registrar e iniciar sesión con correo y contraseña.

#### 5. Crear Funcionalidad de Carga de imágenes
- Crea una página de perfil `ProfilePage` donde los usuarios puedan subir su imagen de perfil.
- Usa `AngularFireStorage` en tu servicio para cargar la imagen al Bucket de Firebase Storage y guardar el enlace de descarga en la base de datos de Firebase.

#### 6. Probar la aplicación
Ejecuta el siguiente comando para iniciar la aplicación en el navegador y verificar que el registro, autenticación y carga de imágenes funcionen correctamente:
`ionic serve`

## APK para Android
Para generar el apk es necesario agregar las variables de entorno en el archivo `enviroment.prod.ts` una vez realizada seguir los comandos a continuación: 

Comandos necesarios para generar el apk. Ejecutarlos en el orden establecido: 
- `ionic capacitor add android`
- `ionic build`
- `npx cap copy android`
- `npx cap sync android`
- `npx cap open android`

Carpeta donde encontrar el apk: 
./APK Generada

# Evidencias
### Web
![image](https://github.com/user-attachments/assets/474ed15c-c876-417c-bbfc-10df01c7b382)
![image](https://github.com/user-attachments/assets/4da7cfd5-44da-4335-997c-4e0153db7e5e)

### Móvil
![image](https://github.com/user-attachments/assets/d8bfe92a-ec85-48c5-ad6f-5271be25aa65)
![image](https://github.com/user-attachments/assets/5ac70aaa-806b-4d7a-a8be-3a2e1afc669b)

# Aportes por Estudiante
Los aportes establecidos por cada uno de los estudiantes se realizaron en commits, en el caso de Steven Castillo los commits realizados
por parte de él son superiores ya que en clase unicamente su computador tenia internet para realizar el proyecto.

## Recursos
- https://devdactic.com/ionic-firebase-auth-upload
- https://firebase.google.com/docs
