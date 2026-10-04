Original reproduction:
ARI
BO
CY
C:\Users\evanf\OneDrive\Desktop\Javascript-appliccation-development\Mod 4\Debug exercise\script.js:3
  console.log(names[i].toUpperCase());
                       ^

TypeError: Cannot read properties of undefined (reading 'toUpperCase')
First wrong Value: Since the code asks for the names.length its running the loop looking for 3  names. The array starts as Ari=0 Bo=1 and CY=2 
The third iteration of the loop tries to access names[3], which is undefined, causing the error. 
Hypothesis: The loop condition uses <= instead of < causing the loop to access an invalid array index.
Fix: Change the loop condition from `i <= names.length` to `i < names.length` to avoid accessing an undefined index.
explanation: The original loop condition `i <= names.length` causes the loop to run one extra time, trying to access `names[3]`, which is undefined. By changing the condition to `i < names.length`, the loop correctly iterates only over the valid indices of the array, preventing the error.
