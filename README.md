# Ex-05: Develop a Population Growth Model
## NAME : AMMINENI MOKSHASREE
## REG NO : 2305001001
## Aim
To develop a simple mathematical model for population growth using Python and predict the population for future years.

## Objectives
1. To enter and display population data.
2. To plot the population growth over time.
3. To develop a linear population growth model.
4. To calculate actual and predicted population values.
5. To predict future population and visualize the growth trend.

## Program
```
import numpy as np
import matplotlib.pyplot as plt
year = np.array([2020, 2021, 2022, 2023, 2024])
population = np.array([10000, 10500, 11000, 11600, 12000])
print("Years:", year)
print("Population:", population)
t = np.array([0, 1, 2, 3, 4])
plt.figure(figsize=(10, 5))
plt.plot(year, population, marker="o", label="Actual")
plt.title("Population Growth")
plt.xlabel("Year")
plt.ylabel("Population")
plt.legend()
plt.grid(True)
plt.show()
b, a = np.polyfit(t, population, 1)

print("Starting Population =", round(a, 2))
print("Growth per Year =", round(b, 2))
predicted = a + b * t
print("\nYear  Actual  Predicted")
for i in range(len(year)):
    print(year[i], population[i], round(predicted[i], 2))
future_year = np.array([2025, 2026, 2027])
future_t = np.array([5, 6, 7])

future_population = a + b * future_t

print("\nFuture Population")
for i in range(len(future_year)):
    print(future_year[i], round(future_population[i], 2))
plt.figure(figsize=(10, 5))
plt.plot(year, population, marker="o", label="Actual")
plt.plot(year, predicted, marker="x", linestyle="--", label="Model")
plt.plot(future_year, future_population, marker="s",
         linestyle=":", label="Forecast")
plt.title("Population Growth Model")
plt.xlabel("Year")
plt.ylabel("Population")
plt.legend()
plt.grid(True)
plt.show()
```

## Output
<img width="442" height="57" alt="image" src="https://github.com/user-attachments/assets/bae0844f-a004-446b-beb6-1725ad46f846" />
<img width="868" height="470" alt="image" src="https://github.com/user-attachments/assets/cb54712c-a317-4c21-a787-b480c9d62c52" /> 
<img width="327" height="60" alt="image" src="https://github.com/user-attachments/assets/4d517ffd-5382-4cba-b215-4a83806366e7" /> <br>
<img width="257" height="150" alt="image" src="https://github.com/user-attachments/assets/feb42928-79eb-40be-a3bd-950e6c6d65af" /> <br>
<img width="187" height="107" alt="image" src="https://github.com/user-attachments/assets/d695feaf-6ff0-4369-bad8-c241dd0a5800" />
<img width="868" height="470" alt="image" src="https://github.com/user-attachments/assets/8fab4006-e590-4855-9902-7164ab3d04e1" />

## Result
A simple linear population growth model was successfully developed using Python. The model was used to calculate predicted population values, forecast the population for future years, and visualize the population growth trend.
