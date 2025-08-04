# Cookie Poisoning

**CTF**: HackTheBox  
**Categoria**: Web  
**Dificuldade**: Fácil  
**Técnica usada**: Interceptação e modificação de cookies

---

## 🔍 Análise

Ao acessar o site, recebemos um cookie de sessão com valor estranho. Usando o Burp Suite, foi possível interceptar o cookie e perceber que ele estava codificado em base64.

Após decodificar, observamos o campo `role=user`.

Modificamos para `role=admin`, recodificamos em base64 e substituímos no navegador.

---

## ✅ Resultado

Após atualizar a página, obtivemos acesso ao painel de administrador e a flag foi exibida:

```
HTB{cookies_can_be_dangerous}
```

---

## 🧠 Conclusão

Sempre desconfie de cookies com dados codificados. Verifique se é possível manipulá-los para escalar privilégios.
