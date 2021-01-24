# numbaplota

Plotting values in the terminal. Simply feed one or two columns of data (delimited by a space) and this plots it.

## Examples

Sine wave:

```
$ python3 -c 'import math; print("\n".join([f"{i/10} {math.sin(i/10)}" for i in range(70)]))' > sin.txt
$ cat sin.txt | ./numbaplota 
 1.1 |                                                                                 
 1.0 |               *** ***                                                           
 0.9 |              *       **                                                         
 0.9 |             *          *                                                        
 0.8 |            *            *                                                       
 0.8 |           *               *                                                     
 0.7 |          *                                                                      
 0.7 |        *                   *                                                    
 0.6 |                             *                                                   
 0.6 |       *                                                                       * 
 0.5 |      *                       *                                              *   
 0.5 |                               *                                                 
 0.4 |     *                                                                      *    
 0.4 |                                *                                                
 0.3 |    *                                                                      *     
 0.3 |                                 *                                        *      
 0.2 |   *                                                                             
 0.2 |                                  *                                      *       
 0.1 |  *                                                                              
 0.1 | *                                  *                                   *        
-0.0 |                                                                                 
-0.1 |                                     *                                 *         
-0.1 |                                      *                                          
-0.2 |                                                                     *           
-0.2 |                                       *                                         
-0.3 |                                                                    *            
-0.3 |                                        *                                        
-0.4 |                                                                   *             
-0.4 |                                         *                        *              
-0.5 |                                                                                 
-0.5 |                                          *                      *               
-0.6 |                                           *                    *                
-0.6 |                                                                                 
-0.7 |                                             *                 *                 
-0.7 |                                              *               *                  
-0.8 |                                               *            *                    
-0.8 |                                                *          *                     
-0.9 |                                                 *        *                      
-0.9 |                                                  ** * ***                       
-1.0 |                                                      *                          
-1.1 |                                                                                 
      - 0 0 0 0 0 1 1 1 1 1 1 2 2 2 2 2 2 3 3 3 3 3 4 4 4 4 4 4 5 5 5 5 5 5 6 6 6 6 6 7
      0 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
      . 1 3 4 6 8 0 1 3 5 7 9 0 2 4 6 7 9 1 3 5 6 8 0 2 3 5 7 9 0 2 4 6 7 9 1 3 5 6 8 0
```

Circle

```
$ python -c 'import math; print("\n".join([f"{i/10} {math.sqrt(25 - (i/10 - 5)**2)}" for i in range(101)]))' > circle.txt
$ python -c 'import math; print("\n".join([f"{i/10} {-math.sqrt(25 - (i/10 - 5)**2)}" for i in range(101)]))' >> circle.txt
$ cat circle.txt | ./numbaplota 
 5.3 |                                                                                 
 5.0 |                           **************************                            
 4.7 |                      *****                          *****                       
 4.5 |                   ****                                  ****                    
 4.2 |                ***                                          ***                 
 3.9 |              **                                                **               
 3.7 |           ***                                                    ***            
 3.4 |          **                                                        **           
 3.2 |        **                                                            **         
 2.9 |       **                                                              **        
 2.6 |     **                                                                  **      
 2.4 |    *                                                                      *     
 2.1 |    *                                                                      *     
 1.8 |   *                                                                        *    
 1.6 |  *                                                                          *   
 1.3 |                                                                                 
 1.1 | *                                                                            *  
 0.8 |                                                                                 
 0.5 |                                                                                 
 0.3 | *                                                                             * 
-0.0 |                                                                                 
-0.3 |                                                                                 
-0.5 |                                                                                 
-0.8 | *                                                                            *  
-1.1 |                                                                                 
-1.3 |  *                                                                          *   
-1.6 |   *                                                                        *    
-1.8 |    *                                                                      *     
-2.1 |    *                                                                      *     
-2.4 |     **                                                                  **      
-2.6 |       **                                                              **        
-2.9 |        **                                                            **         
-3.2 |          **                                                        **           
-3.4 |           ***                                                    ***            
-3.7 |              **                                                **               
-3.9 |                ***                                          ***                 
-4.2 |                   ****                                  ****                    
-4.5 |                      *****                          *****                       
-4.7 |                           **************************                            
-5.0 |                                                                                 
      - 0 0 0 0 1 1 1 1 2 2 2 2 3 3 3 4 4 4 4 5 5 5 5 6 6 6 6 7 7 7 7 8 8 8 8 9 9 9 9 1
      0 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 0
      . 1 4 6 9 2 4 7 9 2 4 7 9 2 5 7 0 2 5 7 0 3 5 8 0 3 5 8 1 3 6 8 1 3 6 8 1 4 6 9 .
                                                                                       
```

X^2

```
$ python3 -c 'import math; print("\n".join([f"{i/10} {(i/10)**2}" for i in range(100)]))' > x2.txt
$ ./numbaplota x2.txt 
100.6 |                                                                                
 98.0 |                                                                              * 
 95.4 |                                                                             *  
 92.9 |                                                                            *   
 90.3 |                                                                           *    
 87.7 |                                                                          *     
 85.1 |                                                                        **      
 82.5 |                                                                       *        
 80.0 |                                                                      **        
 77.4 |                                                                     *          
 74.8 |                                                                   **           
 72.2 |                                                                   *            
 69.6 |                                                                 **             
 67.1 |                                                                *               
 64.5 |                                                               **               
 61.9 |                                                              *                 
 59.3 |                                                            **                  
 56.7 |                                                           **                   
 54.2 |                                                         **                     
 51.6 |                                                        *                       
 49.0 |                                                       **                       
 46.4 |                                                     **                         
 43.8 |                                                    *                           
 41.3 |                                                  **                            
 38.7 |                                                 *                              
 36.1 |                                              ***                               
 33.5 |                                             *                                  
 31.0 |                                           **                                   
 28.4 |                                         **                                     
 25.8 |                                       **                                       
 23.2 |                                     **                                         
 20.6 |                                  ***                                           
 18.1 |                                ***                                             
 15.5 |                             ***                                                
 12.9 |                           **                                                   
 10.3 |                       ****                                                     
  7.7 |                   ****                                                         
  5.2 |              *****                                                             
  2.6 | *************                                                                  
 -0.0 |                                                                                
       - 0 0 0 0 1 1 1 1 2 2 2 2 3 3 3 3 4 4 4 5 5 5 5 6 6 6 6 7 7 7 7 8 8 8 8 9 9 9 9 
       0 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 
       . 1 4 6 9 1 4 6 9 2 4 7 9 2 4 7 9 2 4 7 0 2 5 7 0 2 5 7 0 2 5 7 0 3 5 8 0 3 5 8 
       1                                                                               
```
