Apresentação Java+Javalin - Bernardo Candia

Parte 1 - Mostrar execução de um dos códigos disponibilizados

Nessa primeira parte do trabalho, tentei executar tanto o código do Hello World quanto o código dos Advice, porém, toda vez que eu copiava para o Codespace, ele não funcionava, e abaixo tem um gif mostrando o erro.

<img width="800" height="427" alt="PreviewREADME md-elc117-2026aCodespaces_didactichappiness-VisualStudioCodeMozillaFirefox2026-05-2715-28-23-ezgif com-video-to-gif-converter" src="https://github.com/user-attachments/assets/e93dc7f4-e0c8-45c5-9c35-0536103600de" />


Como pode ser visto, ele dava erro de Bash, e até mesmo no de Random Advice ele dava o mesmo erro, e eu não soube como arrumar, tentei até mesmo criar manualmente a porta 3000 e acessar ela, mas o navegador apenas dava " Página não encontrada " E o "Tentar Novamente"

Parte 2 - Encontrar nos códigos, tanto os disponibilizados, quanto o gerado na Segunda, Códigos conhecidos e desconhecidos

Abaixo, está uma parte do código de Random Advice, e havia algumas coisas que me chamaram a atenção


   public static void main(String[] a) {
        int p = Integer.parseInt(System.getenv().getOrDefault("PORT", "3000"));
        var app = Javalin.create();
        app.get("/advice", ctx -> {
            var i = ThreadLocalRandom.current().nextInt(ADVICES.size());
            ctx.result(ADVICES.get(i));
        });
        app.start(p);



Abaixo, está uma parte do código que foi gerado na Segunda Feira, e nele, pude identificar coisas que me chamaram a atenção por ser conhecidos e desconhecidos

public class Main {
    private static final Logger log = LoggerFactory.getLogger(Main.class);
    private static Javalin app;

Nesse código da Main, ele cria um log, mas confesso não ter entendido o que é o "LoggerFactory", se era um nome criado ou foi gerado a partir do banco de dados ou algo do tipo, e abaixo, entendi que ele estava carregando o Javalin e criando ele do tipo Static.
