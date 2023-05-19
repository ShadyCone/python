
#1st 
import pandas as pd

data = {'Last Name': ['Johnson', 'Smith', 'Williams', 'Brown', 'Jones', 'Garcia', 'Lee'],

                   'Name': ['John', 'Emily', 'Robert', 'Oliver', 'Mia', 'Luis', 'Sophia'],

                   'Year of Birth': [2000, 2001, 2000, 2002, 2001, 2000, 2002],

                   'Exam Score': [7, 8, 5, 9, 6, 7, 4]
        }
df = pd.DataFrame(data)
print(df)



satisfactory_grade = df[df['Exam Score'] >= 7]


print(satisfactory_grade[['Last Name']])





## 2nd Task 
import glob

txt_files = glob.glob("content/gdrive/MyDrive/*.txt")

words_counts = {}
for file in txt_files:
    with open(file) as f:
        file_content = f.read()
        words_list = file_content.split()
        for word in words_list:
            words_counts[word] = len(word)

print(words_counts)

with open('/content/gdrive/MyDrive/userdata.txt', 'r') as f:
  longest_word = max(f.read().split(), key=lambda i: len(i))
  print('The longest word is:'+ longest_word)
  
  
  
  #4th 
n = int(input('Enter a number:'))
for i in range(2**n):
    print(format(i, '0'+str(n)+'b'))
    
    
