# Metasploitable2 – Enumeración

## 🧪 Entorno
- Máquina objetivo: Metasploitable2
- Tipo: Laboratorio vulnerable
- Sistema operativo: Linux
- Atacante: Kali Linux
- Red: Local / NAT / Host-only

---

## 🎯 Objetivo
Identificar hosts, servicios activos y posibles vectores de ataque
mediante técnicas de enumeración de red y servicios.

---

## 🔍 Reconocimiento de red

### Escaneo inicial
```bash
nmap -sn 192.168.0.161
---
Este comando realiza un escaneo de descubrimiento de hosts dentro del rango de red 192.168.161.0/24, con el objetivo de identificar qué dispositivos están activos sin analizar puertos ni servicios.
La opción -sn (scan no port) indica a Nmap que no realice escaneo de puertos, limitándose a enviar paquetes de descubrimiento (ICMP, ARP o TCP) para detectar hosts vivos.
🎯 Uso en pentesting
Se utiliza como primer paso de reconocimiento, permitiendo conocer qué hosts están disponibles en la red antes de continuar con una enumeración más profunda.

---
### Resultado

~ $ nmap -sn 192.168.0.161
Starting Nmap 7.98 ( https://nmap.org ) at 2026-01-02 02:07 -0600
Nmap scan report for 192.168.0.161
Host is up (0.035s latency).
Nmap done: 1 IP address (1 host up) scanned in 0.56 seconds

 

