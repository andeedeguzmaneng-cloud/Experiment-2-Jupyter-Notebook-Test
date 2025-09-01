# Experiment-2-Jupyter-Notebook-Test

This repository contains a Jupyter Notebook with two solved Python problems:

		1. NORMALIZATION PROBLEM
        2. DIVISIBLE BY 3 PROBLEM

each problem is explained with code, outputs, and syntax definitions. It also includes step-by-step instructions on how to get started with Jupyter Notebook in Anaconda and how to upload your completed work to GitHub.

_____________________________________

Getting Started with Jupyter Noteboook

        To begin creating your Python code using Jupyter Notebook:
        
                1. Open Anaconda Navigator on your computer.
                2. Look for Jupyter Notebook and open it.
                3. Once Jupyter Notebook launches in your browser, you can create a folder to keep all your Jupyter files organized.
                4. Open the folder where you want to save your work.
                5. Click the New button (on the top-right side).
                6. From the dropdown, select Python 3 (ipykernel).
                
        A new Jupyter Notebook will open — and now you can start writing and running your Python code!

_____________________________________

--- IMPORTING THE LIBRARY ---
Before starting with the problems, the NumPy library must be imported since both problems require it:

--- CODE ---

	import numpy as np    # Import NumPy library

This import statement should be placed at the very beginning of the notebook so it applies to all the code cells that follow.

Problem # 1. 

NORMALIZATION PROBLEM
                       - This program creates a random 5x5 matrix, then normalizes the data by subtracting the mean and dividing by the standard deviation. It shows how to use NumPy functions such as mean() and std().

---- CODE ---

		NORMALIZATION PROBLEM   # Markdown heading for the problem

	[]: X = np.random.rand(5, 5)                                 # Create a random 5x5 array
		print("Original X:\n", X)
  
  		X_normalized = (X - X.mean()) / X.std()                  # Normalize using (X - mean)/std
    	print("Normalized X:\n", X_normalized)

	[]: np.save("X_normalized.npy", X_normalized)                # Save the normalized array

--- EXECUTION / RUNNING THE CODE ---

To execute the code cell:

	1. Click inside the cell
	2. Then click the Run botton
	3. The output will appear dirctly below the cell

Note this are the outputs it may give:

         1. No Output: Nothing is displayed because the code only defines something it can be a function or variable but does not print it yet.
         2. Normal Output: This is when the program successfully prints a result. 
         3. Input Prompt: The program asks the user to type something before continuing.
         4. Error Message: A red message shown when the code has a mistake or when an undefined variable or function is used.
 

--- OUTPUT ---
	
 	The program prints the original random array and its normalized version, then saves the normalized array to X_normalized.npy.
 
--- DEFINITON OF SYNTAX USED ---

	1. import numpy as np → loads NumPy library.

	2. np.random.rand(5,5) → generates a 5x5 array of random values between 0 and 1.

	3. .mean() → computes the mean of all elements.

	4. .std() → computes the standard deviation of all elements.

	5. (X - X.mean()) / X.std() → formula for normalization.

	6. print() → displays text or results.

	7. np.save(filename, array) → saves an array to a .npy file.



_____________________________________


Problem # 2

DIVISIBLE BY 3 PROBLEM
                       - This program generates the squares of the first 100 integers arranged in a 10x10 array. It then selects all values divisible by 3 and saves them to a file.

---- CODE ---

		DIVISIBLE BY 3 PROBLEM   # Markdown heading for the problem

	[]: A = np.arange(1, 101) ** 2                         # Generate squares of 1–100
   		A = A.reshape(10, 10)                              # Reshape into 10x10 array
    	print("10x10 ndarray of squares:\n", A)

	[]: div_by_3 = A[A % 3 == 0]                           # Select elements divisible by 3
    	print("Elements divisible by 3:\n", div_by_3)

	[]: np.save("div_by_3.npy", div_by_3)                  # Save the result to file

--- EXECUTE / RUN THE CODE ---

Execute the code as you did previously.

--- OUTPUT ---

	The program prints the 10x10 matrix of squares and the list of values divisible by 3. It saves them to div_by_3.npy.

--- DEFINITON OF SYNTAX USED ---

	1. np.arange(1, 101) → creates an array of numbers 1 to 100.

	2. ** 2 → squares each element.

	3. .reshape(10, 10) → reshapes the array into 10 rows and 10 columns.

	4. A % 3 == 0 → finds elements divisible by 3 (modulo operation).

	5. A[A % 3 == 0] → extracts only those elements divisible by 3.

	6. print() → displays the arrays.

	7. np.save(filename, array) → saves results to a .npy file.

_____________________________________


Now that you’re done with all the problems, the next step is to upload your Jupyter Notebook file to GitHub so it can be saved, shared, and accessed easily.

--- PROCEDURE FOR UPLOADING TO GITHUB ---

        1. After finishing all problems in the Jupyter Notebook, click File → Download as → Notebook (.ipynb) to save the file on your computer.
        2. Open your web browser and go to GitHub.
        3. Sign in to your GitHub account.
        4. On the top-right, click the + (plus) button and choose New repository.
        5. Enter a Repository Name (for example: Experiment-1-Jupyter-Notebook-Test).
        6. Turn on "Add a README file" so the repository starts with a description.
        7. Click Create repository.
        8. Once inside the repository, click Add file → Upload files.
        9. Click Choose your files and select the Jupyter Notebook file (.ipynb) you downloaded.
        10. Scroll down and click Commit changes to upload it.

Now your Jupyter Notebook is saved and viewable in your GitHub repository. 







