# Basics-in-Numpy:
----------------------------------------------------------------------------------------------------------------------------------
What is Numpy?:
----------------

    NumPy – Numerical Python.
    It is a library consisting of multi-dimensional array objects and a vast number of functions for 
    processing those multi-dimensional arrays.
    It is a Open Source!.
    It performs
      - Mathematical and logical operations on arrays
      - Operations related to linear algebra.
      - Random number generations (1D and nD array ) 

Defining an array: (ndarray):
-----------------------------
    Syntax: 
        arr=numpy.array(object, dtype=None, ndmin=0)

    e.g:
        a=np.array([[[5,3],[4,2],[3,1]],[[5,3],[4,2],[3,1]],[[5,3],[4,2],[3,1]]])  #3D array 
        print(a)
        print(a.shape)			# (3, 3, 2)  ---> (dimension,row,column)

Datatypes in numpy:
-------------------
    Syntax:
        dt=np.dtype(<type>)
        
    Types:
        bool_     - Boolean (True or False)
        int_      - Default integer type (either int64 or int32)  
        int8      - Byte (-128 to 127)
        int16     - Integer (-32768 to 32767)
        int32     - Integer (-2147483648 to 2147483647)
        int64     - Integer (-9223372036854775808 to 9223372036854775807)
        uint8     - Unsigned integer (0 to 255)
        uint16    - Unsigned integer (0 to 65535)
        uint32    - Unsigned integer (0 to 4294967295)
        uint64    - Unsigned integer (0 to 18446744073709551615)
        float_    - Shorthand for float64
        float16   - Half precision float: sign bit, 5 bits exponent, 10 bits mantissa
        float32   - Single precision float: sign bit, 8 bits exponent, 23 bits mantissa
        float64   - Double precision float: sign bit, 11 bits exponent, 52 bits mantissa 
        complex_  - Shorthand for complex128
        complex64 - Complex number, represented by two 32-bit floats (real and imaginary components)
        complex128 - Complex number, represented by two 64-bit floats (real and imaginary components)
        
<arr>.ndim:
-----------------------------------
    
    This function will return the dimension of the numpy array.

    e.g:
        a=np.arange(1200)			# will create random 1200  1D elements
        b=a.reshape(3,20,20)		# depth=3, height=20, width=20
        print(b.shape)				# (3,20,20)
        print(b.ndim)				# 3

Reshaping an array:
-----------------------------------

    Reshaping an array can be done in two ways.
            i) <arr>.shape=(dim,row,column)
            ii) <arr>.reshape(dim,row,column)
            iii) ndmin parameter for dimensions

Reshaping an array using <arr>.shape
-----------------------------------
    
    This function will reshape the original array.
    
    Syntax:
        <arr>.shape=(dimension, row, column)
        
    e.g:
     a=np.array([1,2,3,4,5,6,7,8,9])
     a.shape=(3,3)
     print(a)		# 3x3 2D array  
     print (a.shape) # (3,3)

    a=np.array([1,2,3,4,5,6,7,8,9])
    a.shape=(1,3,3)
    print(a)		# 1x3x3 3D array
    print (a.shape) #(1,3,3)

    a=np.array([1,2,3,4,5,6,7,8,9])
    a.shape=(1,4,4)	# error since no of element is less for the given dimension
    print(a)		 
    print (a.shape) 

Reshaping an array using <arr>.reshape()
------------------------------------------

    This function will return the reshaped array as new array.
    
    Syntax:
        <arr>.reshape(dimension, row, column)
        
    e.g:
        a=np.array([1,2,3,4,5,6,7,8,9])
        b=a.reshape(3,3)
        print(b)		# 3x3 2D array  
        print (b.shape) # (3,3)

        c=a.reshape(1,3,3)
        print(c)		# 1x3x3 3D array
        print (c.shape) #(1,3,3)

        d=a.reshape(1,4,4)	# error since no of element is less for the given dimension
        print(d)		 
        print (d.shape) 
        
Some numpy functions:
----------------------

    NumPy has some useful function to generate the n dimensional arrays. They are,
        - numpy.zeros()
        - numpy.ones()
        - numpy.full()
        - numpy.eye()
        - numpy.random.random()

zeros():
-------

    For the given  dimension, this function will  generate the given dimensional array which filled with zeros.
    
    Syntax:
        numpy.zeros((dimension, row, column))
        
    e.g:
        a=np.zeros((2,2)) 		 #2D array
        print(a)
        print(a.shape)		# (2,2)  array of having all zero elements

        a=np.zeros((3,4,4))  	#3D array
        print(a)
        print(a.shape)		# (3,4,4) array of having all zero elements

        a=np.zeros((10,3,4))  	#10D array
        print(a)
        print(a.shape)		# (10,3,4) array of having all zero elements










