# Container sem Docker(chroot, namespace, cgroups)

## namespace

- Quando falamos de namespace estamos nos referindo a um isolamento a nivel de
  processo, que é basicamente isolar

onde os arquivos vão rodar no sistema, fazendo com que alguns processo não se misturem com o sistema padrão.

## chroot

- Diferente do namespace, quando usamos o chroot estamos definindo um diretório e sinalizando para o sistema que
  é a partir dele que vamos ter acesso, pois sem essa flag um namespace tem acesso total aos arquivos que temos no
  sistema original, que é exatamente o que não queremos com um cointainer

## cgroups

- Permite separar os recursos de hardwares do seu pc.

## Conclusão

- Sozinhos esses processos não fazem tanto sentido, mas quando usados completamente temos todas as
  caracteristicas de um container, um ambiente isolado que não compartilha processos e recursos com o
  resto do ambiente padrão da maquina.
- O docker automatiza muito esse processo para a gente, mas é sim possivel trabalhar com containers
  em sua maneira mais "rudimentar".

# LXC & LXD

- Ferramentas que facilitam o uso de containers com abistrações que lembram muito o mais baixo nivel de container no linux

# Container X Imagem

- Container é o ambiente separado que executamos as aplicações

- Imagem é a base para esse container

- Imagem é a receita de bolo e o container é um bolo

# Arquitetura do Docker

## Docker Daemon

- Responsavel por gerenciar os objetos do docker(Container / Images / Network / Volumes)

- Antigo modelo de interação do docker

![png antigo modelo de interação](../../../../../assets/2024-05-22-10-26-25.png)

- Novo modelo de interação do docker

## Docker Host

- Maquina responsavel por hospedar o docker deamon

## Docker client

- É a asbstração que se comunica com o docker daemon

## Docker Registry

- Github do docker
