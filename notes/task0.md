# 现代 Agent = LLM + 上下文 + 工具
Agent = LLM + 上下文 + 工具
- **LLM = 大脑**：思考、规划、决策
- **上下文 = 眼睛**：决定 Agent 当前能看到什么
- **工具 = 手脚**：决定 Agent 能对外界做什么
Agent 外面还有一个 **Environment（环境）**，例如网页、文件系统、数据库、用户、操作系统等。Agent 通过“观察”和“行动”不断与环境交互。

## 眼睛 +工具是模型与世界的接口
扩展上下文=扩展观察空间
扩展工具=扩展动作空间

## 工具是agent的手脚
有感知工具，执行工具，协作工具，事件触发工具，用户沟通工具等
他们可以直接帮用户做事

## LLM是agent的大脑
agent特别依赖模型的推理能力

## 上下文是agent的眼睛

实验1.1：
![[Pasted image 20260916221818.png]]

# ReAct循环
agent执行任务的核心模式是ReAct（Reasoning思考+Acting行动）
实际就是LLM+Tool+Loop
不断循环

实验1.2：
![[Pasted image 20260916222149.png]]
实验1.3：![[Pasted image 20260916222207.png]]


# Harness工程
可以理解为包围在LLM外面的agent工程系统
Agent=Model+Harness
Harness=Context+Tools+Constrain+Verify+Correct
1. Context让Agent知道现在发生了什么
2. Tools让Agent有能力做事情
3. Constrain限制Agent能做什么，不能做什么
4. Verify检查Agent做的对不对
5. Correct发现错误后自动修复

# 从提示工程到Loop工程
提示工程->上下文工程->Harness工程->Loop工程->graph工程

## 构建有效Agent的原则
1. 保持简单
2. 保持透明
3. 设计好工具接口

# 工作流和自主
工作流是程序员提前规定好的一条路线
自主是执行路线由模型自己决定
实际产品经常采用工作流+自主的混合模式
实验1.4：![[Pasted image 20260916224102.png]]