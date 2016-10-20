# MultiTypeTemplates
An intellij idea plugin for Android to generate `MultiType` `Item` and `ItemViewProvider` easily.

#### Usage

`Right click` your packge/directory - `New` - `MultiType Item`, then input your name of Item to generate Item and ItemViewProvider files and codes.

![](http://ww4.sinaimg.cn/large/86e2ff85gw1f8yj0sejd6j21340ben1s.jpg)

Example: If you input "Category", it will generate the `Category.java` and `CategoryViewProvider.java`:

```java
public class Category implements Item {

}
```

```java
public class CategoryViewProvider
        extends ItemViewProvider<Category, CategoryViewProvider.ViewHolder> {

    @NonNull @Override protected ViewHolder onCreateViewHolder(
            @NonNull LayoutInflater inflater, @NonNull ViewGroup parent) {
        View root = inflater.inflate(R.layout.item_category, parent, false);
        return new ViewHolder(root);
    }
    

    @Override protected void onBindViewHolder(
            @NonNull ViewHolder holder, @NonNull Category category) {

    }

    
    static class ViewHolder extends RecyclerView.ViewHolder {

        ViewHolder(View itemView) {
            super(itemView);
        }
    }
}
```
