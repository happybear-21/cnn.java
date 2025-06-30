# CNN from Scratch in Java

This project is a clean, educational implementation of a Convolutional Neural Network (CNN) built from scratch in Java—no external machine learning libraries required. It demonstrates the core principles of deep learning, including forward and backward propagation, and is designed to work with the MNIST dataset for handwritten digit recognition.

---

## Features

- **Pure Java Implementation:** No external ML dependencies.
- **Modular Design:** Separate classes for layers, network logic, data handling, and utilities.
- **Layer Types:** Includes Convolution, Max Pooling, and Fully Connected layers.
- **Manual Backpropagation:** All training logic is implemented from first principles.
- **MNIST Support:** Reads and processes MNIST CSV data files.
- **Extensible:** Easy to add new layer types or adapt to other datasets.

---

## Project Structure

```
app/
  └── src/
      └── main/
          └── java/
              └── cnn/
                  ├── data/         # Data loading and image representation
                  ├── layers/       # Layer implementations (Conv, Pool, FC, etc.)
                  ├── network/      # Network builder and main logic
                  ├── utils/        # Matrix operations and utilities
                  └── Main.java     # Entry point
      └── test/
          └── java/cnn/MainTest.java
```

---

## Getting Started

### Prerequisites

- Java 8 or higher
- Gradle (or use the included wrapper scripts)

### Setup

1. **Clone the repository:**
   ```sh
   git clone https://github.com/happybear-21/cnn.java
   cd cnn.java
   ```

2. **Download MNIST CSV Data:**
   - Place `mnist_train.csv` and `mnist_test.csv` in `app/src/main/resources/data/` (or update the path in `Main.java`).

3. **Build the project:**
   ```sh
   ./gradlew build
   ```

4. **Run the program:**
   ```sh
   ./gradlew run --console=plain
   ```

---

## Usage

- The main class (`Main.java`) loads the MNIST data, builds a simple CNN, tests its accuracy, trains for several epochs, and prints the accuracy after each epoch.
- You can modify the network architecture in `Main.java` using the `NetworkBuilder` class.

---

## Customization

- **Add Layers:** Edit `Main.java` and use `NetworkBuilder` to add/remove layers.
- **Change Hyperparameters:** Adjust learning rates, number of filters, epochs, etc.
- **Extend Functionality:** Implement new layer types by extending the `Layer` class.

---

## Contributing

Pull requests and suggestions are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## License

[MIT](LICENSE) (or your preferred license)
