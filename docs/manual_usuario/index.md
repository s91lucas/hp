---
hide:
  - feedback
---

# Manual de Usuário
---

<p align="center">
  <img src="img/manual1i.svg" alt="Logo" width="500"/>
</p>

Bem-vindo à Central de Ajuda do MILO. Aqui você encontrará informações úteis para tirar dúvidas, resolver problemas e aproveitar ao máximo todas as funcionalidades da plataforma.

---
<p align="center">
  <span class="text-destaque">Olá, como podemos te ajudar?</span>
</p>

<form role="search" id="custom-search" style="max-width:800px;margin:2rem auto;display:flex;">
  <input type="search" placeholder="Digite o termo de pesquisa aqui..." style="flex:1;padding:1rem;border-radius:420px 0 0 420px;border:1px solid #ccc;">
  <button type="submit" style="padding:0.5rem 1rem;border-radius:0 420px 420px 0;border:1px solid #ccc;background:#F37335;color:#fff;">Buscar</button>
</form>
---
<div class="grid cards" markdown>

-   🚚 <span class="text-laranja">__Vendas e Rotas__</span>

    ---
    [Cadastro de Vendas](vendas.md)

    [Rotas e Entregas](rotas.md)


-   📦 <span class="text-laranja">__Estoques__</span>

    ---
    [Cadastrando Produtos](estoques.md)

    [Gerenciando Estoque](gerenciando-estoque.md)

    [Fornecedores](fornecedores.md)

-   📃 <span class="text-laranja">__Relatórios e Controle__</span>

    ---
    [Relatórios MILO](relatorios.md)

    [Alertas do Sistema](alertas.md)


-   🔐 <span class="text-laranja">__Conta e segurança__</span>

    ---
    [Redefinindo a Senha](segurança.md)

    [Perfil de Usuário](perfil.md)

</div>



<script>
document.addEventListener("DOMContentLoaded", function() {
  const customSearch = document.getElementById("custom-search");
  const customInput = customSearch.querySelector("input[type='search']");
  customSearch.addEventListener("submit", function(e) {
    e.preventDefault();
    // Encontra o input da barra de busca do header
    const headerSearch = document.querySelector("input.md-search__input");
    if (headerSearch) {
      headerSearch.value = customInput.value;
      headerSearch.focus();
      // Abre o painel de busca se estiver fechado
      const searchToggle = document.querySelector('label[for="__search"]');
      if (searchToggle) {
        searchToggle.click();
      }
      // Dispara o evento de input para ativar a busca instantânea
      headerSearch.dispatchEvent(new Event('input', { bubbles: true }));
    }
  });
});
</script>