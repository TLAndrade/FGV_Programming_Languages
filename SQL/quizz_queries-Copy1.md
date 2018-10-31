Sobre o banco de dados "classicmodels", indique as queries para obter as seguintes informações:

- Quantos registros há na tabela "customers"?
- Na tabela "customers", quantos clientes (" customersName") têm nome iniciado pela letra "M"?
- Na tabela "customers", crie uma saída que concatene nomes e sobrenomes em uma única coluna.
- Agora repita a query acima, mas com todas as letras em maiúsculo, e ordene pelo sobrenome.
- Na tabela "payments", selecione os registros ordenados por volume ("amount") e data de pagamento ("paymentDate")
- Na tabela "employees", indique quantos nomes de cargos ("jobTitle") únicos existem? 
- Qual destes cargos ("jobTitle") possuem mais funcionários?


1-select * from customers;
    há 13 registros
    
2-select customerName from customers where customerName regexp '^[M]{1}.*';
    há 14 clientes.
    
3-select concat(contactFirstName,contactLastName) from customers;

-select upper(concat(contactFirstName,contactLastName)) from customers order by contactLastName;

7-select jobTitle,count(jobTitle) as soma from classicmodels.employees group by jobTitle;