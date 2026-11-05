# Criar um FDU e uma ficha adicional no ARTSOFT

Guia baseado na gravação `Gravação 2026-11-05 114412.mp4`, de 05/11/2026,
com duração de 2 min 50 s, no ARTSOFT Professional v26.
As capturas abaixo foram extraídas do vídeo. Os tempos indicam a posição
na gravação, não a hora do dia.

## Objetivo

Criar um campo adicional (FDU), colocá-lo numa ficha e apresentar essa
ficha no registo correspondente do ARTSOFT.

O exemplo usa Colaboradores. Conforme indicado pelo utilizador, pode
selecionar outro tipo de ficha para criar o FDU na tabela pretendida.
Use o mesmo tipo de ficha ao criar o campo e ao desenhar a ficha.

| Elemento | Valor do exemplo | Onde é utilizado |
| --- | --- | --- |
| Tipo de ficha | 06 - Colaboradores | Campo e ficha adicional |
| Número do campo FDU | 701 | Propriedade Campo do controlo |
| Nome do campo | testefdu2 | Definição do FDU |
| Tipo do campo | Alfanumérico | Definição do FDU |
| Número da ficha | 11 | Acessos do utilizador |
| Nome inicial da ficha | testefdu2 | Criação da ficha |
| Texto da ficha no editor | ficha testefdu2 | Título do separador |

Os números e nomes são os usados na demonstração. Para outro caso,
escolha identificadores disponíveis e nomes adequados.

## 1. Abrir a definição de campos adicionais

1. Abra **Configurações → Fichas Adicionais**.
2. Selecione **Definição de campos adicionais**.
3. Em **Tipo de ficha**, escolha a tabela de destino.
4. No exemplo, marque **06 - Colaboradores** e confirme em **OK**.

![Menu de fichas adicionais][img-menu]

*00:04,5 — Acesso à definição de campos e ao Editor de Fichas.*

![Escolha da tabela de destino][img-tabela]

*00:08 — Seleção do tipo de ficha.*

## 2. Criar o campo FDU

Na janela de manutenção da tabela de campos de fichas adicionais:

1. Clique no botão **+** verde para inserir um campo.
2. Preencha o número, o nome e o tipo do campo.
3. Ajuste as restantes opções à finalidade do campo.
4. Confirme em **OK** e verifique o campo na lista.

A barra de estado identifica o comando como **Inserir novo campo FDU**,
com os atalhos **Ins / Ctrl+N**.

| Propriedade | Valor observado no exemplo |
| --- | --- |
| 01 - Nº do campo | 701 |
| 02 - Nome do campo | testefdu2 |
| 03 - Descrição do campo | Em branco |
| 04 - Tipo de campo | Alfanumérico |
| 05 - Campo para imprimir? | Não |
| 06 - Campo contém texto unicode? | Não |
| 07 - Campo contém dados pessoais? | Não |
| 08 - Campo para exportar em XML? | Sim |
| 13 - Campo usado nas fichas | Em branco nesta fase |

![Definição do campo FDU 701][img-fdu]

*00:36 — Campo 701, nome testefdu2 e exportação XML ativa.*

As opções acima reproduzem o exemplo; não são obrigatórias para todos
os FDU. A ajuda visível descreve **Campo usado nas fichas** como a lista
de fichas onde o campo é usado atualmente. A ligação ao controlo será
definida no editor, no passo 4.

## 3. Criar a ficha adicional

1. Regresse a **Configurações → Fichas Adicionais**.
2. Abra **Editor de Fichas**.
3. Selecione o mesmo tipo usado no FDU: **06 - Colaboradores**.
4. Confirme em **OK**.
5. Na manutenção das fichas adicionais, clique no **+** verde.
6. Na janela **Inserir nova ficha**, indique o número e o nome.
7. Confirme em **OK** para abrir o editor.

Na demonstração, o número da nova ficha é **11** e o nome introduzido
é **testefdu2**.

![Inserir nova ficha][img-ficha]

*01:02 — Criação da ficha 11 com o nome testefdu2.*

## 4. Desenhar a ficha e associar o FDU

### 4.1. Configurar a área da ficha

Selecione o fundo da ficha e ajuste as propriedades da área de desenho.
No vídeo, a propriedade **Texto** da ficha apresenta **ficha testefdu2**;
este é também o título do separador mostrado no final.

![Propriedades da ficha][img-area]

*01:12 — Área da ficha e propriedade Texto.*

### 4.2. Inserir a legenda

1. Na barra do editor, selecione **Texto estático**, identificado por
   um ícone com letras e pela respetiva ajuda ao passar o rato.
2. Coloque a legenda na área da ficha.
3. Nas propriedades do objeto, altere **Texto** para **testefdu2**.
4. Ajuste a posição e as dimensões para deixar espaço para a entrada.

A legenda identifica visualmente o campo. A associação ao FDU é feita
no controlo de entrada seguinte.

### 4.3. Inserir e ligar o controlo de entrada

1. Selecione o controlo de entrada de texto na barra do editor
   (ícone **ab|**, usado no vídeo).
