---
title: "Guía de Nmap"
date: 2026-03-31
draft: false
tags: ["nmap", "networking", "hacking"]
categories: ["reconocimiento"]
---

Nmap (Network Mapper) es una herramienta de código abierto utilizada para el escaneo de redes y auditoría de seguridad.

Permite descubrir:

hosts activos
puertos abiertos
servicios corriendo
posibles vulnerabilidades

Se usa muchísimo en:

pentesting
administración de redes
ciberseguridad ofensiva


---------------------------

## Como usarlo??

La estructura es la siguiente:

```bash
nmap [tipo escaneo] [filtros/Especificaciones] [IP víctima]
```
Por ejemplo,
```bash
nmap -sS -p- -T4 10.10.10.10
```
- -sS = escaneo general
- -p- = que se escaneen todos lo puertos
- -T4 = que se haga a velocidad intermedia


## Tipos de escaneo

Los tipos de escaneo determinan lo que quieres conseguir a través del escaneo, aquí los más importantes:

- -sS = un escaneo general, el más común.

- -sT = lo mismo pero con conexión completa. Es muy detectable

- -sU = un escaneo UDP, bastante lento

- -sA = detectar firewall y ver puertos filtrados

- -sV = te específica las versiones

- -sC = ejecuta scripts automaticos

- -O = para detectar el sistema operativo 

- -A = los ejecuta todos

## Filtros / Especificaciones

Aquí especificamos las cosas que queremos escanear y como hacerlo:

- Puertos:
    - -p [puerto] (aquí específicas los puertos que quieres escanear, si quieres más de un puerto los separas por coma)

    - -p-  (hace que escanee todos los puertos

- Velocidad:

    - -T0 = Lento pero casi indetectable
    - -T4 = El punto intermedio 
    - -T5 = Muy agresivo y detectable


