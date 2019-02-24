Anotacoes
```
                // problema do NOLOCK

                // desafio delete 100 linhas


                // placa de carro
                var id5 = ctx.Users
                .Where(u => u.Nick.Replace("-", "") == "f")
                .FirstOrDefault();

                // join
                var id4 = from u in ctx.Users
                          join d in ctx.UserDescs on u.Id equals d.Id 
                          where u.Name == "f" && d.Etc != null                          
                          select (new
                          {
                              d.Id
                          });
                var ids4 = id4.Distinct().ToArray();

                // placa de carro
                var id3 = ctx.Users
                .Where(u => u.Nick == "f")
                .FirstOrDefault();

                // agencia e conta
                var id2 = ctx.Users
                .Where(u => u.Name + u.Nick == "f" )
                .FirstOrDefault();

                // case insensitive?
                var id1 = ctx.Users
                    .Where(u => u.Name.ToLower() == "f")
                    .Where(u => u.Password == "a")
                    .SingleOrDefault();
                
                // replace cpf .
```
