# ![Power BI](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/New_Power_BI_Logo.svg/29px-New_Power_BI_Logo.svg.png) Desafio de projeto

O desafio tem como proposta a criação de uma instância MySQL na Azure e a modelagem simples de um banco de dados pré-definido pela professora ministrando do módulo e a partir dele realizar ajustes na estrutura e a importação dos dados para o Power BI, transformá-las e montar um relatório.

## Respondendo perguntas do docx

11.	Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.
~~~SQL
-- Query utilizada

SELECT CONCAT(m.Fname, " ", m.Lname) AS Nome_gerente, CONCAT(e.Fname, " ", e.Lname) AS Nome_colaborador FROM employee m
	JOIN departament d ON m.Ssn = d.Mgr_ssn
		LEFT JOIN employee e ON e.Super_ssn = d.Mgr_ssn;
~~~

13.	Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro. 

14.	Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir. 

> **RESPOSTA:** Devido a opção de escolher um separador entre as colunas à mesclar, podemos colocar um caracter padrão pra caso haja necessidade futura de separá-las irá ficar de fácil separação.

O relatório está disponível no repositório - [Repositório](https://github.com/KevinSRodrigues/desafio-projeto-DIO.git)

**Jesus te Ama!** ❤️​