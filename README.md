# nestjs_postgresql_example
Microservicio hecho en NestJS con conexion a postgresql utilizando TypeORM

## Configuracion de variables de entorno
`yarn add @nestjs/config`

`npm i @nestjs/config`

## app.module.ts
```js
import { Module } from '@nestjs/common';
import { ConfigModule } from '@nestjs/config';
@Module({
 imports: [ConfigModule.forRoot()],
})
export class AppModule {}
```

## Instalar TypeORM y driver Postgres
 yarn add @nestjs/typeorm typeorm pg

## Proyecto de ejemplo PostgreSQL
https://github.com/Klerith/nest-teslo-shop/tree/fin-seccion-10

## Proyecto de ejemplo MongoDB
https://github.com/Klerith/nest-pokedex/tree/fin-seccion-7

## Documentacion de NestJS
https://docs.nestjs.com/techniques/database

## Documentacion de TypeORM

## Comandos basicos de NestJS

```js
//Instalar Nest.js CLI:
npm i -g @nestjs/cli

//Nuevo prroyecto:
nest new project-name

//Comandos útiles del CLI
nest generate <comando>
nest g <comando>

//Mostrar ayuda: 
nest -h
nest g -h
nest g s nombre -h

```
## Componentes comunes:
```js
//Crear una clase
nest g cl <path/nombre>

//Crear un controlador
nest g co <path/nombre>

//Crear un decorador
nest g d <path/nombre>

//Crear un guard
nest g gu <path/nombre>

//Crear un interceptor
nest g in <path/nombre>

//Crear un módulo
nest g mo <path/nombre>

//Crear un pipe
nest g pi <path/nombre>

//Crear un servicio
nest g s <path/nombre>

//Crear un recurso completo
nest g resource <nombre>

```

## Pipes integrados por defecto
```
ValidationPipe ParseIntPipe
ParseBoolPipe ParseArrayPipe
ParseFloatPipe ParseUUIDPipe
```

## Convertir :id del segmento a entero
```js
@Get(':id')
async findOne(
@Param('id', ParseIntPipe) id: number
){
  return this.catsService.findOne(id);
}
```

## Librerías externas útiles:
`yarn add class-validator class-transformer`

