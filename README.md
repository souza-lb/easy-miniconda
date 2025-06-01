# EASY MINICONDA - Instalação e Desinstalação Automática

## Visão Geral
O Easy Miniconda fornece scripts para instalação e desinstalação simplificada do Miniconda em sistemas Linux. Os scripts automatizam todo o processo, incluindo configuração de ambiente e gerenciamento de dependências.

## 📦 Como instalar?

**No terminal com sua conta de usuário comum execute:**

```bash
wget -qO- https://raw.githubusercontent.com/souza-lb/easy-miniconda/main/install | bash
```

### Saída Esperada:
```
--------------------------------------------
  Instalação do Miniconda versão 1.0        
--------------------------------------------

1 - Verificar dependências
2 - Verificar instalação existente
3 - Baixar o instalador do Miniconda
4 - Instalar em: '/home/user/miniconda3'
5 - Configurar aliases no bashrc
6 - Realizar limpeza automática

Dependências verificadas: wget e bash encontrados.
Download concluído com sucesso!
Miniconda instalado em: /home/user/miniconda3
Configuração adicionada ao .bashrc:
  # miniconda3 auto config
  alias conda-on="source '/home/user/miniconda3/bin/activate'"
  alias conda-off="conda deactivate"

--------------------------------------------
     Instalação concluída com sucesso !     
--------------------------------------------

Próximos passos:
1. Recarregue o terminal ou execute:
   source ~/.bashrc
2. Para ativar o conda:
   conda-on
3. Para criar novo ambiente:
   conda create -n meu_ambiente
4. Para desativar o conda:
   conda-off
```

## Comandos Após Instalação

### Ativar o Conda
```bash
conda-on
```

### Desativar o Conda
```bash
conda-off
```

### Gerenciar Ambientes
```bash
# Criar novo ambiente
conda create -n meu_ambiente

# Criar ambiente com versão python específica (Ex: 3.9.2)
conda create -n meu-ambiente python=3.9.2

# Ativar ambiente
conda activate meu_ambiente

# Instalar pacotes
conda install numpy pandas

# Listar ambientes
conda env list

# Remover ambiente
conda env remove -n meu_ambiente
```

## Fluxo de Trabalho Recomendado
1. Ative o conda: `conda-on`
2. Crie um novo ambiente para cada projeto
3. Instale os pacotes necessários no ambiente
4. Quando terminar, desative o conda: `conda-off`

## Notas Importantes
- Requer permissão de superusuário apenas se instalar em locais restritos
- Mantém seu `.bashrc` seguro com backups durante modificações
- Compatível com a maioria das distribuições Linux modernas
- Sempre solicita confirmação para operações destrutivas

## 🗑️ Como desinstalar?

**No terminal com sua conta de usuário comum execute:**

```bash
wget -qO- https://raw.githubusercontent.com/souza-lb/easy-miniconda/main/uninstall | bash
```

### Etapas da Desinstalação:
1. **Verificação de instalação**: Confirma existência do Miniconda
2. **Confirmação do usuário**: Solicita confirmação para desinstalação
3. **Remoção de configurações**:
   - Remove aliases e configurações do `.bashrc`
   - Cria backup do arquivo original
4. **Remoção da instalação principal**:
   - Remove o diretório `$HOME/miniconda3`
   - Mostra tamanho da instalação antes de remover
5. **Finalização**: Exibe mensagem de conclusão

### Saída Esperada:
```
--------------------------------------------
  Desinstalação Miniconda versão 1.0        
--------------------------------------------

1 - Verificar instalação
2 - Remover entradas do bashrc
3 - Remover instalação principal
4 - Finalizar desinstalação

Instalação localizada: /home/user/miniconda3
Deseja realmente desinstalar o Miniconda? [s/N]: s
Removendo configurações do .bashrc...
Configurações removidas do .bashrc!
Backup salvo em: /home/user/.bashrc.backup-miniconda
Tamanho da instalação: 1.2G
Atenção! Esta operação é irreversível!
Confirme a remoção do Miniconda? [s/N]: s
Removendo instalação principal...
Remoção concluída: /home/user/miniconda3

--------------------------------------------
   Desinstalação concluída com sucesso !    
--------------------------------------------

Recomendações:
1. Recarregue seu terminal com:
   source ~/.bashrc
2. Verifique se todas as entradas foram removidas

Suporte: souzalb@proton.me
```

---

## ❤️ Apoie o Projeto

**Dúvidas, sugestões e contribuições?**  
Leonardo Bruno  
souzalb@proton.me  

**Gostou do projeto e quer realizar uma contribuição voluntária?**  
*(Pode ser o valor de uma xícara de café ou chá...) ☕ 🍵*  

Chave PIX:  
`8dcc7e3c-0c6a-4c6f-a4c0-26a5e62686db`  

Ou utilize o QR Code abaixo:  

<p align="center">
  <img src="images/qrcode-pix.png" alt="QR Code PIX" width="200">
</p>

**Você também pode utilizar o PayPal:**  

[![PayPal](https://img.shields.io/badge/Donate-PayPal-00457C?style=for-the-badge&logo=paypal)](https://www.paypal.com/donate/?hosted_button_id=EQVW5QQ7GBGSY)

<p align="center">
  <img src="images/qrcode-paypal.png" alt="QR Code PayPal" width="200">
</p>

**A utilização deste projeto é livre para alterações e adaptações**  
*Desde que feita a devida referência ao repositório original e seu criador.*
