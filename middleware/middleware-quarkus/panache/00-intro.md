In this scenario, you will get an introduction to **Panache**, one of the features of [Quarkus](https://quarkus.io).

## What is Panache?

Hibernate ORM is the de facto JPA implementation and offers you the full breadth of an Object Relational Mapper. It makes complex mappings possible, but many simple and common mappings can also be complex. Hibernate ORM with **Panache** focuses on making your entities trivial and fun to write and use with Quarkus.

With Panache, we took an opinionated approach to make hibernate as easy as possible. Hibernate ORM with Panache offers the following:

* By extending `PanacheEntity` in your entities, you will get an ID field that is auto-generated. If you require a custom ID strategy, you can extend `PanacheEntityBase` instead and handle the ID yourself.

* By using Use public fields, there is no need for functionless getters and setters (those that simply get or set the field). You simply refer to fields like `Person.name` without the need to write a `Person.getName()` implementation. Panache will auto-generate any getters and setters you do not write, or you can develop your own getters/setters that do more than get/set, which will be called when the field is accessed directly.

* The `PanacheEntity` superclass comes with lots of super useful static methods and you can add your own in your derived entity class, and much like traditional object-oriented programming it's natural and recommended to place custom queries as close to the entity as possible, ideally within the entity definition itself. Users can just start using your entity `Person` by typing `Person`, and getting completion for all the operations in a single place.

* You don't need to write parts of the query that you don’t need: write `Person.find("order by name")` or `Person.find("name = ?1 and status = ?2", "stef", Status.Alive)` or even better `Person.find("name", "stef")`.

That’s all there is to it: with Panache, Hibernate ORM has never looked so trim and neat.

### Other possibilities

Learn more at [quarkus.io](https://quarkus.io), or just drive on and get hands-on!