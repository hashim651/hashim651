def main():
    # how many numbers to input
    try:
        num_count = int(input("How many numbers do you want to input? "))
        if num_count <= 0:
            print("Please enter a positive integer.")
            return
    except ValueError:
        print("Invalid input. Please enter a valid integer.")
        return
    
    numbers = []

    # input the numbers
    for i in range(num_count):
        while True:
            try:
                num = float(input("Enter a number: "))
                numbers.append(num)
                break
            except ValueError:
                print("Invalid input. Please enter a valid number.")

    # arrange in ascending orderr
    numbers.sort()
    sorted_number_string = ",".join(map(str,numbers))
    # Display in ascending order
    print("Numbers in ascending order:")
    for number in numbers:
        print(number)
        print(sorted_number_string)

if __name__ == "__main__":
    main()
