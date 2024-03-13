### CAP-теорема и СУБД

Теорема CAP (Consistency, Availability, Partition tolerance) утверждает, что в распределённой системе данных можно обеспечить только два из трёх следующих свойств: согласованность (Consistency), доступность (Availability) и устойчивость к разделению (Partition tolerance).

[**DragonFly:**](https://www.dragonflydb.io/) 

> Dragonfly is a simple, performant, and cost-efficient in-memory data store. Dragonfly is fully compatible with Redis APIs but without the Redis management complexity.

Так как СУБД позиционируется как in-memory, то разговора о partition tolerance идти не может. Причем на сайте сказано, что данная СУБД делает акцент на high availability, таким образом DragonFly относится к CA.

[**ScyllaDB:**](https://www.scylladb.com/scylladb-vs-cassandra/) 

> With ScyllaDB you will achieve higher performance at scale using dramatically fewer nodes, with far less administration, and lower infrastructure costs.

ScyllaDB, как и Cassandra (на котором он базируется), стремится к  AP-модели, обеспечивая высокую доступность и устойчивость к разделению, допуская при этом потенциальные проблемы с согласованностью в некоторых ситуациях.

[**ArenadataDB:**](https://arenadata.tech/products/arenadata-db/) 

> Arenadata DB (ADB) — аналитическая, распределённая СУБД, построенная на MPP-системе с открытым исходным кодом Greenplum. 
> Полное соответствие принципам строгой изоляции транзакции (принципы ACID). Одни и те же таблицы могут быть использованы для записи и чтения, без страха потерять данные.

Как заявлено на официальном сайте, СУБД поддерживает принципы ACID, что говорит о соблюдении consistency, при этом так же делается акцент на partition tolerance, а значит относится к CP
