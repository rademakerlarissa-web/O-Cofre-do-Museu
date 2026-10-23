# O Cofre do Museu

Página interativa de investigação lógica, baseada no **dossiê 3** da atividade *"Detetive: O Caso da Cláusula Vazia"* (Profa. Wilcilene Kowal, Lógica para Computação, IFC São Bento do Sul).

O jogador investiga o arrombamento de um cofre de museu usando **lógica proposicional**, **forma normal conjuntiva (FNC)** e o **método da resolução** para decidir se as pistas são contraditórias ou não.

[Atividade original](https://wilcilene.github.io/estudos/disciplinas/logica-para-computacao/2027/atividade-clausula-vazia.html)

## O caso

O cofre onde o museu guardava a coleira de ouro da Estrela foi encontrado aberto. O chefe da segurança garante que foi arrombamento, mas a perícia tem dúvidas.

**Pergunta do caso:** as pistas provam que o cofre foi arrombado? Para responder, nega-se a conclusão, aplica-se resolução e verifica-se se aparece a cláusula vazia (□).

### Símbolos

| Símbolo | Significado |
|---------|-------------|
| K | o cofre foi aberto com a chave |
| F | o cofre foi arrombado |
| A | o alarme foi desativado |
| S | o segurança estava de plantão |

### Pistas e cláusulas

| Pista | Em lógica | Cláusula |
|-------|-----------|----------|
| 1 | K ∨ F | (1) {K, F} |
| 2 | F → A | (2) {¬F, A} |
| 3 | S | (3) {S} |
| 4 | ¬A ∨ ¬S | (4) {¬A, ¬S} |
| Conclusão negada | ¬F | (5) {¬F} |

### Resultado

Não surge □ em nenhum momento: o conjunto é **satisfatível**, com a valoração `K = V, F = F, A = F, S = V`. Ou seja, as pistas **não** provam o arrombamento. O cofre foi aberto com a chave, e a versão do chefe da segurança contradiz as evidências.

## Estrutura da página

A página tem um HUD fixo no topo (com as cinco estrelas de progresso) e quatro fases:

1. **Cena do crime:** quatro cartões de pista. Ao examinar cada um, aparecem a tradução em lógica, a conversão para FNC e a cláusula correspondente.
2. **Laboratório:** o jogador nega a conclusão e escolhe pares de cláusulas para aplicar a regra de resolução. Todos os passos ficam registrados em uma tabela, com o literal cancelado, o resolvente e uma explicação em linguagem natural.
3. **Interrogatório:** interruptores para os valores de verdade de K, F, A e S, com verificação em tempo real de cada cláusula. Inclui a tabela das 16 valorações possíveis; clicar em uma linha mostra a explicação completa dela.
4. **Veredito:** conclusão do caso, carimbo final, roteiro das oito perguntas da apresentação e um modelo de registro preenchido que pode ser copiado.

## Objetivos (cinco estrelas)

- Examinar as 4 pistas
- Negar a conclusão
- Derivar {¬A}, {¬F} e {K} pela regra de resolução
- Saturar o conjunto (nenhum resolvente novo, sem □)
- Achar a valoração que satisfaz todas as cláusulas

Ao cumprir os cinco, o caso é carimbado como **"Sem contradição"**.

## Recursos do laboratório

- **Negar a conclusão:** acrescenta {¬F} ao conjunto.
- **Aplicar resolução:** valida o par escolhido e avisa quando não há literal complementar, quando há dois pares complementares ou quando o cruzamento já foi feito.
- **Dica:** destaca o próximo par de cláusulas a cruzar.
- **Verificar saturação:** indica se ainda existem resolventes novos.
- **Mostrar solução completa:** executa os seis passos da resolução automaticamente.
- **Reiniciar:** volta ao conjunto inicial de quatro pistas.

## Tecnologia

- Arquivo único: `O Cofre do Museu.html`, com HTML, CSS e JavaScript puro (sem frameworks e sem etapa de build).
- Fontes via Google Fonts: Barlow, Barlow Condensed e JetBrains Mono. Sem internet, a página usa fontes de sistema.
- Layout responsivo, com suporte a áreas seguras (*safe areas*) em celulares.

## Acessibilidade

- Navegação por teclado, com indicador de foco visível.
- Atributos ARIA (`aria-live`, `aria-pressed`, `aria-expanded`, `role="switch"`) para leitores de tela.
- Respeita `prefers-reduced-motion`, desativando animações e transições.

## Como usar

1. Baixe ou clone o arquivo `O Cofre do Museu.html`.
2. Abra-o em qualquer navegador moderno (basta dar duplo clique).
3. Percorra as quatro fases e cumpra os cinco objetivos.

Não há dependências para instalar.

## Autores

- João Victor de Souza Mendes
- Larissa R. Gabriel

## Créditos

Baseado no dossiê 3 da atividade *"Detetive: O Caso da Cláusula Vazia"*, da Profa. Wilcilene Kowal, disciplina de Lógica para Computação, IFC São Bento do Sul.