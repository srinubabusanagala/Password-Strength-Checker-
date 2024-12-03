# Password-Strength-Checker-
Python code:
import re
def check_password_strength(password): strength_score = 0
# Check the length of the password if len(password) >= 8:
strength_score += 1

# Check for lowercase letters if re.search("[a-z]", password):
strength_score += 1
# Check for uppercase letterif re.search("[A-Z]", password): strength_score += 1

# Check for digits
if re.search("[0-9]", password): strength_score += 1

# Check for special characters
if re.search("[!@#$%^&*(),.?\":{}|<>]", password): strength_score += 1

# Determine strength based on the score if strength_score <= 2:
return "Weak"
elif strength_score == 3 or strength_score == 4: return "Moderate"
else:
return "Strong"

# Test the function
password = input("Enter a password to check its strength: ") print(f"Password strength: {check_password_strength(password)}")
Output:1
Enter a password to check its strength: P@ssw0rd!
 Password strength: Strong
