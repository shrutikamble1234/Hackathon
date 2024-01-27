# Hackathon
def calculate_pizza_count(individuals):
    # Pizza types and their slices
    large_slices = 8
    medium_slices = 6
    regular_slices = 4
    small_slices = 1

    # Calculate the minimum number of each pizza type
    large_pizzas = individuals // large_slices
    individuals %= large_slices

    medium_pizzas = individuals // medium_slices
    individuals %= medium_slices

    regular_pizzas = individuals // regular_slices
    individuals %= regular_slices

    small_pizzas = individuals // small_slices

    # Print the results
    print(f"We will have {large_pizzas} Large pizza")
    print(f"We will have {medium_pizzas} Medium pizza")
    print(f"We will have {regular_pizzas} Regular Pizza")
    print(f"We will have {small_pizzas} Small Pizza")

    # Calculate and print the total slices
    total_slices = (large_pizzas * large_slices) + (medium_pizzas * medium_slices) + \
                   (regular_pizzas * regular_slices) + (small_pizzas * small_slices)
    print(f"Total slices: {total_slices}")


# Example usage
calculate_pizza_count(100)
print("-----------------------------------------------------------")
calculate_pizza_count(19)
