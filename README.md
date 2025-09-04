python projects

This repo will contain all my python project in the summer coding class 

# Luhn Algorithm Credit Card Validator

This repository contains a Python implementation of the Luhn algorithm, used for validating credit card numbers and other identification numbers.

## Description

The Luhn algorithm, also known as the "modulus 10" algorithm, is a simple checksum formula used to validate a variety of identification numbers, such as credit card numbers, IMEI numbers, and Canadian Social Insurance Numbers. This script provides a function to verify if a given number is valid according to the Luhn algorithm.

## How it Works

The `verify_card_number` function takes a string representing the card number as input and performs the following steps:

1.  **Reverses the number:** The digits are processed from right to left.
2.  **Sums odd-positioned digits:** Starting from the rightmost digit (which is considered the first, or odd-positioned), it sums all digits at odd positions.
3.  **Doubles and sums even-positioned digits:** For digits at even positions (second from right, fourth from right, etc.), it doubles their value. If a doubled digit is greater than or equal to 10, its digits are summed (e.g., 16 becomes 1+6=7). These modified values are then summed.
4.  **Calculates the total sum:** The sum of odd-positioned digits and the sum of modified even-positioned digits are added together.
5.  **Checks for validity:** The total sum is checked if it is divisible by 10. If it is, the number is considered valid according to the Luhn algorithm.

The `main` function demonstrates how to use `verify_card_number` by taking a sample credit card number, cleaning it by removing hyphens and spaces, and then printing "VALID!" or "INVALID!" based on the verification result.

## Usage

1.  **Save the code:** Save the provided Python code as a `.py` file (e.g., `luhn_validator.py`).
2.  **Run from terminal:** Open a terminal or command prompt, navigate to the directory where you saved the file, and run the script:
    ```bash
    python luhn_validator.py