2. Desenhe o controlo à direita da legenda.
3. Com o controlo selecionado, abra **Propriedades → Dados**.
4. Em **Campo**, introduza **701**, o número do FDU criado no passo 2.
5. Defina **Escrita = Sim** para permitir o preenchimento.
6. No exemplo, mantenha **Obrigatório = Não** e **Hiperligação = Não**.

![Controlo associado ao campo 701][img-ligacao]

*02:04 — Propriedade Campo = 701 e Escrita = Sim.*

| Propriedade do controlo | Valor final visível |
| --- | --- |
| Tipo | Texto |
| Campo | 701 |
| Escrita | Sim |
| Obrigatório | Não |
| Hiperligação | Não |
| X / Y | 115 / 10 |
| Largura / Altura | 100 / 12 |

As medidas são apenas as do exemplo. Ajuste-as ao desenho pretendido.
O valor essencial para a ligação é **Campo = número do FDU**.

### 4.4. Guardar

Guarde a ficha através do ícone de disquete no canto superior esquerdo
e feche o editor. Saia das janelas de manutenção para regressar ao
ecrã principal.

## 5. Configurar a apresentação da ficha no ARTSOFT

Depois de criar a ficha, associe o seu número ao utilizador que a deve
visualizar, na empresa em causa.

1. Abra **Empresa → Funções de Supervisão → Acessos**.
2. Selecione **Registo de Utilizadores**.
3. Escolha o utilizador pretendido. No vídeo é **ADMIN**, número **1**.
4. Abra o separador **Acessos na Empresa** e clique em **Alterar**.
5. Na secção **Fichas Adicionais**, localize **Empregados**.
6. Acrescente o número da ficha à lista, separado por ponto e vírgula.
7. Preserve os números já existentes e clique em **Gravar**.

![Caminho para o registo de utilizadores][img-menu-acessos]

*02:18,5 — Empresa → Funções de Supervisão → Acessos.*

No exemplo, a lista é alterada da seguinte forma:

```text
Antes:  1;2;3;4;5;6;7;8
Depois: 1;2;3;4;5;6;7;8;11
```

![Ficha 11 adicionada aos acessos][img-acessos]

*02:31 — Fichas Adicionais → Empregados com o número 11 acrescentado.*

**Neste campo deve ser indicado 11, o número da ficha.** O número
**701** identifica o FDU e é utilizado na propriedade **Campo** do
controlo no editor.

O exemplo configura **Empregados** dentro de **Fichas Adicionais**.
Existe outra secção chamada **Fichas Configuráveis** no mesmo ecrã;
não é essa a secção utilizada nesta demonstração.

Para outras tabelas, escolha a entrada correspondente quando disponível.
O vídeo demonstra a configuração de Colaboradores/Empregados e não
mostra a configuração de apresentação de todos os outros tipos.

## 6. Confirmar a apresentação no registo

1. Feche o registo de utilizadores.
2. Abra **Registo Colaboradores** na barra principal.
3. Na linha de separadores, use as setas da direita para localizar
   **ficha testefdu2**, se não estiver imediatamente visível.
4. Selecione esse separador.
5. Confirme a presença da legenda **testefdu2** e da caixa de entrada.

![Ficha apresentada no registo de colaborador][img-resultado]

*02:48 — Separador ficha testefdu2 aberto no Registo de Colaborador
Interno, com o campo visível.*

O vídeo confirma a apresentação da ficha e do controlo. Não mostra
o preenchimento e a gravação de um valor num colaborador. Para validar
também a persistência, abra um registo de teste, preencha o campo,
grave e volte a abrir o registo para conferir o valor.

## Verificações quando a ficha ou o campo não aparecem

| Situação | O que verificar |
| --- | --- |
| O separador não aparece | Ficha guardada e número nos acessos |
| Só outro utilizador vê a ficha | Utilizador e empresa configurados |
| O separador está fora da área visível | Setas da linha de separadores |
| A legenda aparece sem ligação ao FDU | Campo = número do FDU no controlo |
| O controlo não permite escrita | Escrita = Sim e registo em alteração |
| Surgiu uma ficha diferente | Número da ficha e tipo de ficha escolhidos |

Estas verificações decorrem das configurações mostradas. Não representam
um diagnóstico de erros testados durante a gravação.

## Sequência de referência

**Criar FDU → Criar ficha → Inserir controlo → Associar ao FDU →
Guardar ficha → Adicionar ficha aos acessos → Verificar no registo.**

Documentação produzida por análise visual do vídeo fornecido.
Não foram feitas alterações no ARTSOFT durante a elaboração deste guia.

[img-menu]: documentacao/capturas-video/video-4-5s.png
[img-tabela]: documentacao/capturas-video/video-008s.png
[img-fdu]: documentacao/capturas-video/video-036s.png
[img-ficha]: documentacao/capturas-video/video-062s.png
[img-area]: documentacao/capturas-video/video-72s.png
[img-ligacao]: documentacao/capturas-video/video-124s.png
[img-menu-acessos]: documentacao/capturas-video/video-138-5s.png
[img-acessos]: documentacao/capturas-video/video-151s.png
[img-resultado]: documentacao/capturas-video/video-168s.png
