## Query:

```
> SELECT * FROM shirt;
```

## SQL Result:

╒═════════════╕
│ shirt_color │
╞═════════════╡
│ GREEN       │
├─────────────┤
│ BLUE        │
├─────────────┤
│ PURPLE      │
╘═════════════╛

## Visual Representation:

╒════════════════════╕
│                    │
│                  │
│   GREEN    BLUE    │
│                    │
│                   │
│       PURPLE       │
│                    │
╘════════════════════╛

## Query:

```
> SELECT * FROM pants;
```

## SQL Result:

╒═════════════╕
│ pants_color │
╞═════════════╡
│ GREEN       │
├─────────────┤
│ BLUE        │
├─────────────┤
│ PINK        │
╘═════════════╛

## Visual Representation:

╒════════════════════╕
│                    │
│     👖      👖     │
│   GREEN    BLUE    │
│                    │
│         👖         │
│        PINK        │
│                    │
╘════════════════════╛

## Query:

```
> SELECT * FROM shirt INNER JOIN pants ON shirt.shirt_color = pants.pants_color;
```

## SQL Result:

╒═════════════╤═════════════╕
│ shirt_color │ pants_color │
╞═════════════╪═════════════╡
│ GREEN       │ GREEN       │
├─────────────┼─────────────┤
│ BLUE        │ BLUE        │
╘═════════════╧═════════════╛

## Visual Representation:

╒════════════════════╕
│                    │
│                  │
│     👖      👖     │
│   GREEN    BLUE    │
│                    │
╘════════════════════╛

## Query:

```
> SELECT * FROM shirt LEFT JOIN pants ON shirt.shirt_color = pants.pants_color;
```

## SQL Result:

╒═════════════╤═════════════╕
│ shirt_color │ pants_color │
╞═════════════╪═════════════╡
│ GREEN       │ GREEN       │
├─────────────┼─────────────┤
│ BLUE        │ BLUE        │
├─────────────┼─────────────┤
│ PURPLE      │ <null>      │
╘═════════════╧═════════════╛

## Visual Representation:

╒════════════════════╕
│                    │
│                  │
│     👖      👖     │
│   GREEN    BLUE    │
│                    │
│                   │
│                    │
│       PURPLE       │
│                    │
╘════════════════════╛

## Query:

```
> SELECT * FROM shirt RIGHT JOIN pants ON shirt.shirt_color = pants.pants_color;
```

## SQL Result:

╒═════════════╤═════════════╕
│ shirt_color │ pants_color │
╞═════════════╪═════════════╡
│ GREEN       │ GREEN       │
├─────────────┼─────────────┤
│ BLUE        │ BLUE        │
├─────────────┼─────────────┤
│ <null>      │ PINK        │
╘═════════════╧═════════════╛

## Visual Representation:

╒════════════════════╕
│                    │
│                  │
│     👖      👖     │
│   GREEN    BLUE    │
│                    │
│                    │
│         👖         │
│        PINK        │
│                    │
╘════════════════════╛
