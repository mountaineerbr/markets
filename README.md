# markets
Bitcoin, crypto and stock related 

![ScreenShot](git_screenshot1.png)
Fig. 1. Scripts on display: binance.sh, bitfinex.sh, binfo.sh,
bitstamp.sh, cgk.sh, cmc.sh and others.


## SUMMARY

This is a repo related to crypto, bank currency and stock markets.

Run scripts with `-h` for help pages. These bash scripts mostly need
`curl`. Some of them will work if you have got `wget` instead.
Some other important packages are `jq` and `websocat` or `wscat` for some scripts.

_I cannot promise to follow up api changes and update these scripts
once they start failing._


## SUMÁRIO

Este repo é relacionado com mercados cripto, moedas de
banco centrais e ações. Rode os scripts com `-h` para páginas de ajuda.

A maioria desses scripts de bash precisam do `curl`.
Alguns irão funcionar se você tiver somente o `wget`.
Alguns outros pacotes importantes para alguns scripts são `jq` e
'websocat' ou `wscat`.

_Não posso prometer acompanhar as alterações das APIs e atualizar esses
scripts assim que começarem a falhar._


## INDEX / ÍNDICE

NAME | DESCRIPTION
:-------------|:-----------
[bakkt.sh](bakkt.sh) | Price and contract/volume tickers from bakkt public api
[binance.sh](binance.sh) |  Binance public API, crypto converter, prices, book depth, coin ticker
[binfo.sh](binfo.sh) | Blockchain explorer for bitcoin; uses <blockchain.info> and <blockchair.com> public apis; notification on new block found
[brasilbtc.sh](brasilbtc.sh) | Fetches bitcoin rates from brazilian exchanges public apis. Puxa cotações de bitcoin de agências de câmbio brasileiras de apis públicas
[cgk.sh](cgk.sh) | <Coinggecko.com> public api, convert one crypto, bank/fiat currency or metal into any another, market ticker, cryptocurrency ticker. This is my favorite everyday-use script for all-currency rates!
[cmc.sh](cmc.sh) |  <Coinmarketcap.com> convert any amount of one crypto, bank/fiat currency or metal into any another, NON-public api access
[myc.sh](myc.sh) | <Mycurrency.net> public api, central bank currency rate converter
[novad.sh](novad.sh) | puxa dados das apis públicas da NovaDax brasileira. fetch public api data from NovaDax brazilian enchange
[ourominas.sh](ourominas.sh) | Ourominas (precious metals exchange) rates public api. Pega taxas da api pública da Ouro Minas
[parmetal.sh](parmetal.sh) | Parmetal (precious metals exchange) rates public api. Pega taxas da api pública da Parmetal
[stocks.sh](stocks.sh) | <Financialmodelingprep.com> latest and historical stock and major index rates
[uol.sh](uol.sh) | Fetches rates from uol service provider public api. Puxa dados de páginas da api pública do uol economia
[whalealert.sh](whalealert.sh) | Data from whale-alert.io free api with the latest whale transactions.
[yahooscrape.sh](yahooscrape.sh) | Scrape some Yahoo! Finance tickers


## API KEYS / CHAVES DE API

Please create free API keys and add them to shell environment or set
them in the script head source code. Demo api keys may have been
added to the scripts, however they may stop working at any time
or get rate limited quickly.

Por favor, crie chaves de API grátis e as adicione no ambiente da shell
ou as configure na cabeça do código-fonte dos scripts. Chaves para fins
de demonstração podem ter sido adicionadas aos scripts, porém elas
podem parar de funcionar a qualquer momento ou serem limitadas rapidamente.
 

## SEE ALSO / TAMBÉM VEJA

