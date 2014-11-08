underscorePlus
==============

Underscore Plus


A simple set of additions to underscore.js

## _.exists

The main and most useful part is just: 

``` _.exists(value) ```

which fails if value is either null or undefined.



## _.isReachabl

The other main utilyt added is:


```
var points =  _.isReachable(stats, "season.yearly.offense.points", "N/A");
```

Which will traverse the stats object withouf failing on any intermediate key:

```
stats.seasaon.yearly.offense.points
```
Without the need of writting:


```
if ( stats.season && stats.yearly && stats.yearly.offense) {
    var points = stats.seasaon.yearly.offense.points;
}

```







TODO:

- make it possible to have isReachable take functions, but most importantly array indexes
- have optional keys such that we can travers complex structures with minor differences:


We only care about x

But we might have objects such as:

```
a.b.c.d.e.f.x

&

a.b.c.d.e.m.x


&

a.b.c.d.e.g.x

```


Or maybe the last variable is either x,y or z.






