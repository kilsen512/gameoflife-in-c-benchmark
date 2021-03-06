# Game of Life in C Benchmark

## performance optimization  
500 iterations using 1000x1000 matrix  

ubuntu 15.04  
Intel Core 2 Duo CPU P8400 @ 2.26GHz * 2  
2.9 GiB RAM  

### Version 1:  
working version including one testcase  
no parallelizations  
1st run: 41.36475s  
2nd run: 41.29861s  
3rd run: 41.31800s  

### Version 1.1:  
check Fields using inline functions  
1st run: 38.26025s  
2nd run: 38.40372s  
3rd run: 38.39163s  

### Version 2:  
switched algorithm to only be active if field is one  
1st run: 14.01448s (500084 ones in initial matrix)  
2nd run: 14.18841s (499864)  
3rd run: 14.25374s (499343)  

### Version 3:  
added parallelization  
1st run: 12.349921s (499538)  
2nd run: 12.693045s (499712)  
3rd run: 12.428803s (500223)  

### Version 3.1:  
added more parallelization for matrix operations  
1st run: 8.018553s (499448)  
2nd run: 8.124357s (499328)  
3rd run: 8.089620s (500540)

## usage
just run `make` OR  
`make testcase` to create a simple testcase
