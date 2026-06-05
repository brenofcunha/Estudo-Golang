# Preparar ambiente Go no Ubuntu

Este guia mostra como preparar o ambiente de trabalho para estudar Go no Ubuntu.

## 1) Instalar o Go

Opcao A: via pacote da distro (mais simples, pode ser versao mais antiga)

```bash
sudo apt update
sudo apt install golang-go
```

Opcao B: via pacote oficial (mais atual)

1. Baixe o tarball do Go em: https://go.dev/dl/
2. Extraia para /usr/local:

```bash
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.xx.x.linux-amd64.tar.gz
```

3. Adicione o Go no PATH (exemplo para bash):

```bash
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
source ~/.bashrc
```

## 2) Verificar a instalacao

```bash
go version
```

Se aparecer a versao do Go, a instalacao esta ok.

## 3) Criar um projeto simples

```bash
mkdir -p ~/go-estudos/hello
cd ~/go-estudos/hello
go mod init hello
```

Crie o arquivo main.go:

```go
package main

import "fmt"

func main() {
    fmt.Println("Ola, Go!")
}
```

Executar:

```bash
go run main.go
```

## 4) Estrutura recomendada

- Use uma pasta por exercicio ou projeto.
- Sempre rode `go mod init` no inicio.
- Mantenha arquivos .go pequenos e focados no tema do estudo.

## 5) Dicas

- Atualizar o Go: remova /usr/local/go e repita a instalacao oficial.
- Editor: VS Code com extensao Go ajuda com auto-complete e testes.
