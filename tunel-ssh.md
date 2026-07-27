# Túnel SSH

Durante el curso de Security & Ethical Hacking: Attacking the Network de university of Colorado Boulder, aprendí a como abrir y establecer un túnel SSH

Primero de todo me asegure de tener el servicio SSH instalado y activo en la maquina virtual:

```bash
sudo apt update
sudo apt install openssh-server
sudo systemctl enable ssh
sudo systemctl start ssh
```

Después verifique si estaba corriendo:

```bash
sudo systemctl status ssh
```

Primer paso:

```bash
python3 -m http.server 8080
```

Segundo paso:

```bash
Ifconfig
```

Como esta práctica la ejecute en la misma máquina virtual utilice para establecer el túnel SSH con reenvío local "-L"

Esto es lo ejecuté:

```bash
ssh -L 9090:localhost:8080 usuario@192.168.1.100
```

Esto redirige el puerto local 9090 a la máquina virtual en el puerto 8080.

El resultado:

![Resultado del túnel SSH](images/tunel-ssh-resultado.png)
