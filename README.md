# <p align="center">AI for Finance - Stock Price Prediction</p> 

Stock market prediction is the act of trying to determine the future value of a company stock or other financial instrument traded on an exchange. In this project a quantitative analysis over 5 italian companies (“AMZT.MI”, “ENI.MI”, “AGL.MI”, “LDOF.MI”, “ENEI.MI”) is carried out using different type of predictive models. The goal is to show how different methods can give a prediction of the stock price percentual variation of the next quarter and assessing the quality of the generated predictions. To perform this analysis, input data have been retrieved from the Refintiv Eikon platform using the Eikon API for python. After that, the data has been cleaned and processed before undergoing the analysis using different tools such as: VAR model, OLS regressions, LSTM recurrent neural networks. Finally, the obtained prediction have been evaluated using metrics such as MSE and RMSE. The data choosen for this analisys are: company fundamentals, historical price and opinion of the main analysts.

This repository is a student project developed by Kevin Depedri for the "AI for Finance" course of the Master in Artificial Intelligent Systems at the University of Trento, a.y. 2021-2022.

The repository is composed of:
- A folder for each company under analysis, in this you can find:
  - Notebook file showing all the computed results
  - CSV file with all the input data retrieved from Refinitiv Eikon
- Report pdf
- Guide to build the needed virtual environment and to run the code (this readme)

When looking at the notebooks please take notice that:
  1. Plotted charts are interactive, for this reason they cannot be shown on GitHub, since it performs a static render of the notebooks and it doesn't include the embedded HTML/JavaScript that makes up these graphs.
  2. Results of the OLS analysis are quite long when visualized on GitHub since they are not shown in a fixed size window.
  
For the two reasons above it is advised to download the repository and to visualize the notebooks locally using your IDE.

****
# Building the virtual environment and running the code
To build the virtual environment follow the next few steps
  1. Clone the repository and get inside it
  ```shell
  git clone https://github.com/KevinDepedri/AI-for-Finance
  cd AI-for-Finance
  ```
  2. From terminal run the following commands to start building the environment
  - On windows
      ```shell
      python -m venv venv
      venv/Scripts/pip install -r requirements.txt
      ```
  - On UNIX 
      ```shell
      python3 -m venv venv
      venv/bin/pip install -r requirements.txt
      ```
  3. Import the venv into your IDE to parse the notebook file
  4. Update the Eikon-API key if you have a valid one (2nd cell of the notebook). Otherwise, comment cell number 2 and 5, then uncomment cell number 6, in this way the data will be loaded from the attached CSV file, instead of downloading them from Refinitiv. This option has been provided appositly for who does not have access to the Refinitiv Eikon platform. 
****
