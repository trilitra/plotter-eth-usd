# Ethereum Price Plotter
This project loads Ethereum price data from a CSV file, processes it, and generates a visual price chart saved as an image.

## Features
- Reads ETH price data from a CSV file
- Processes price pairs
- Generates a plot using the `gonum/plot` library
- Saves the plot as a PNG image

## Project Structure
.
├── main.go
├── prices.csv
├── csv_process/
│   └── (CSV loading logic)
├── plotter/
│   └── (Plot generation logic)
└── ethereum_prices.png (generated output)

## Requirements
- Go 1.20+ (recommended)
- Gonum Plot library

Install dependencies:
go get gonum.org/v1/plot/...

## CSV Format
The program expects a CSV file (`prices.csv`) containing Ethereum price data. The exact structure depends on the `csv_process` package, but typically it should include:
Date,Price
2024-01-01,2300
2024-01-02,2350
...

## How to Run
1. Place your price data into `prices.csv`.
2. Run the program:
   go run main.go
3. After successful execution, the program will generate: `ethereum_prices.png`

## Output
The program creates a chart showing Ethereum price changes over time.

## Error Handling
The program will terminate if:
- The CSV file cannot be read
- The plot cannot be generated
- The output file cannot be saved
  Error messages will be displayed in the console.

## Packages Used
- `csv_process` – Handles CSV data loading
- `plotter` – Generates the price chart
- `gonum/plot` – Plotting library

## License
This project is open-source. You may modify and distribute it freely.
