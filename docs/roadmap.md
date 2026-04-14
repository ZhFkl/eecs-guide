# 🗺️ EECS 选课与技能路线图

想要在 EECS 领域打怪升级，理清课程之间的**前置依赖关系（Prerequisites）**至关重要。

下方是为你梳理的全局技能树。

```mermaid
graph TD
classDef math fill:#e1f5fe,stroke:#0288d1,stroke-width:2px;
classDef cs fill:#e8f5e9,stroke:#388e3c,stroke-width:2px;
classDef ee fill:#fff3e0,stroke:#f57c00,stroke-width:2px;
classDef core fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px;

subgraph 大一阶段
M1[高等数学]:::math
M2[线性代数]:::math
P1[大学物理]:::math
C1[C/C++程序设计]:::cs
end

subgraph 大二阶段
DS[数据结构与算法]:::cs
C1-->DS
E1[电路原理]:::ee
P1-->E1
Control[自动控制原理]:::core
M1-->Control
M2-->Control
end

E1-->AnaE[模拟电子技术]:::ee
E1-->DigE[数字电子技术]:::ee
DigE-->CO[计算机组成原理]:::ee
DS-->CO

subgraph 大三及以后分支
AnaE-->Motor[电机控制与FOC]:::ee
CO-->Embed[嵌入式系统设计]:::ee
DigE-->FPGA[FPGA与数字系统]:::ee
CO-->OS[操作系统]:::cs
DS-->DB[数据库系统15-445]:::cs
DS-->Net[计算机网络]:::cs
Control-->Robot[机器人学与运动学]:::core
DS-->CV[计算机视觉与深度学习]:::core
CV-->3D[3D重建与空间感知]:::core
OS-->ROS[ROS与系统集成]:::core
end