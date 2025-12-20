# 📊 No-Show Appointments – Data Analysis

This repository contains a **data analysis project** on the **No-Show Medical Appointments** dataset.  
The goal is to explore factors that influence whether patients **attend** or **miss** their scheduled medical appointments.

---

## Dataset Overview

The dataset includes **110,527 appointments** in Brazil, with information on:

- **Patient demographics:** age, gender  
- **Appointment details:** scheduled day, appointment day  
- **Health indicators:** hypertension, diabetes, alcoholism, disability  
- **Social indicator:** scholarship (Bolsa Família welfare program)  
- **Communication:** SMS reminder received  
- **Target variable:** `No-show`  
  - `No` → patient showed up  
  - `Yes` → patient did not show up  

Each row represents one scheduled medical appointment.

---

## Research Questions

1. Does **age** influence the likelihood of missing an appointment?  
2. Do patients with **hypertension, diabetes, or alcoholism** tend to miss appointments more often?  
3. Does **gender** influence the likelihood of missing an appointment?  

---

## Data Wrangling

### Cleaning Steps

- Removed unnecessary ID columns: `PatientId` and `AppointmentID`  
- Removed unrealistic ages: <0 or >100  
- Converted the dataset into an **analysis-ready format**  

### Feature Engineering

- **AgeGroup:** Children (0–14), Youth (15–24), Adults (25–64), Seniors (65+)  
- **Multiple_Condition:** 1 if patient has **two or more** conditions (hypertension, diabetes, alcoholism), otherwise 0  

---

## Exploratory Data Analysis

### Age and Attendance

- Children and seniors have **lower no-show rates**  
- Youth and adults have **higher proportions of missed appointments**  

### Chronic Conditions and Attendance

- Majority of patients have **no recorded conditions**  
- Patients with multiple conditions account for a small subset  
- Hypertension slightly more common among missed appointments  

### Gender and Attendance

- Females represent a higher proportion of missed appointments, reflecting dataset demographics  
- No strong evidence that gender alone predicts no-show behavior  

---

## Conclusions

- **Age** influences attendance: younger and middle-aged adults are more likely to miss appointments  
- **Chronic conditions** show limited association with no-show rates  
- **Gender** does not strongly predict missed appointments  

Attendance is influenced by multiple factors; no single variable fully explains no-show behavior.

---

## Limitations

- Descriptive analysis only; no statistical testing performed  
- Missing contextual variables such as distance, insurance type, or prior attendance patterns  
- Small sample sizes in some subgroups limit reliability  

---

## Future Work

- Investigate the effect of **SMS reminders** on attendance  
- Explore interactions between **age, gender, and chronic conditions**  
- Collect additional variables to better model no-show behavior  
- Apply **predictive modeling** to identify high-risk patients  

---

## Repository Structure

