# Blockchain com Javascript

A seguir seguir um script simples para escrever uma transação na Blockchain. Utilizou-se a biblioteca bitcore.
Para a importar a biblioteca foi necessário realizar a instalação do NodeJS.

## Passo a Passo - Alô Mundo!
Demonstrando como escrever uma mensagem no Blockchain.
Primeiro foi necessário importar a bliblioteca "bitcore". Isto nos permitiu criar uma transação.

### Passo 1
Importar as bibliotecas "bitcore" e "bitcore-exploradores", utilizado o comando:

> sudo NPM instalar bitcore@0.13.0~~number=plural && sudo NPM instalar bitcore-exploradores

### Passo 2
Foi criado um arquivo com o nome "blockchainTransaction.js" e importados os módulos "bitcore" e "bitcore-exploradores"
que foram obtidos via NPM.

> var bitcore = require ( 'bitcore');
> var exploradores = require ( 'bitcore-exploradores');

Após isso, foi utilizada a função Insight().

> var visão = new explorers.Insight ();

### Passo 3
Criado a carteira e enviando Bitcoin de um endereço para outro. 
E necessário criar uma chave pública usando o hash SHA-256 da chave privada.
Para gerar a chave privada foi necessário ir ao site rushwallet.com, através deste site foi obtido o "endereço bitcoin". 
Este endereço foi copiado e armazenado no arquivo blockchainTransaction.js como uma variável pública.

No site rushwallet foi possível "exportar a chave" e então copiá-la no arquivo blockchainTransaction.js como a variável "PrivateKey".

 > var bitcore = require ( 'bitcore');
 > var exploradores = require ( 'bitcore-exploradores');
 > var visão = new explorers.Insight ();

 > var publicAddress = '1DuFRRFEJvchWpTQiDqMk3DW3mP9XZ3UTa';
 > var PrivateKey = '5KG7bZhGX5jaCD46cxbN1tX6nq1zSa4gAZ4baKmw277RKGbH3qc'
 
 Foi definida também uma taxa de mineração, conforme abaixo:
 
 > var minerFee = 667;
 
 A mensagem enviada para a Blockchain foi:
 
> var blockchainMessage = 'Olá Satoshi!';

Abaixo um exemplo de envio de um centavo para um endereço de teste.

 > var bitcore = require ( 'bitcore');
 > var exploradores = require ( 'bitcore-exploradores');
 > var visão = new explorers.Insight ();

 > var publicAddress = '18JYiBktnAzbS2sEZSrdKgSEFwLjXvW9Uy';
 > var PrivateKey = '5HxKWX4pkze3AiB4yWrdZKMYrf9hWYdAVp3TnkpYMiGbxnLuLWN'

 > insight.getUnspentUtxos (publicAddress, função (erro, utxos) {
 > console.log ( 'utxos' + ':' + JSON.stringify (utxos, indefinido, 2));
 > });
 
 A resposta deve ser semelhante a a esta:
 
> utxos: [
>	 {
>	 "Endereço": "18JYiBktnAzbS2sEZSrdKgSEFwLjXvW9Uy",
>	 "Txid": "6c2e97cd10906ad89fdd10c1f068fc20ecc709a9dcc152dab1d7a2c7118a4158",
>	 "Vout": 1,
>	 "ScriptPubKey": "76a914501a6c0e1e7030100a9a3cdc14b906760fc45bb388ac",
>	 "Quantidade": 0.000042
>	 }
> ]  

## 
Bem-vindo

