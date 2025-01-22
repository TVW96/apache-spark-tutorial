Exploring Apache Spark 
======================
[Installation](#installation)

[Pyspark Session](#pyspark-session)

# Installation
**How to install and run apache spark using homebrew in Mac OS**:
### 1. Install Java
Apache Spark requires Java, make sure that you have java installed with its latest verision.

``brew install openjdk``
### 2. Install Apache Spark
`brew install apache-spark`
### 3. Set Environment Variables
Add environment variables in either ~/.zshrc or ~/.bash_profile specifying location of Apache Spark file and bin executables. 

`nano ~/.zshrc`

`export SPARK_HOME=<path-to-spark>
export PATH=$SPARK_HOME/bin:$PATH`

Replace <path-tospark> with the directory location of apache spark. Example: 
export SPARK_HOME='/usr/local/Cellar/apache-spark/3.5.4'

### 4. Run Apache Spark with PySpark Shell
   `pyspark`
   differs depending on set up of your local environment but my system requires that I run pyspark as root user. Running as user account or admin user displays no output (corrupt symlink to bin/pyspark executable).
   
# Pyspark Session
After install apache spark and needed environment variables I can now open and interact with my pyspark shell.
<img width="1266" alt="Screenshot 2025-01-21 at 10 24 11 PM" src="https://github.com/user-attachments/assets/15ad357b-614c-464b-ac21-60e8a07c91ba" />

#### Creating a Spark Session
<img width="1273" alt="Screenshot 2025-01-21 at 10 26 05 PM" src="https://github.com/user-attachments/assets/f7aca530-64b1-470b-b332-6dcc3cc3bc2e" />

#### Create a Spark DataFrame
<img width="1273" alt="Screenshot 2025-01-21 at 10 27 27 PM" src="https://github.com/user-attachments/assets/d7313841-cb81-4807-b60f-cbb09b1103c3" />

#### Add a column to the Spark DataFrame
<img width="1260" alt="Screenshot 2025-01-21 at 10 28 29 PM" src="https://github.com/user-attachments/assets/53435d57-740f-4728-ae01-610497c6acf6" />
Notice original DataFrame is unchanged:
<img width="1257" alt="Screenshot 2025-01-21 at 10 30 15 PM" src="https://github.com/user-attachments/assets/f4f873a4-5777-41b1-8639-64e980f233c1" />

#### Filter Spark DataFrame
<img width="1264" alt="Screenshot 2025-01-21 at 10 30 38 PM" src="https://github.com/user-attachments/assets/5b2d83fc-b018-4c79-aa73-025729a6cdca" />

#### Group by aggregation on Spark DataFrame
<img width="1265" alt="Screenshot 2025-01-21 at 10 31 12 PM" src="https://github.com/user-attachments/assets/bea941d1-8a2d-4990-88a6-2f834c437cc0" />
computing average age of lifecycle:
<img width="722" alt="Screenshot 2025-01-21 at 10 31 43 PM" src="https://github.com/user-attachments/assets/4ce4e4f0-1e88-478c-82f8-7371bb0fc23b" />

#### Query DataFrame with SQL
<img width="1264" alt="Screenshot 2025-01-21 at 10 32 48 PM" src="https://github.com/user-attachments/assets/97d8e888-4621-4e02-901f-d182ab5e8125" />
compute the average age by life_stage with SQL: 
<img width="1266" alt="Screenshot 2025-01-21 at 10 33 36 PM" src="https://github.com/user-attachments/assets/4335a4b9-90dc-40c5-8bdd-54f059bd567f" />




