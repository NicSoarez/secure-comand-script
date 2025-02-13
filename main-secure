import subprocess

# Dicionário com descrições dos comandos
DESCRICOES = {
    "mkdir": "mkdir - Cria um novo diretório no sistema.",
    "rmdir": "rmdir - Remove um diretório vazio.",
    "ls": "ls - Lista os arquivos e diretórios no diretório atual.",
    "pwd": "pwd - Mostra o caminho do diretório atual.",
    "rm": "rm - Remove arquivos ou diretórios.",
    "df": "df -h - Exibe informações sobre o uso do disco.",
    "free": "free -h - Exibe informações sobre o uso da memória RAM.",
    "uname": "uname -a - Exibe informações do sistema operacional.",
    "uptime": "uptime - Mostra há quanto tempo o sistema está ligado.",
    "whoami": "whoami - Exibe o usuário atual.",
    "id": "id - Exibe detalhes do usuário atual.",
    "ps": "ps aux - Lista os processos em execução.",
    "top": "top - Exibe os processos em execução em tempo real.",
    "htop": "htop - Alternativa ao top, com interface mais amigável.",
    "history": "history - Mostra o histórico de comandos do terminal.",
    "echo": "echo 'mensagem' - Exibe uma mensagem no terminal.",
    "cat": "cat arquivo - Exibe o conteúdo de um arquivo.",
    "head": "head arquivo - Mostra as primeiras linhas de um arquivo.",
    "tail": "tail arquivo - Mostra as últimas linhas de um arquivo.",
    "grep": "grep 'texto' arquivo - Busca um texto dentro de um arquivo.",
    "find": "find /caminho -name 'arquivo' - Busca arquivos no sistema.",
    "chmod": "chmod 755 arquivo - Altera as permissões de um arquivo.",
    "chown": "chown usuario:grupo arquivo - Altera o proprietário de um arquivo.",
    "ifconfig": "ifconfig - Exibe informações das interfaces de rede.",
    "ip": "ip a - Exibe informações de IP das interfaces de rede.",
    "ping": "ping endereco - Testa conectividade com um host.",
    "wget": "wget url - Faz download de um arquivo da web.",
    "curl": "curl url - Faz requisições HTTP.",
    "tar": "tar -cvf arquivo.tar pasta - Compacta arquivos.",
    "unzip": "unzip arquivo.zip - Extrai arquivos de um ZIP.",
    "zip": "zip -r arquivo.zip pasta - Compacta arquivos em ZIP.",
    "kill": "kill PID - Finaliza um processo pelo seu ID.",
    "killall": "killall nome_processo - Finaliza processos pelo nome.",
    "reboot": "reboot - Reinicia o sistema.",
    "shutdown": "shutdown -h now - Desliga o sistema imediatamente."
}

def executar_comando(comando):
    """Pergunta ao usuário antes de executar um comando."""
    if comando not in DESCRICOES:
        print(f"Comando '{comando}' não reconhecido.")
        return

    print(f"\nDescrição: {DESCRICOES[comando]}")
    confirmacao = input("Deseja executar este comando? (Sim/Não): ").strip().lower()

    if confirmacao in ["sim", "s"]:
        print(f"\nExecutando: {comando}\n")
        try:
            resultado = subprocess.run(comando.split(), capture_output=True, text=True)
            print(resultado.stdout)  # Mostra a saída do comando
        except Exception as e:
            print(f"Erro ao executar o comando: {e}")
    else:
        print("Comando não executado.\n")

# Loop para interação com o usuário
if __name__ == "__main__":
    while True:
        cmd = input("Digite um comando (ou 'sair' para encerrar): ").strip()
        if cmd.lower() == "sair":
            break
        executar_comando(cmd)
