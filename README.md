# Spring core

## IoC Conteiner
Inversion of Control principle ==> is a principle of design of software implemented by spring boot
The control is inverted: who creates and provides the dependencies is a container => the IoC container.

DI - Dependency injection
Instead of your code instanciating the objects it need, you just declare what it needs.

org.springframework.beans and org.springframework.context areth basis for SpringFramework IOC container.

## Bean Factory
Interface who provides an advanced configuration mechanism capable of managing any type of object.

## Bean
Is an object that is instanciated, assembled and managed by a Spring IoC container. Is one of many objects in your application.

## Application Context
Subinterface of Bean Factory and adds some mechanisms as message resource handling and easier integration with Spring AOP features.

## Conteiner Overview
org.springframework.context.ApplicationContext interface represents the Spring IoC container and is responsible for instantiating, configuring and assembling the **beans**
The container get its instructions on the components to instantiate, configure and assemble by reading configuration metadata.

**Configuration metadata**
Can be represented as annotated component classes, configuration classes with factory methods or external XML files or groovy scripts.
With either format, you may compose your application and the rich interdependencies between those components.
Examples:
- Annotates component classes:
@Component, @Service, @Repository
Spring scan those components and create the beans to you

- Java based configuration
Use a class java with @Configuration and the beans are created using @Bean
@Import - indicates one or more components classes to import - typically @Configuration classes. 
@DependsOn - Beans on which the current bean depends

-XML Configuration
Definition of the beans are made with an XML file and the context are loaded with:
ApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");


