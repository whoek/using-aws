
# Install OCaml on Amazon Linux (EC2)

AMI: Amazon Linux 2 LTS Candidate AMI 2017.12.0 (HVM)

if new image update & upgrade
```
sudo yum update -y && yum upgrade -y
sudo yum install m4 patch ocaml -y
```

Install OPAM as per notes https://opam.ocaml.org/doc/Install.html
```
wget https://raw.github.com/ocaml/opam/master/shell/opam_installer.sh -O - | sh -s /usr/local/bin
```
Install rest via OPAM

```
exit

opam init
eval `opam config env`

opam switch
opam switch 4.06.1
eval `opam config env`
```
This will take a while.
You can then install other programs via opam, e.g. utop
```
opam install utop
```
CURRENTLY UNABLE TO INSTALL CORE
```
opam install core
```






