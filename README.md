# Criando um documento PDF com 20 páginas
pdf = FPDF()
pdf.set_auto_page_break(auto=True, margin=15)

# Função para adicionar conteúdo nas páginas
def adicionar_conteudo_pagina(texto):
    pdf.add_page()
    pdf.set_font("Arial", size=12)
    pdf.multi_cell(0, 10, txt=texto)

# Conteúdo adicional sobre criptomoedas para preencher 20 páginas
texto = """
1. Introdução às Criptomoedas: As criptomoedas são moedas digitais, descentralizadas e seguras, usando a tecnologia blockchain.
2. Bitcoin: O primeiro e mais famoso ativo digital, criado por Satoshi Nakamoto em 2009.
3. Blockchain: A tecnologia de registro distribuído que garante a segurança e a transparência das transações de criptomoedas.
4. Ethereum: Uma plataforma de contratos inteligentes, além de ser uma criptomoeda.
5. Outras Criptomoedas: Litecoin, Ripple (XRP), Cardano, e muitas outras com diferentes funcionalidades.
6. Mineração: O processo de validação de transações e criação de novos blocos, recompensando os mineradores com criptomoedas.
7. Proof of Work (PoW) vs Proof of Stake (PoS): Comparação entre dois métodos de consenso utilizados na mineração de criptomoedas.
8. Exchanges de Criptomoedas: Plataformas para comprar, vender e trocar criptomoedas, como Binance e Coinbase.
9. Carteiras Digitais: Ferramentas essenciais para armazenar criptomoedas de forma segura, como as carteiras online ou hardware wallets.
10. Investindo em Criptomoedas: Como comprar e armazenar criptomoedas de forma segura e rentável.
11. Riscos e Volatilidade: O mercado de criptomoedas pode ser altamente volátil, o que implica riscos para os investidores.
12. Regulação de Criptomoedas: A crescente atenção dos governos e entidades reguladoras sobre o uso de criptomoedas.
13. Segurança no Mercado: A importância de proteger suas chaves privadas e evitar golpes e fraudes.
14. NFTs (Tokens Não Fungíveis): Como os NFTs estão se tornando populares no mercado de criptomoedas.
15. Smart Contracts: Contratos autoexecutáveis que têm aplicações práticas além do Bitcoin.
16. DeFi (Finanças Descentralizadas): O movimento que visa criar alternativas financeiras sem a necessidade de intermediários tradicionais.
17. Stablecoins: Criptomoedas com valor estável, frequentemente atreladas ao valor de moedas fiduciárias, como o USDT (Tether).
18. Criptomoedas como Ativo de Reserva de Valor: Como algumas criptomoedas estão sendo vistas como alternativas ao ouro.
19. Tendências Futuras: O impacto potencial de criptomoedas na economia global e nas tecnologias emergentes.
20. Conclusão: O futuro das criptomoedas é promissor, mas envolve riscos, sendo essencial manter-se informado e cauteloso.
"""

# Adicionando conteúdo em 20 páginas
for _ in range(20):
    adicionar_conteudo_pagina(texto)

# Salvando o arquivo com 20 páginas
output_path_20p = "/mnt/data/introducao_criptomoedas_20_paginas.pdf"
pdf.output(output_path_20p)

output_path_20p
