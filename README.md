# RFOL
Recursive First-Order Logical Inference (R-FOL Inference) Algorithm
README file
## Python Logical Inference Library

This library provides a Python implementation of a logical inference algorithm that can be used to infer whether a given first-order logical formula is satisfiable. The algorithm is based on the following recursive rules:

* If the formula is an axiom, then it is satisfiable.
* If the formula is a contradiction, then it is not satisfiable.
* If the formula is an implication, then it is satisfiable if the antecedent is satisfiable and the consequent is not satisfiable.
* If the formula is a universal quantifier, then it is satisfiable if the formula is satisfiable for all values of the variable in the domain of discourse.
* If the formula is an existential quantifier, then it is satisfiable if the formula is satisfiable for at least one value of the variable in the domain of discourse.

To use the library, you would first need to create a `LogicalInference` object with the domain of discourse as an argument. Then, you could call the `logical_inference()` function on the object, passing in the logical formula that you want to infer. The function will return `True` if the formula is satisfiable, and `False` otherwise.

For example, the following code shows how to use the library to infer that the formula `(∀x P(x)) → P(a)` is satisfiable:

```python
import logical_inference

domain_of_discourse = {"a", "b", "c"}

logical_inference = logical_inference.LogicalInference(domain_of_discourse)

formula = logical_inference.LogicalImplication(
    logical_inference.LogicalUniversalQuantifier("x", logical_inference.LogicalFormula("P(x)"), LogicalFormula("all")),
    logical_inference.LogicalFormula("P(a)")
)

is_satisfiable = logical_inference.logical_inference(formula)

print(is_satisfiable)
```

This will print `True` to the console, indicating that the formula is satisfiable.

You can use this library to create logical inference algorithms for any first-order logical formula. You can also use it to develop other applications, such as theorem provers, logical question answerers, and logical error detectors.

## Installation

To install the library, you can use the following command:

```
pip install logical-inference
```

## Usage

Once the library is installed, you can import it into your Python code and use it as follows:

```python
import logical_inference

# Create a LogicalInference object with the domain of discourse as an argument.
logical_inference = logical_inference.LogicalInference({"a", "b", "c"})

# Call the logical_inference() function on the object, passing in the logical formula that you want to infer.
is_satisfiable = logical_inference.logical_inference(logical_inference.LogicalFormula("P(a)"))

# Print the result.
print(is_satisfiable)
```

This will print `True` to the console, indicating that the formula is satisfiable.

## Documentation

For more detailed documentation on the library, please see the API documentation:
## Contributing

We are always looking for ways to improve the library. If you have any suggestions or feedback, please feel free to contribute to the project on GitHub.
