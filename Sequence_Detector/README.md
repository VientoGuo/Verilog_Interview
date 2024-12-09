## 题目描述
有一位输入信号in，在无限长时间内连续输入一位信号。  
设计序列检测器，检测输入序列：10110。  
当检测到该序列时（检测到最后一位1时），立即将输出信号out置1一个时钟周期，其余时候out保持为0。  
该题目根据要求不同，解法也不同，且有多种实现方法。
### 1. 重叠（Overlapping）
即上一个序列可作为下一个序列的一部分。  
#### 举例：  
```
in:  010110110110  
out: 000001001001
```
#### 实现方法
* 状态机（Moore状态机 / Mealy状态机）
* 移位寄存器
### 2. 非重叠 (Non-overlapping）
即上一个序列不能作为下一个序列的一部分。  
#### 举例： 
```
in:  010110110110  
out: 000001000001
```
#### 实现方法
* 状态机（Moore状态机 / Mealy状态机）
* 移位寄存器