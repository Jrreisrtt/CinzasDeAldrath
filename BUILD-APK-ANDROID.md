# Como gerar o APK de Cinzas de Aldrath pelo celular

O projeto Unity está dentro de `game.zip`. O workflow extrai os arquivos, cria a arena de teste e tenta compilar um APK de desenvolvimento.

## 1. Gerar o arquivo de ativação
1. Abra https://github.com/Jrreisrtt/CinzasDeAldrath/actions
2. Selecione **Preparar licença Unity Personal** e toque em **Run workflow**.
3. Ao terminar, abra a execução e baixe o artefato **Unity-Activation-Request**. Ele contém o arquivo `.alf`.

## 2. Obter a licença Unity Personal
1. Acesse https://license.unity3d.com/manual e entre na sua conta Unity.
2. Envie o arquivo `.alf` e baixe a licença `.ulf`.
3. No GitHub, abra **Settings → Secrets and variables → Actions → New repository secret**.
4. Nome do segredo: `UNITY_LICENSE`. Valor: o conteúdo completo do arquivo `.ulf`. Salve.

Não publique o arquivo de licença nem o coloque no repositório.

## 3. Executar a compilação
1. Volte a https://github.com/Jrreisrtt/CinzasDeAldrath/actions
2. Selecione **Compilar APK Android** → **Run workflow**.
3. Se concluir com sucesso, baixe **CinzasDeAldrath-APK-Android** na página da execução.

Não envie sua senha Unity nesta conversa. O APK será de desenvolvimento e ainda precisará ser instalado e testado no celular. A compilação ainda não foi executada.
