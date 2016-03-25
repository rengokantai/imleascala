##### imleascala
#####5
######2 curry
basic example:
```
def curry(x:Int)(y:Int) = x+y
```
more
```
def curry(x:Int)(y:Int) = x+y
def curry2 = curry(1)
curry3 = curry2(1) //2
#####6
######1 list basic
```
val a = 1::2::Nil
val b =List(3,4,5):::a
```
######5 stream
```
1#::2#::3#::Stream.empty
```
lazy eval
```
(1 to 10000).toStream
```
######6 tuple
syntax:
```
1->2
(1,2)
```

return three-item tuple: number of elem in tuple, sum of tuple, sum of square of tuple

```
val a = List(1,2,3)

def sumTup(in:List[int]):(Int,Int,Int) = {in.foldLeft((0,0,0))((t,v=>(t._1+1,t._2+v, t._3+v*v))

sumTup(a)  //3,6,14
```

Map
```
val m = Map(1->"a", 2->"b")
m.contains(1)
m+(3->"c")
m-3 //delete 3->"c"
m++ List(3->"c",4->"d") //append list of map
m--List(1,2)
```
######7 quicksort
//paste mode
```
scala> :paste     (ctrl D finish editing)
```

full code:
```scala
def quick(in:List[Int]):List[Int] = {
if in.length<2 in
else quick(in.filter(_<in.head) ++ in.filter(_==in.head) ++ quick(in.filter(_>in.head) 
}
quick(4,2,3,1)
```

