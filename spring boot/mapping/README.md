# Примеры коды

```
@Mapper(componentModel = "spring")
public interface ObjectMapper {

    @Mapping(source="fieldFromDto", target="filedFromEntity")
    @Mapping(source="fieldFromDto2", target="filedFromEntity2")
    Entity toEntity(Dto dto);
}
```

* ``` @Mapper(componentModel = "spring") ``` - используем в Spring boot
* ``` @Mapping(source="fieldFromDto", target="filedFromEntity") ``` - если в объектах ```dto``` и ```entity``` разные названия полей и их нужно сопоставить друг с другом, то используем ```@Mapping```. В ```source=""``` используем поле из входящего объект (в данном случае ```dto```), в ```target=""``` используем выходной объект (в данном случае ```entity```). Можно использоать несколько ```@Mapping()``` если хотим сопоставить несколько полей.