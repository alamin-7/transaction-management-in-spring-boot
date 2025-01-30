# transaction-management-in-spring-boot
This repo is for exploring transaction management in spring boot with a payment method project

-> simple Transactional Management implementation
i. Annotated Main class as @EnableTransactionManagement 
ii. Annotated The method as @Transactional

-> What happen when use @Transactional
Temporary memory = Hibernate’s Persistence Context (first-level cache).
Spring keeps changes in memory (RAM) until commit.
If transaction is successful → Hibernate flushes data to DB.
If transaction fails → Hibernate discards temporary data.
