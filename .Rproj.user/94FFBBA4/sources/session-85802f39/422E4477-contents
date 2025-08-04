# ===================================================================
#               AI and Biotechnology/Bioinformatics        
# ===================================================================
# -------------------------------------------------------------------
#             AI and Omics Resrarch Internship (2025)
# -------------------------------------------------------------------
#               Module I: Getting Started with R (Class Ib)
# -------------------------------------------------------------------
# ==================================================================

# Topics:
# 1. Setting the working directory properly
# 2. Creating and organizing project folders
# 3. How R code works: functions, syntax, and execution
# 4. Variables and data types in R
# 6. Importing CSV files and working with categorical data
# 7. Saving scripts, outputs, and the R workspace
# -------------------------------------------------------------------------------------------------------
#### Tasks ####

# 1. Set Working Directory
# Create a new folder on your computer "AI_Omics_Internship_2025".

# 2. Create Project Folder

# In RStudio, create a new project named "Module_I" in your "AI_Omics_Internship_2025" folder.

# Inside the project directory, create the following subfolders using R code:
# raw_data, clean_data, scripts, results or Tasks, plots etc
# Create common subfolders for project organization
dir.create("raw_data")    
dir.create("clean_data")   
dir.create("scripts")   
dir.create("results")  
dir.create("plots")     


# ---------------------------------------------------------------------------
# 3. Download "patient_info.csv" dataset from GitHub repository

# load the dataset into your R environment
# Import Data from CSV

data <- read.csv("patient_info.csv")

# Inspect the structure of the dataset using appropriate R functions
# View data in spreadsheet format
View(data)

# Check structure of the dataset
str(data)

# Identify variables with incorrect or inconsistent data types.

# Convert variables to appropriate data types where needed

# Create a new variable for smoking status as a binary factor:
  
# 1 for "Yes", 0 for "No"

# Save the cleaned dataset in your clean_data folder with the name patient_info_clean.csv
# Save your R script in your script folder with name "class_Ib"
# Upload "class_Ib" R script into your GitHub repository

# Load dataset
data <- read.csv("raw_data/patient_info.csv")

# View the structure
str(data)
View(data)
# Summary statistics to catch anomalies
summary(data)

# Check unique values for each column
sapply(data, unique)

# Convert gender and smoker to factors
data$gender <- as.factor(data$gender)
data$diagnosis <- as.factor(data$diagnosis)

# Convert smoking status to binary: 1 = Yes, 0 = No
data$smoking_status <- ifelse(data$smoker == "Yes", 1, 0)

# Check data again
str(data)

library(ggplot2)

#  BMI by Smoking Status plot
ggplot(data, aes(x = as.factor(smoking_status), y = bmi)) +
  geom_boxplot(fill = "skyblue") +
  labs(x = "Smoking Status (0 = No, 1 = Yes)", y = "BMI") +
  ggtitle("BMI by Smoking Status")

# Save the plot
ggsave("plots/bmi_by_smoking_status.png", width = 6, height = 4)

# Save cleaned data
write.csv(data, "clean_data/patient_info_clean.csv", row.names = FALSE)

