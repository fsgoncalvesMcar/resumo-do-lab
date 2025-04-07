# resumo-do-lab
Guia: Como Criar Máquinas Virtuais no Azure
1. Criando uma máquina virtual pelo Portal do Azure (Interface Gráfica)
  Acesse o Portal do Azure: Entre no portal do Azure e faça login com suas credenciais.
  Crie um grupo de recursos:
  Clique em "Grupos de Recursos" no menu esquerdo.
  Selecione "Criar".
  Insira um nome para o grupo e a região desejada.
  Configure a máquina virtual:
  Clique em "Máquinas Virtuais" e selecione "Criar".
  Escolha o sistema operacional (ex.: Windows Server ou Ubuntu).
  Defina o nome, região, e o tamanho (CPU e memória).
  Escolha o tipo de autenticação (Senha ou chave SSH).
  Configuração de rede: Configure a rede virtual, sub-rede e defina as regras de acesso como RDP ou SSH.
  Revisão e criação: Valide as configurações e clique em "Criar".
  Acesso à máquina: Use o IP público para conectar via RDP ou SSH.

2. Criando uma máquina virtual usando o Azure CLI
  Instale e configure a CLI do Azure:
  Certifique-se de ter a CLI instalada. Use o link oficial.
  Faça login com o comando: az login
  Criar um grupo de recursos: az group create --name myResourceGroup --location eastus
  Criar a máquina virtual: 
    az vm create \
    --resource-group myResourceGroup \
    --name myVM \
    --image Ubuntu2204 \
    --admin-username azureuser \
    --generate-ssh-keys
  Acessar a máquina: Use SSH: ssh azureuser@<PUBLIC_IP_ADDRESS>
