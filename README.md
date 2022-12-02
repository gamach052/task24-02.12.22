###  [Task 8 kyu](https://www.codewars.com/kata/5601c5f6ba804403c7000004/train/java)

The medians of a triangle are the segments that unit the vertices with the midpoint of their opposite sides. The three medians of a triangle intersect at the same point, called the barycenter or the centroid. Given a triangle, defined by the cartesian coordinates of its vertices we need to localize its barycenter or centroid.

The function bar_triang() or barTriang or bar-triang, receives the coordinates of the three vertices A, B and C as three different arguments and outputs the coordinates of the barycenter O in an array [xO, yO]

This is how our asked function should work: the result of the coordinates should be expressed up to four decimals, (rounded result).

You know that the coordinates of the barycenter are given by the following formulas. 


### My solution
```Java
class Barycenter {

    public static double[] barTriang(double[] x, double[] y, double[] z)
    {
        double [] arr = new double[2];
        arr[0] = (double)((int)Math.round((x[0] + y[0] + z[0])/3*10000))/10000;
        arr[1] = (double)((int)Math.round((x[1] + y[1] + z[1])/3*10000))/10000;
        return arr;
    }
}


```

### Fav solution
```Java
import java.text.DecimalFormat;

class Barycenter {

    public static double[] barTriang(double[] x, double[] y, double[] z)
    {
        double[] coordinates = new double[2];

        for(int i=0;i<2;i++){
            coordinates[i] = Double.parseDouble(new DecimalFormat("##.####").format((x[i]+y[i]+z[i])/3));
        }

        return coordinates;
    }
}
```
I like this solution because I like it
