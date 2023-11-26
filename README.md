# password-strength-checke
print("----Welcome to password strength checker----")
import getpass
while(1):
 choice=input("Do you want to check your password strength:")
 strength=0
 lowercount,uppercount,digit_count,white_space_count,special_character_count=0,0,0,0,0
 digit='0123456789'
 if choice.lower()=='yes':
 password=getpass.getpass("Enter your password:")
 for char in password:
 if char.isupper():
 uppercount+=1
 elif char.islower():
 lowercount+=1
 elif char in digit:
 digit_count+=1
 elif char==' ':
 white_space_count+=1
 else:
 special_character_count+=1
 if uppercount>=1:
 strength+=1
 if lowercount>=1:
 strength+=1
 if digit_count>=1:
 strength+=1
 if white_space_count>=1:
 strength+=1
 if special_character_count>=1:
 strength+=1
 print("Your password has:")
 print(f'{uppercount} uppercaseletters')
 print(f'{lowercount} lowercaseletters')
 print(f'{digit_count} digits')
 print(f'{white_space_count} whitespaces')
 print(f'{special_character_count} special character count')
 if strength==1:
 print("Your password is bad...change it immediately")
 elif strength==2:
 print("Your password is weaker...consider a toughest password")
 elif strength==3:
 print("Your password is okay, but it can be improved.")
 elif strength==4:
 print("Your password is hard to guess. But you could make it even more secure.")
 elif strength==5:
 print("Now that\'s one hell of a strong password!!!' Hackers don\'t have a chance guessing
that password!")
 elif choice.lower()=='no':
 print('Exit')
 else:
 print("Invalid")
