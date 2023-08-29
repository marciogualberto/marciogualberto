- 👋 Hi, I’m @marciogualberto
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
marciogualberto/marciogualberto is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
class Membro:
    def __init__(self, nome, telefone, email):
        self.nome = nome
        self.telefone = telefone
        self.email = email

class Financa:
    def __init__(self, entrada, saida):
        self.entrada = entrada
        self.saida = saida

class AppIgreja:
    def __init__(self):
        self.videos = []
        self.noticias = []
        self.recados = []
        self.membros = []
        self.financas = Financa(0, 0)

    def postar_video(self, video):
        self.videos.append(video)
        print("Vídeo postado com sucesso!")

    def postar_noticia(self, noticia):
        self.noticias.append(noticia)
        print("Notícia postada com sucesso!")

    def enviar_recado(self, recado):
        self.recados.append(recado)
        print("Recado enviado com sucesso!")

    def adicionar_membro(self, membro):
        self.membros.append(membro)
        print("Membro adicionado com sucesso!")

    def registrar_financas(self, entrada, saida):
        self.financas.entrada += entrada
        self.financas.saida += saida
        print("Finanças registradas com sucesso!")

    def exibir_membros(self):
        print("Lista de Membros:")
        for membro in self.membros:
            print(f"Nome: {membro.nome}, Telefone: {membro.telefone}, Email: {membro.email}")

    def exibir_financas(self):
        print("Finanças da Igreja:")
        print(f"Entrada: R${self.financas.entrada}, Saída: R${self.financas.saida}")

# Exemplo de uso do aplicativo
app = AppIgreja()

# Criando membros
membro1 = Membro("João", "(11) 9999-1234", "joao@example.com")
membro2 = Membro("Maria", "(22) 9876-5432", "maria@example.com")

# Adicionando membros
app.adicionar_membro(membro1)
app.adicionar_membro(membro2)

# Postando vídeo e notícia
app.postar_video("https://exemplo.com/video1")
app.postar_noticia("Nova programação para o próximo culto!")

# Enviando recado
app.enviar_recado("Lembrando a todos sobre o ensaio do coral amanhã.")

# Registrando finanças
app.registrar_financas(1500, 800)

# Exibindo informações
app.exibir_membros()
app.exibir_financas()