**[Scripts Repo](https://github.com/mountaineerbr/scripts)** -
Check some bitcoin-related scripts at my other repo, such as
[binfo.sh](https://github.com/mountaineerbr/scripts/blob/main/binfo.sh),
[bitcoin.blk.sh](https://github.com/mountaineerbr/scripts/blob/main/bitcoin.blk.sh),
[bitcoin.hx.sh](https://github.com/mountaineerbr/scripts/blob/main/bitcoin.hx.sh),
[bitcoin.tx.sh](https://github.com/mountaineerbr/scripts/blob/main/bitcoin.tx.sh) and
[blockchair.btcoutputs.sh](https://github.com/mountaineerbr/scripts/blob/main/blockchair.btcoutputs.sh).

**[Some market-related shell functions](https://github.com/mountaineerbr/dotfiles/blob/main/.rc)** can be found at my shell config file.

---

Alexander Epstein's _currency_bash-snipet.sh_ uses the same API as _erates.sh_

<https://github.com/alexanderepstein>

MiguelMota's _Cointop_ for crypto currency tickers

<https://github.com/miguelmota/cointop>

8go's _CoinBash.sh_ for CoinMarketCap simple tickers (outdated)

<https://github.com/8go/coinbash> 

Brandleesee's _Mop: track stocks the hacker way_

<https://github.com/mop-tracker/mop>

Packages `units` and `qalc` (qalculate) also have got
bank currency rate convertion.


## IMPORTANT / IMPORTANTE

None of these scripts are supposed to be used under truly professional constraints. Do your own research!

Nenhum desses scripts deve ser usado em meio profissional sem análise prévia. Faça sua própria pesquisa!


## BASIC INSTRUCTIONS

On Ubuntu 20.04, you can install `curl`, `jq` and `lolcat` packages easily from the official repos.
The `websocat` and `wscat` packages may be a little more complicated..

To download a script, view it on Github.
Then, right-click on the _Raw_ button and choose _Save Link As ..._ option.
Once downloaded (_eg_ `~/Downloads/binance.sh`),
you will need to mark the script as executable.
In GNOME, _right-click on the file > Properties > Permissions_
and check the _Allow executing file as programme_ box, or

```bash
chmod +x ~/Downloads/binance.sh
```

Then cd to the folder where the script is located.

```bash
cd ~/Downloads
```

To execute it, be sure to add './' before the script name:

```bash
./binance.sh
```
 
or

```bash
bash binance.sh
```

Alternatively, you can clone this entire repo.

```bash
cd Downloads

git clone https://github.com/mountaineerbr/markets.git

chmod +x ~/Downloads/markets/*.sh
```

You can use bash aliases to individual scripts or place them under your $PATH .

Some scripts may need free api keys.

---

## INSTRUÇÕES BÁSICAS

No Ubuntu 20.04, pode-se instalar os pacotes `curl`, `jq` e `lolcat`
facilmente dos repos oficiais.
Já o pacote `websocat` e `wscat` podem ser um pouco mais complicado..

Para fazer o download de um script, abra-o/visualize-o no Github e
depois clique com o botão direito do mouse em cima do botão _Raw_ e
escolha a opção _Salvar Link Como..._.
Depois de feito o download (_por exemplo_, em `~/Downloads/binance.sh`),
será necessário marcar o script como executável.
No GNOME, clicar com o botão direito em
_cima do arquivo > Propriedades > Permissões_ e selecione a caixa
_Permitir execução do arquivo como programa_, ou

```bash
chmod +x ~/Downloads/binance.sh
```

Então, caminhe até a pasta onde script se encontra.

```bash
cd ~/Downloads
```

Para executá-lo, não se esqueça de adicionar './' antes do nome do script:

```bash
./binance.sh
```

ou


```bash
bash binance.sh</i>
```

Alternativeamente, você pode clonar este repo inteiro.

```bash
cd Downloads

git clone https://github.com/mountaineerbr/markets.git

chmod +x ~/Downloads/markets/*.sh
```

Você pode fazer bash aliases individuais para os scripts
ou colocar os scripts sob seu $PATH .

Alguns scripts precisam de chaves de API gratuitas.

---

> If useful, please consider sending me a nickle! =)
>  
> Se foi útil, considere me lançar um trocado!
>
>    bc1qlxm5dfjl58whg6tvtszg5pfna9mn2cr2nulnjr

---

