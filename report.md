## Part 1 – Debugging Scenario
**Student**:
Hi, I think that is something wrong with junit test. When I use ` bash test.sh` to test my code with comile junit on it, It fails said cannot find Junit. But I am should that there is a file call lib and the junit package is in it. How can I fix it?

![image](junit.png)
![image](files.png)

**TA**:
Hi, Can I see your test.sh file? it should be something wrong in the file that cause this kind of error. You might write the path of the junit package wrong.

**Student**:
Sure! But the codes I wrote for the test.sh are copy from lab3 document which should be correct and my peer run the same code and they can run without such error. 

![image](test.shbefore.png)

**TA**:
I see. I think the code have no error. Do you use Windows system or IOS system? It might works different on different computer system. If you using Window system, Please try to make all the `:` to be `;`. For examples, `.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar` should be `.;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar` in Windows system.

**Student**:
Oh, yeah! I use windows system, and I try to make all the  `:` to `;` and it works!! But need help with my code now. I already swich the last elements to the front, why I cannot pass the test I wrote?

![image](worksbutfails.png)

**TA**:
Can I see your code and tests? I can help you to debug it.

**Student**:
Here it is! Thank you for helping me!

![image](wrongcode.png)
![image](code.png)

**TA**:
No problems. In your code, you only swich the last elements to the front but did not swich the back elements to the front, so the last half of the array will stay the same, which cause errors. In the test error message, you can see that in the position 1, expect value is 3, but the actual is 2, which means that the second value did not change at all and you need to fix it.

**Student**:
Oh! yeah, I got it! Thanks！

![image](testpass.png)

### set ups:
#### The file & directory structure needed
![image](files.png)
#### The contents of each file before fixing the bug
![image](wrongcode.png)
![image](code.png)
![image](test.shbefore.png)
#### The full command line (or lines) you ran to trigger the bug
For both bugs, I ask student to use `bash test.sh` to ran to trigger the bug.

#### A description of what to edit to fix the bug
- It might works different on different computer system. If you using Window system, Please try to make all the `:` to be `;`. For examples, `.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar` should be `.;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar` in Windows system.
- In your code, you only swich the last elements to the front but did not swich the back elements to the front, so the last half of the array will stay the same, which cause errors. In the test error message, you can see that in the position 1, expect value is 3, but the actual is 2, which means that the second value did not change at all and you need to fix it.

## Part 2 – Reflection
The most useful things is I know that we can create a .sh file and use bash to ran mutiple command at the same time. And we can use .sh file to write if statement and for loop using specific format. I think it is really useful and I never learn it before. 

Also I learn jdb, one of the hardesst thing I learn in cse 15l and I still have a hard time to use it. But it is really useful to find the infinity loops. when there is a lot of loops and function, it is hard to find the one that is infinity loop, But jdb could find it easily just set up different break points. 

The tool I like the most is vim. It can change the file directly without find and open it on tap. It is really helpful when we cannot find or access the file directly but remotely. 

In labs, I recieve a lot of help from tutors and classmates which really help me to understand the concepts and the method that we learn in class and also might apply to the skill demo. Thanks everyone!!
