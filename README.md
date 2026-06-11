const botao = document.getElementById("saibaMais");

if(botao){
    botao.addEventListener("click", () => {
        alert(
            "O comedouro sustentável foi projetado para reduzir desperdícios, facilitar o manejo e aumentar a eficiência da alimentação animal."
        );
    });
}

// animação ao rolar a página

const elementos = document.querySelectorAll(
    ".card, .imagem, .conteudo, .grid img"
);

const observer = new IntersectionObserver((entries)=>{
    entries.forEach((entry)=>{
        if(entry.isIntersecting){
            entry.target.style.opacity = "1";
            entry.target.style.transform = "translateY(0)";
        }
    });
},{
    threshold:0.2
});

elementos.forEach((el)=>{
    el.style.opacity = "0";
    el.style.transform = "translateY(40px)";
    el.style.transition = ".8s ease";
    observer.observe(el);
});

// formulário

const form = document.querySelector("form");

if(form){
    form.addEventListener("submit",(e)=>{
        e.preventDefault();

        alert("Mensagem e# Comedouro Sustentável

Landing page inspirada em páginas do setor agro para divulgação de comedouros e equipamentos rurais.

## Estrutura

- index.html
- style.css
- script.js
- README.md

## Funcionalidades

- Hero banner
- Seção do produto
- Benefícios
- Galeria
- Formulário de contato
- Layout responsivo

## Como usar

1. Baixe os arquivos.
2. Mantenha todos na mesma pasta.
3. Abra o arquivo `index.html` no navegador.

## Tecnologias

- HTML5
- CSS3
- JavaScript
nviada com sucesso!");

        form.reset();
    });
}
