   // adiciona um acrescimo comum ao Açaí
     adicionarOuRemoverAcrescimoComum: (idCarrinho, idAcrescimoComum) => {
        acrescimoComum = ACRESCIMOS['acrescimos-comum'].find(acrescimo => idAcrescimoComum == acrescimo.id);

        $.each(MEU_CARRINHO, function (index, item) {
            if (item.idCarrinho == idCarrinho) {

                let acrescimoExistente = item.acrescimosComuns.find(acrescimo => acrescimo.id == acrescimoComum.id);

                if (!acrescimoExistente) {
                    // Adiciona novos itens de acréscimosComuns aos itens antigos
                    item.acrescimosComuns.push(acrescimoComum);

                } else {

                    item.acrescimosComuns = item.acrescimosComuns.filter(acrescimo => acrescimo.id !== acrescimoExistente.id);

                }
                return false; // Para de percorrer assim que encontrar o item
            }
        });
    },

    adicionarOuRemoverAcrescimoComum: (idCarrinho, idAcrescimoComum) => {
        acrescimoComum = ACRESCIMOS['acrescimos-comum'].find(acrescimo => idAcrescimoComum == acrescimo.id);

        $.each(MEU_CARRINHO, function (index, item) {
            if (item.idCarrinho == idCarrinho) {

                let acrescimoExistente = item.acrescimosComuns.find(acrescimo => acrescimo.id == acrescimoComum.id);

                if (!acrescimoExistente) {
                    // Adiciona novos itens de acréscimosComuns aos itens antigos
                    item.acrescimosComuns.push(acrescimoComum);

                } else {

                    item.acrescimosComuns = item.acrescimosComuns.filter(acrescimo => acrescimo.id !== acrescimoExistente.id);

                }
                return false; // Para de percorrer assim que encontrar o item
            }
        });
    },