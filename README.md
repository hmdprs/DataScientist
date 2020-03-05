# Kaggle Learn

These micro-courses are the single fastest way to gain the skills you'll need to do independent data science projects.

## **Python**

Learn the most important language for data science.

### [Hello, Python](https://www.kaggle.com/colinmorris/hello-python)

- Variable Assignment
- Function Calls
- Numbers and Arithmetic in Python
  ```py
  a / b     # true division
  a // b    # floor division
  a % b     # modulus
  a ** b    # exponentiation
  ```
- Order of Operators: **PEMDAS**
- Builtin Functions for Working with Numbers
  ```py
  min()
  max()
  abs()
  int()
  float()
  ```

### [Functions and Getting Help](https://www.kaggle.com/colinmorris/functions-and-getting-help)

- Getting Help
  ```py
  help()
  ```
- Defining Functions
- Docstrings, returns by `help()`
  ```py
  """ docstring """
  ```
- Functions that don't Return
- Default Arguments
  ```py
  print(..., sep='\t')
  ```
- Functions Applied to Functions
  ```py
  fn(fn(arg))
  string.lower().split()
  ```

### [Booleans and Conditionals](https://www.kaggle.com/colinmorris/booleans-and-conditionals)

- Booleans
  - Comparison Operations
    ```py
    a == b    # a equal to b
    a != b    # a not equal to b
    a < b     # a less than b
    a > b     # a greater than b
    a <= b    # a less than or equal to b
    a >= b    # a greater than or equal to b
    ```
  - Combining Boolean Values
    - Order of Operators, use `()` for clarity & readability
      ```py
      ()
      **
      +x, -x, ~x
      *, /, //, %
      +, -
      <<, >>
      &
      ^
      |
      ==, !=, >, >=, <, <=, is, is not, in, not in
      not
      and
      or
      ```
- Conditionals
  ```py
  if
  elif
  else
  ```
- Boolean Conversion
  - `bool()`
  - all numbers are treated as true, except `0`
  - all strings are treated as true, except the empty string `""`
  - empty sequences (strings, lists, tuples, sets)  are "falsey" and the rest are "truthy"
- Conditional Expressions (aka 'ternary')
  - Setting a variable to either of two values depending on some condition
  - 1-line-form:
    ```py
    outcome = 'failed' if grade < 50 else 'passed'
    ```

### [Lists](https://www.kaggle.com/colinmorris/lists)

- Lists
  - `[]` + mutable + a mix of different types of variables
       - Indexing
         - `0` is first, `-1` is last
  - Slicing
    ```py
    planets[:3]
    planets[-3:]
    ```
  - Changing Lists
    ```py
    planets[:3] = ['Mur', 'Vee', 'Ur']
    ```
  - List Functions
    ```py
    len()
    sorted()
    max()
    sum()
    any()
    ```
  - Methods
    ```py
    c = 12 + 5j
    c.imag
    c.real
    x = 12
    x.bit_length()
    help(x.bit_length)
    help(int.bit_length)
    ```
  - List Methods
    ```py
    list.append()
    help(list.append)
    list.pop()
    list.index()
    in
    ```
    - to find all methods: `help(list)`
- Tuples
  - `()` or `, , ,` + **immutable**
  ```py
  x = 0.125
  numerator, denominator = x.as_integer_ratio()
  ```

### [Loops and List Comprehensions](https://www.kaggle.com/colinmorris/loops-and-list-comprehensions)

- Loops
  - `for _ in _:`
       - in every iteratable objects: list, tuples, strings, ...
       - `range()`
       - `while` loops
- List Comprehensions
  ```py
  squares = [n**2 for n in range(10)]
       short_planets = [planet.upper() + "!" for planet in planets if len(planet) < 6]
       [32 for planet in planets]
  ```
       - with functions like `min()`, `max()`, `sum()`, `any()`:
         ```py
    return len([num for num in nums if num < 0])
         return sum([num < 0 for num in nums])
         return any([num % 7 == 0 for num in nums])
    ```
- Solving a problem with less code is always nice, but it's worth keeping in mind the following lines from **The Zen of Python** (`import this`):
  > Readability counts.<br>
  > Explicit is better than implicit.

### [String and Directories](https://www.kaggle.com/colinmorris/strings-and-dictionaries)

