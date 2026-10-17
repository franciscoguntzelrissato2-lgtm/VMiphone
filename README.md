# Meta Velha

Jogo da velha para iPhone, criado com HTML/CSS/JavaScript e Capacitor. O fluxo do Codemagic cria o projeto nativo iOS no Mac de compilação, compila um app para iPhone sem assinatura e o empacota como IPA com a pasta `Payload/MetaVelha.app`. Esse pacote é destinado ao Sideloadly, que fará a assinatura durante a instalação.

## Compilar no Codemagic

1. Envie esta pasta para um repositório GitHub.
2. No Codemagic, conecte o repositório e selecione o workflow `Meta Velha iOS`.
3. Inicie a compilação e baixe `MetaVelha-unsigned.ipa` em Artifacts.
4. Abra esse IPA no Sideloadly e use o fluxo Apple ID Sideload para assinar e instalar no aparelho.

O identificador `com.metavelha.game` é o Bundle ID inicial. O IPA criado pelo Codemagic não está assinado e não instala diretamente; o Sideloadly assina uma cópia para a instalação.
