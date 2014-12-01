ER Diagram: Blog
```
     +-----+------------------------------------------------+---------------------------+
+----+-----+                                              / | \                       / | \
| Authors  |       +-------------------+           +--------+---------+       +---------+---------+
+----------+      /| Posts             |           |Comments          |       | Subcomment        |
| omniauth |     / +-------------------+          /+------------------+      /+-------------------+
|          +-------+ title, string, NF |         / |title, string, NF |     / | title, string, NF |
+----------+     \ | content, text, NF +-----------+text, text, NF    +-------+ text, text, NF    |
                  \| author_id         |         \ |author_id         |     \ | author_id         |
                   | categorization_id |          \|post_id           |      \| comment_id        |
                   | timestamps        |           |                  |       |                   |
                   +----------+--------+           +------------------+       +-------------------+
                             /|\
                       +------+----------+        +--------------------+
                       |Categorizations  |        | Categories         |
                       +-----------------+\       +--------------------+
                       |name, string, NF +--------+ name, string, NF   |
                       |                 |/       | categorizations_id |
                       +-----------------+        +--------------------+
```

ER Diagram: Site
```


