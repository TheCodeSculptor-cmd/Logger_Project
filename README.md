# Logger_Project
A Python-based logging utility designed to efficiently generate, process, analyze, and visualize application logs.
# Table of Contents
* Features
* Installation
* Usage
* Generating Logs
* Processing Logs
* Analyzing Logs
* Visualizing Logs
* Contributing
* License

# Features
* Random Log Generation: Create logs with varying levels (INFO, DEBUG, ERROR, WARNING) and actions (Login, Logout, Data Request, etc.).
* Log Processing: Load and clean log data for analysis.
* Statistical Analysis: Perform basic analytics, including log counts, unique user identification, and activity metrics.
* Visualization: Graph log frequency trends over time using Matplotlib.

# Installation
* Clone the Repository:
` git clone https://github.com/TheCodeSculptor-cmd/Logger_Project.git 
cd Logger_Project`
* Set Up a Virtual Environment (Optional but recommended):
`python3 -m venv venv
source venv/bin/activate  # On Windows, use venv\Scripts\activate
`
* Install Dependencies:
`pip install -r requirements.txt`
Note: Ensure requirements.txt includes all necessary packages, such as pandas, numpy, matplotlib, beautifulsoup4, and requests.


# Usage

* Generating Logs
To generate random log entries and save them to a file:
`from log_generator import write_logs_to_file
write_logs_to_file('generated_logs.txt', num_entries=200)
`
This script creates a file named generated_logs.txt containing 200 random log entries. You can adjust the num_entries parameter as needed.

* Processing Logs
Load and process the generated logs:
`from log_processor import load_and_process_logs
df_logs = load_and_process_logs('generated_logs.txt')
`
This function reads the log file into a pandas DataFrame, cleans the data, and sets the timestamp as the index for further analysis.

* Analyzing Logs
Perform basic statistical analysis on the processed logs:
`from log_analyzer import analyze_data
stats = analyze_data(df_logs)
`
This will output statistics such as log level counts, action counts, total number of logs, unique users, and average logs per day.

* Visualizing Logs
Visualize log frequency trends over time:
`from log_visualizer import visualize_trends
visualize_trends(df_logs)`
A line graph will display the number of logs per day, helping identify activity patterns.


## Contributions are welcome! Please follow these steps:
## Fork the repository.
* Create a new branch (git checkout -b feature/YourFeature).
* Commit your changes (git commit -m 'Add YourFeature').
* Push to the branch (git push origin feature/YourFeature).
* Open a Pull Request.
For major changes, please open an issue first to discuss what you'd like to change.

Note: Replace placeholders like log_generator, log_processor, log_analyzer, and log_visualizer with the actual module names in your project. Ensure that the requirements.txt file is up-to-date with all dependencies.
