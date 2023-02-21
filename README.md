### Infraestrutura como Código: Script de Criação de Estrutura de Usuários, Diretórios e Permissões
<p>Aluna: Mirian Ajiki Molicawa </p>
<p>Digital Innovation One </p>
<p>Instrutor: Denilson Bonatti </p>
<p>Data: 21/02/2023 </p>

--------------------------------------------------------------------------------------------------------------------------------------------------------
### Desafio: 
* Excluir diretórios, arquivos, grupos e usuários criados anteriormente;
* Todo provisionamento deve ser feito em um arquivo do tipo Bash Script
* O dono de todos os diretórios criados será o usuário root
* Todos os usuários terão permissão total dentro do diretório público;
* Os usuários não poderão ter permissão de leitura, escrita e execução em diretórios de departamentos que eles não pertencem.
* Subir arquivo de script criado para sua conta do GitHub

--------------------------------------------------------------------------------------------------------------------------------------------------------

* Exclusão diretórios criados anteriormente:
root@LAPTOP-6BPS8238:/home/ajikisan# rm - RF /adm/
root@LAPTOP-6BPS8238:/home/ajikisan# rm - RF /publica/
root@LAPTOP-6BPS8238:/home/ajikisan# rm - RF /ven/
root@LAPTOP-6BPS8238:/home/ajikisan# ls -l

* Exclusão de usuários criados anteriormente:
root@LAPTOP-6BPS8238:/home/ajikisan# cat /etc/passwd
root@LAPTOP-6BPS8238:/home/ajikisan# userdel --help
Options:
  -f, --force                   force removal of files,
                                even if not owned by user
  -h, --help                    display this help message and exit
  -r, --remove                  remove home directory and mail spool
  -R, --root CHROOT_DIR         directory to chroot into
  -P, --prefix PREFIX_DIR       prefix directory where are located the /etc/* files
      --extrausers              Use the extra users database
  -Z, --selinux-user            remove any SELinux user mapping for the user
root@LAPTOP-6BPS8238:/home/ajikisan# user
root@LAPTOP-6BPS8238:/home/ajikisan# userdel -r maisa
root@LAPTOP-6BPS8238:/home/ajikisan# userdel -r mariana
root@LAPTOP-6BPS8238:/home/ajikisan# userdel -r daniel
userdel: user 'daniel' does not exist

* Exclusão de grupos criados anteriormente:
root@LAPTOP-6BPS8238:/home/ajikisan# cat /etc/group
root@LAPTOP-6BPS8238:/home/ajikisan# groupdel GRP_ADM
groupdel: group 'GRP_ADM' does not exist
root@LAPTOP-6BPS8238:/home/ajikisan# groupdel GRP_VEN

* Realização da instalação do git no Ubuntu, gerar token no site do github e upload do projeto:
root@LAPTOP-6BPS8238:/home/ajikisan# apt install git -y
Reading package lists... Done
Building dependency tree
Reading state information... Done
git is already the newest version (1:2.25.1-1ubuntu3).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
root@LAPTOP-6BPS8238:/home/ajikisan#


--------------------------------------------------------------------------------------------------------------------------------------------------------
### Conclusão

Neste projeto foi criado um script iacl.sh onde toda a infraestrutura de usuários, grupos de usuários, diretórios e permissões quando executado 
na máquina virtual serão criados automaticamente e deste modo estarão para uso. 

Diretórios
/publico 
/adm
/ven
/sec

Grupos
GRP_ADM
GRP_VEN
GRP_SEC

Usuários
carlos
maria
joao
debora
sebastiana
roberto
josefina
amanda
rogerio