- Strings
  - `''` or `""` or `""" """`
  - Escaping
    | you type | you get | example                   | print(example)         |
    | -------- | ------- | ------------------------- | ---------------------- |
    | `\'`     | `'`     | `'What\'s up?'`           | `What's up?`           |
    | `\"`     | `"`     | `"That's \"cool\""`       | `That's "cool" `       |
    | `\\`     | `\`     | `"Look, a mountain: /\\"` | `Look, a mountain: /\` |
  - Strings are Sequences, same as lists, but they are **Immutable**
    ```py
    [char + '! ' for char in planet]
    ```
  - String Methods
    ```py
    str.upper()
    str.lower()
    str.index()
    str.startswith()
    str.endswith()
    ```
    - Going between strings and lists:
      ```py
      year, month, day = datestr.split('-')
      '/'.join([month, day, year])
      ```
    - Building strings
      ```py
      " ".format()
      f" "
      ```
    - From Exercise:
      ```py
      # Iterate through the indices (i) and elements (doc) of documents
      for i, doc in enumerate(documents):
          print(i, doc)
      ```
- Dictionaries
  - Pairs of (Keys, Values)
    ```py
    numbers = {'one':1, 'two':2, 'three':3}
    numbers['one']
    numbers['eleven'] = 11
    ```
  - Dictionary Comprehensions
    ```py
    planets = ['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune']
    planet_to_initial = {planet: planet[0] for planet in planets}
    ```
  - `in`
  - Loops
    - A for loop over a dictionary will loop over its Keys
    - Access to all the Keys or all the Values
      ```py
      dict.keys()
      dict.values()
      ' '.join(sorted(planet_to_initial.values()))
      ```
    - In Python jargon, an `item` refers to a (key, value) pair
      ```py
      for planet, initial in planet_to_initial.items():
          print("{} begins with \"{}\"".format(planet, initial))
      ```
  - `help(dict)`

### [Working with External Libraries](https://www.kaggle.com/colinmorris/working-with-external-libraries)

- Imports
  - Simple Import, `.` Access
    ```py
    import math
    math.pi
    ```
  - `as` Import, short `.` Access
    ```py
    import math as mt
    mt.pi
    ```
  - `*` Import, Simple Access
    ```py
    from math import *
    pi
    ```
  - Combined
    ```py
    # The problem of * Import is that some modules (ex. `math` and `numpy`) have functions with same name (ex. `log`) but with different semantics. So one of them overwrites (or "shadows") the function. The solution is:
    from math import log, pi
    from numpy import asarray
    ```
- Submodules
  - Modules contain variables which can refer to functions or values. Sometimes they can also have variables referring to other modules.
    ```py
    import numpy
    dir(numpy.random)
    >>> ['set_state', 'shuffle', 'standard_cauchy', 'standard_exponential', 'standard_gamma', 'standard_normal', 'standard_t', 'test', 'triangular', 'uniform', ...]

    rolls = numpy.random.randint(low=1, high=6, size=10)
    rolls
    >>> array([3, 2, 5, 2, 4, 2, 2, 3, 2, 3])
    ```
  - Get Help
    - Standard Python datatypes are: `int`, `float`, `bool`, `list`, `string`, and `dict`. But as you work with various libraries for specialized tasks, you'll find that they define their own types. For example datatypes for **matplotlib** are `Subplot`, `Figure`, `TickMark`, and `Annotation`, for **pandas** are `DataFrame` and `Serie`, and for **tensorflow** is `Tensor`.
      ```py
      # to find the type of an object
      type(rolls)
      >>> numpy.ndarray

      # to see all variables in the module
      dir(rolls)
      >>> [...,'__bool__', ..., '__delattr__', '__delitem__', '__dir__', ..., '__sizeof__', ..., 'max', 'mean', 'min', ..., 'sort', ..., 'sum', ..., 'tobytes', 'tofile', 'tolist', 'tostring', ...]

      rolls.mean()
      >>> 2.8

      rolls.tolist()
      >>> [3, 2, 5, 2, 4, 2, 2, 3, 2, 3]

      # to see combined doc for functions and values in the module
      help(rolls)
      help(rolls.ravel)
      ```
- Operator Overloading
  - Index
    ```py
    xlist = [[1,2,3],[2,4,6]]
    xlist[1,-1]
    >>> TypeError: list indices must be integers or slices, not tuple
    xarray = numpy.asarray(xlist)
    xarray[1,-1]
    >>> 6
    ```
  - Add
    ```py
    [3, 4, 1, 2, 2, 1] + 10
    >>> TypeError: can only concatenate list (not "int") to list
    rolls + 10
    >>> array([13, 12, 15, 12, 14, 12, 12, 13, 12, 13])
    ```
  - Add in `tensorflow`
    ```py
    import tensorflow as tf
    # Create two constants, each with value 1
    a = tf.constant(1)
    b = tf.constant(1)
    # Add them together to get...
    a + b
    >>> <tf.Tensor 'add:0' shape=() dtype=int32>
    ```
  - When Python programmers want to define how operators behave on their types, they do so by implementing **Dunder/Special Methods**, methods with special names beginning and ending with 2 underscores such as `__add__` or `__contains__`.
  - For more info: https://is.gd/3zuhhL

## **Intro to Machine Learning**

Learn the core ideas in machine learning, and build your first models.

### [How Models Work](https://www.kaggle.com/dansbecker/how-models-work)

- Introduction
  > You ask your cousin how he's predicted real estate values in the past. and he says it is just intuition. But more questioning reveals that he's identified price patterns from houses he has seen in the past, and he uses those patterns to make predictions for new houses he is considering. Machine learning works the same way.
  - **Fitting** or **Training**: capturing patterns from data
  - **Training Data**: the data used to fit the model
  - **Predicting**: getting results from applying model to new data
- Decision Tree

### [Basic Data Exploration](https://www.kaggle.com/dansbecker/basic-data-exploration)

- Using Pandas to Get Familiar with the Data
  - **DataFrame**: The most important part of the Pandas library, similar to a sheet in Excel, or a table in a SQL database
    ```python
    # save filepath to variable for easier access
    melbourne_file_path = '../input/melbourne-housing-snapshot/melb_data.csv'
    # read the data and store data in DataFrame titled melbourne_data
    melbourne_data = pd.read_csv(melbourne_file_path)
    # print a summary of the data in Melbourne data
    melbourne_data.describe()
    ```
    |       |  Price  | Rooms | Bedroom2 | Bathroom | Landsize | BuildingArea | YearBuilt | Lattitude | Longtitude |  ...  |
    | :---: | :-----: | :---: | :------: | :------: | :------: | :----------: | :-------: | :-------: | :--------: | :---: |
    | count |  13580  | 13580 |  13580   |  13580   |  13580   |     7130     |   8205    |   13580   |   13580    |  ...  |
    | mean  | 1075684 | 2.93  |   2.91   |   1.53   |  558.41  |    151.96    |  1964.68  |  -37.80   |   144.99   |  ...  |
    |  std  | 639310  | 0.95  |   0.96   |   0.69   | 3990.66  |    541.01    |   37.27   |   0.07    |    0.10    |  ...  |
    |  min  |  85000  |   1   |    0     |    0     |    0     |      0       |   1196    |  -38.18   |   144.43   |  ...  |
    |  25%  | 650000  |   2   |    2     |    1     |   177    |      93      |   1940    |  -37.85   |   144.92   |  ...  |
    |  50%  | 903000  |   3   |    3     |    1     |   440    |     126      |   1970    |  -37.80   |   145.00   |  ...  |
    |  75%  | 1330000 |   3   |    3     |    2     |   651    |     174      |   1999    |  -37.75   |   145.05   |  ...  |
    |  max  | 9000000 |  10   |    20    |    8     |  433014  |    44515     |   2018    |  -37.40   |   145.52   |  ...  |
  - Interpreting Data Description
    - `count`: shows how many rows have non-missing values.
    - `mean`: the average.
    - `std`: the standard deviation, measures how numerically spread out the values are.
    - `min`, `25%` (25th percentile), `50%` (50th percentiles), `75%` (75th percentiles) and `max`

### [Your First Machine Learning Model](https://www.kaggle.com/dansbecker/your-first-machine-learning-model)

- Selecting Data for Modeling
  - The dataset has too many variables to wrap your head around. We'll start by picking a few variables using our intuition. Later, we use statistical techniques to automatically prioritize variables.
    ```python
    # look at the list of all columns in the dataset
    melbourne_data.columns
    # filter rows with missing values
    dropna_melbourne_data = melbourne_data.dropna(axis=0)
    ```
  - Selecting The **Prediction Target** (`y`)
    ```python
    y = dropna_melbourne_data['Price']
    ```
  - Choosing **Features** (input columns, `X`)
    ```python
    feature_list = ['Rooms', 'Bathroom', 'Landsize', 'BuildingArea', 'YearBuilt', 'Lattitude', 'Longtitude']
    X = dropna_melbourne_data[feature_list]
    # quick look at the data we'll be using to predict house prices
    X.describe()
    X.head()
    ```
- Building the Model
  - Steps
    - **Define**: What type of model will it be? A decision tree? Some other type of model?
    - **Fit**: Capture patterns from provided data. This is the heart of modeling.
    - **Predict**: Just what it sounds like.
    - **Evaluate**: Determine how accurate the model's predictions are.
  - scikit-learn
    ```python
    from sklearn.tree import DecisionTreeRegressor
    # define model, `random_state` ensures you get the same results in each run
    melbourne_model = DecisionTreeRegressor(random_state=1)
    # fit model
    melbourne_model.fit(X, y)
    # make predictions
    predictions = melbourne_model.predict(X)
    ```

### [Model Validation](https://www.kaggle.com/dansbecker/model-validation)

- Summarizing the Model Quality into Metrics
  - There are many metrics for summarizing the model quality.
  - **Predictive Accuracy**: Will the model's predictions be close to what actually happens?
    - **Mean Absolute Error** (MAE)
      ```python
      from sklearn.metrics import mean_absolute_error
      mean_absolute_error(y, predictions)
      >>> 434.715
      ```
- **Big Mistake**: Measuring scores with the training data or the problem with **"In-Sample" scores**!
- **Validation Data**
  - **Making Predictions on New Data**
  - The most straightforward way to do that is to exclude some data from the model-building process, and then use those to test the model's accuracy.
    ```python
    from sklearn.model_selection import train_test_split
    # split data into training and validation data, for both features and target
    train_X, val_X, train_y, val_y = train_test_split(X, y, random_state=1)
    # define model
    melbourne_model = DecisionTreeRegressor(random_state=1)
    # fit model
    melbourne_model.fit(train_X, train_y)
    # get predicted prices on validation data
    val_predictions = melbourne_model.predict(val_X)
    mean_absolute_error(val_y, val_predictions)
    >>> 259556.721
    ```
    > The MAE for the in-sample data was about 500 dollars. For out-of-sample data, it's more than 250,000 dollars. As a point of reference, the average home value in the validation data is 1.1 million dollars. So the error in new data is about a quarter of the average home value.
- There are many ways to improve a model, such as
  - Find **better features**, the iterating process of building models with different features and comparing them to each other
  - Find **better model types**
  - Find better **data pre-processing methods**. For example look at the different ways of using `dropna()`
    ```python
    # raw data
    melbourne_data.shape
    >>> (13580, 21)
    # rows without price
    melbourne_data['Price'].dropna(axis=0).shape
    >>> (13580,)
    # rows without the features we want
    melbourne_data[feature_list].dropna(axis=0).shape
    >>> (6858, 7)
    # rows with missing data
    melbourne_data.dropna(axis=0).shape
    >>> (6196, 21)
    ```

### [Underfitting and Overfitting](https://www.kaggle.com/dansbecker/underfitting-and-overfitting)

### [Random Forests](https://www.kaggle.com/dansbecker/random-forests)

### [Exercise: Machine Learning Competitions](https://www.kaggle.com/kernels/fork/1259198)

## **Intermediate Machine Learning**

Learn to handle missing values, non-numeric values, data leakage and more. Your models will be more accurate and useful.

## **Data Visualization**

Make great data visualizations. A great way to see the power of coding!

## **Pandas**

Solve short hands-on challenges to perfect your data manipulation skills.

## **Feature Engineering**

Discover the most effective way to improve your models.

## **Deep Learning**

Use TensorFlow to take machine learning to the next level. Your new skills will amaze you.

## **Intro to SQL**

Learn SQL for working with databases, using Google BigQuery to scale to massive datasets.

## **Advanced SQL**

Take your SQL skills to the next level.

## **Geopatial Analysis**

Create interactive maps, and discover patterns in geospatial data.

## **Microchallenges**

Solve ultra-short challenges to build and test your skill.

## **Machine Learning Explainability**

Extract human-understandable insights from any machine learning model.

## **Natural Language Processing**

Distinguish yourself by learning to work with text data.
