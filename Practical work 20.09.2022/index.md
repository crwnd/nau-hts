20.09.2022
# Task 6
## Scheme
*[Link](https://lucid.app/lucidchart/e0d7c026-06e3-4c2e-86ae-5f8c22951854/edit?viewport_loc=347%2C846%2C822%2C411%2C0_0&invitationId=inv_73e6f087-f253-4e78-a087-031fe4db0e36#)*
![task 6 scheme](20.09.2022_Task_6.png)
## Code
Run *[here](http://ibcomp.fis.edu/pseudocode/pcode.html)*:
```
output "Enter first element of sequence:"
input a1
output "a1: ", a1
output "Enter progression difference"
input d
output "d: ", d

nIsCorrect = false
loop while nIsCorrect == false
    output "Enter last progression element number"
    input n
    output "n: ", n

    if n >= 1 then
        nIsCorrect = true
    else 
        output "n MUST BE HIGHER THAN 0!"
    end if
end loop

output "Calculating ..."

iter = 1
sum = 0

loop while iter <= n
    thisElement = a1+d*(iter - 1)
    output "Element ", iter ," is ", thisElement
    sum = sum + thisElement
    iter = iter + 1
end loop

output "Sum is ", sum
```

# Task 7
## Scheme
*[Link](https://lucid.app/lucidchart/e0d7c026-06e3-4c2e-86ae-5f8c22951854/edit?viewport_loc=-60%2C-146%2C2389%2C1195%2CYW1S-Ph1Hl4V&invitationId=inv_73e6f087-f253-4e78-a087-031fe4db0e36#)*
![task 7 scheme](20.09.2022_Task_7.png)
## Code
Run *[here](http://ibcomp.fis.edu/pseudocode/pcode.html)*:
```
nIsCorrect = false
loop while nIsCorrect == false
    output "Enter n"
    input n
    output "n: ", n

    if n >= 1 then
        nIsCorrect = true
    else 
        output "n MUST BE HIGHER THAN 0!"
    end if
end loop

output "Calculating ..."

iter = 1
sum = 0

loop while iter <= n
    thisFactorial = 1
    multiplier = 1
    loop while multiplier <= iter
        thisFactorial = thisFactorial * multiplier
        multiplier = multiplier + 1
    end loop
    sum = sum + thisFactorial
    iter = iter + 1
end loop

avgOfFactorials = sum / n

output "Avg is ", avgOfFactorials
```
# Task 8
## Code

As pseudocode don`t have sqrt function and ^ symbol, then we should do next:

Run *[here](http://ibcomp.fis.edu/pseudocode/pcode.html)*:
```
input a
input b
input c

if a!=0 then
    d=(b*b)-(4*a*c)
    if d>0 then
        dRoot = 1
        loop while dRoot*dRoot < d
            if dRoot*dRoot==d then
                output "found"
            else
                dRoot=dRoot+1
            end if
        end loop

        x1=(-b+dRoot)/(2*a)
        x2=(-b-dRoot)/(2*a)
        output "x1: ",x1
        output "x2: ",x2
    else
        if d==0 then
            x=b/(2*a)
            output "x: ",x
        else
            output "no roots"
        end if
    end if
else
    if b!=0 then
        x=-c/b
        output "x: ",x
    else
        if c!=0 then
            output "no roots"
        else
            output "any value"
        end if
    end if
end if
```

Or as required:

```
input a
input b
input c

if a!=0 then
    d=(b^2)-(4*a*c)
    if d>0 then
        x1=(-b+sqrt(d))/(2*a)
        x2=(-b-sqrt(d))/(2*a)
        output "x1: ",x1
        output "x2: ",x2
    else
        if d==0 then
            x=b/(2*a)
            output "x: ",x
        else
            output "no roots"
        end if
    end if
else
    if b!=0 then
        x=-c/b
        output "x: ",x
    else
        if c!=0 then
            output "no roots"
        else
            output "any value"
        end if
    end if
end if
```