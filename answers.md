# Answers — first 6502 lab

Please open this file and write your answers below each question.

1. What happened when you changed `lda #10` to `lda #25` and ran the program?

   Answer: The program rturned 25 as its exit status. It loaded 25 into the accumulator (A) and saved a copy in i. Loading 0 into A left the copy in i untouched, so lda i loaded 25 back into A just before the program exited.

2. What is the difference between `lda #10` and `lda i`?

   Answer: In lda #10, the # tells the CPU to load the number 10 directly into A. With lda i, the CPU reads the value stored at the memory location labeled i and loads that value into A.

3. What was the result of `(i + j) * 2 - k` with `i = 10`, `j = 7`, `k = 4`? Which instruction did you use to multiply by two?

   Answer: I got 30 from (10 + 7) * 2 - 4. I used asl to shift the sum one bit to the left, doubling it from 17 to 34 before subtracting 4.

4. Change `i = 20`, `j = 3`, `k = 5`. What did you expect, and what did the simulator return?

   Answer:

5. In your own words, what is the difference between a CPU register and a byte reserved in memory with `.res 1`?

   Answer: A register is a small storage location inside the CPU. For example, I used A to hold the value I was working with. .res 1 sets aside one byte at an address in memory. In this lab, I used that byte to keep a copy of my value so I could load it again after changing A.
