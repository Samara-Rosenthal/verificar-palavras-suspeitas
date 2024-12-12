# verificar-palavras-suspeitas
Verificar se o corpo do e-mail contém palavras suspeitas de phishing

def verificar_phishing(mensagem):
    palavras_suspeitas = ["ganhe", "prêmio", "urgente", "desconto", "click", "promoção"]
    for palavra in palavras_suspeitas:
        if palavra in mensagem.lower():
            return "Phishing"
    return "Seguro"

def main():
    email_usuario = input("Digite o e-mail: ")
    resultado = verificar_phishing(email_usuario)
    print(f"Classificação: {resultado}")

if __name__ == "__main__":
    main()
