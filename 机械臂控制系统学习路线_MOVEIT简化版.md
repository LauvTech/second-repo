# 暑期阶段安排与学习路线（UR 实机与数据同步版）

### 第一阶段：ROS1 基础与数据记录（时间安排：第 1 周）

**1. 学习目标：**

掌握 ROS1 基础开发环境，理解 ROS1 通信机制与常用工具，能够独立创建工作空间、功能包并完成基础节点通信；掌握 TF 坐标变换、rosbag 数据录制与回放，为后续 UR 机械臂实机控制、力传感器读取、机械臂与力传感器数据同步采集打基础。

**2. 理论内容：**

- ROS1 计算图结构。
- Node、Topic、Service、Action 的通信机制。
- TF 坐标变换原理。
- ROS 工作空间与功能包结构。
- URDF/SDF 机器人描述模型基础。
- ROS 时间戳、消息频率与多 topic 数据对齐的基本概念。
- rosbag 数据录制、回放与检查的基本流程。
- Git 基本概念，包括工作区、暂存区、本地仓库和远程仓库。
- Git 基本提交流程，包括 add、commit、push、pull。
- README.md 与 .gitignore 在项目管理中的作用。

**3. 技术内容：**

- Python 基础，掌握 conda 虚拟环境管理。
- catkin 工作空间创建、编译与管理。
- ROS 功能包创建与节点编写。
- roslaunch、rosparam、rosbag 等工具使用。
- RViz 可视化与调试。
- TF 坐标变换查看与可视化。
- 使用 rostopic 查看 topic 名称、消息类型、频率和时间戳。
- 使用 rosbag 完成多 topic 数据录制、回放与检查。
- 学习同时记录机械臂状态 topic 与力传感器 topic 的方法。
- 安装并配置 Git。
- 在 GitHub 创建远程仓库。
- 在本地初始化 Git 仓库。
- 将 ROS1 项目绑定到 GitHub 远程仓库。
- 编写适用于 ROS1 项目的 .gitignore 文件，避免提交 build、devel、log 等中间文件。
- 编写 README.md，说明项目简介、环境依赖、编译方法、运行方式和演示结果。
- 使用 Git 完成基础代码提交和远程推送。

**4. GitHub 基本提交流程：**
1. 在 GitHub 创建远程仓库。
2. 在本地项目目录初始化仓库：
   ```bash
   git init
   ```
3. 添加远程仓库地址：
   ```bash
   git remote add origin https://github.com/用户名/仓库名.git
   ```
4. 查看文件修改状态：
   ```bash
   git status
   ```
5. 添加需要提交的文件：
   ```bash
   git add .
   ```
6. 提交到本地仓库：
   ```bash
   git commit -m "add initial ros project"
   ```
7. 设置主分支名称：
   ```bash
   git branch -M main
   ```
8. 推送到 GitHub：
   ```bash
   git push -u origin main
   ```

后续更新代码时，重复以下流程：

```bash
git status
git add .
git commit -m "update ros data collection demo"
git push
```

**5. 阶段产出：**
- ROS1 环境配置说明文档。
- Topic、Service、Action 示例程序。
- TF 坐标变换可视化 Demo。
- rostopic 查看 topic、频率和时间戳的操作记录。
- rosbag 录制、回放与检查 Demo。
- 机械臂状态 topic 与力传感器 topic 同步录制样例。
- ROS1 基础学习笔记。
- GitHub 远程仓库链接。
- 适用于 ROS1 项目的 .gitignore 文件。
- README.md 项目说明文档。

---

### 第二阶段：UR 实机使用、示教器操作与机械臂基础配置（时间安排：第 2 周）

**1. 学习目标：**
掌握实际 UR 机械臂的基本使用方法，能够通过示教器完成机械臂上电、初始化、手动移动、自由拖动、程序运行与安全恢复；理解 UR 机械臂末端、工具、传感器与目标物之间的坐标关系，并完成 MoveIt! 基础配置和姿态目标测试。

**2. 理论内容：**
- UR 机械臂基本组成与安全操作流程。
- 示教器 Polyscope 基本操作逻辑。
- 自动模式、手动模式、保护停止、急停与恢复流程。
- TCP、Payload、Base、Tool 等 UR 常用概念。
- 连杆坐标系、末端坐标系、工具坐标系与基坐标系的关系。
- 正运动学基本概念。
- 数值逆运动学基本概念。
- 运动学求解器与基本姿态目标的概念。
- URDF/SDF 机器人描述模型基础。

**3. 参考书籍与资料：**
- 《机器人学导论》
- UR 机械臂用户手册或实验室 UR 操作规范。
- UR 示教器 Polyscope 基础操作资料。

**4. 技术内容：**
- 学习 UR 机械臂上电、初始化、断电和急停流程。
- 学习示教器中的手动移动、关节空间移动和 TCP 移动。
- 学习 freedrive / teach mode 的使用方式。
- 学习设置和检查 TCP、Payload、工具坐标系。
- 学习保护停止后的恢复流程和安全注意事项。
- 理解机械臂 URDF/SDF 模型结构。
- 在 RViz 中完成机械臂模型加载与显示。
- 使用 MoveIt! Setup Assistant 生成配置包。
- 配置 MoveIt! 运动学求解器。
- 测试机械臂基本姿态目标是否可求解。
- 在 RViz 中检查机械臂末端坐标系、工具坐标系和相关 TF 关系。

**5. 阶段产出：**
- UR 示教器基础操作记录。
- UR 上电、急停、保护停止与恢复流程说明。
- TCP、Payload、Tool 坐标系设置说明。
- freedrive / teach mode 操作记录。
- MoveIt! 配置包。
- RViz 机械臂模型展示截图或视频。
- 基本姿态目标求解测试结果。
- 运动学求解器配置说明。
- 机械臂末端、工具和传感器坐标关系说明。

---

### 第三阶段：UR 机械臂 ROS 控制与 MoveIt! 基础运动（时间安排：第 3—4 周）

**1. 学习目标：**
掌握 UR 机械臂在 ROS 下的基本连接、状态读取和运动控制方法；能够结合示教器与 ROS 完成实际机械臂的基础运动执行，并使用 rosbag 记录机械臂状态、TF 和末端位姿信息，为后续接触实验中的定位、接近、撤离和简单动作执行提供基础。

**2. 理论内容：**
- UR 机械臂示教器控制与 ROS 控制的区别。
- UR 机械臂 ROS 驱动的基本工作流程。
- MoveIt! 系统架构。
- MoveIt! 规划、执行与控制器接口的基本流程。
- 关节空间点到点规划原理。
- 笛卡尔空间位姿目标规划原理。
- 关节空间控制与笛卡尔空间控制的区别。
- 规划轨迹、控制器与实际执行之间的关系。
- Planning Scene 基础概念。
- 机械臂状态数据、控制命令和执行反馈之间的关系。

**3. 技术内容：**
- 连接 UR 机械臂与 ROS 工作站。
- 启动 UR 机械臂 ROS 驱动。
- 在 ROS 中读取 UR 机械臂 /joint_states。
- 在 ROS 中查看 UR 机械臂 TF。
- 在 RViz 中检查 UR 实机状态与模型显示是否一致。
- 基于第二阶段生成的 MoveIt! 配置包，完善基础规划参数与控制器配置。
- Motion Planning 模块使用。
- JointTrajectoryController 基础配置。
- Planning Scene 基础场景管理。
- 机械臂关节空间点到点控制。
- 机械臂笛卡尔空间点到点控制。
- 机械臂运动执行状态检查。
- 使用示教器配合 ROS 进行安全监控和模式切换。
- 使用 RViz 观察规划路径与执行结果。
- 使用 rosbag 记录运动过程中的 /joint_states、TF 和末端位姿信息。

**4. 实现步骤：**
1. 通过示教器完成 UR 机械臂上电、初始化和安全检查。
2. 启动 UR 机械臂 ROS 驱动，确认 ROS 工作站与机械臂通信正常。
3. 使用 rostopic 查看 /joint_states、TF 和控制相关 topic。
4. 在 RViz 中检查机械臂模型、末端坐标系和工具坐标系。
5. 调用 MoveIt! 实现关节角度控制，完成关节空间点到点运动。
6. 调用 MoveIt! 实现笛卡尔空间位姿目标规划，完成末端从一个位姿到另一个位姿的点到点运动。
7. 执行轨迹并记录机械臂关节状态、末端位姿和 TF 信息。
8. 对 rosbag 数据进行回放，检查机械臂状态记录是否完整。

**5. 阶段产出：**

- UR 机械臂 ROS 驱动启动流程说明。
- 示教器与 ROS 配合使用流程说明。
- /joint_states、TF 和末端位姿读取记录。
- 关节空间点到点控制 Demo。
- 笛卡尔空间点到点控制 Demo。
- MoveIt! 点到点规划与执行代码。
- 机械臂基础运动执行视频。
- rosbag 记录的 UR 实机运动数据。
- MoveIt! 点到点运动 README 文档。

---

### 第四阶段：力传感器读取、UR 力控与机械臂-力数据同步（时间安排：第 5-6 周）

**1. 学习目标：**

理解阻抗控制与导纳控制的基本原理，掌握六轴力传感器在机械臂接触实验中的应用方式；能够读取力/力矩数据，了解 URCap 力控插件使用流程，完成 UR 机械臂状态数据与力传感器数据的同步记录和回放检查，并设计简单接触任务中的柔顺控制实验。

**2. 理论内容：**

- 阻抗控制基本原理。
- 导纳控制基本原理。
- 阻抗控制与导纳控制的区别。
- 阻抗控制与导纳控制的适用场景。
- 力传感器在柔顺控制中的应用。
- 接触阈值、预载控制与接触保护的基本概念。
- 接触、冲击、脱开和滑移等接触事件的力信号特征。
- 力/力矩数据与机械臂关节状态、末端位姿之间的对应关系。
- ROS 时间戳、采样频率、数据延迟与同步误差的基本概念。
- rosbag 中多 topic 同步录制与回放检查方法。

**3. 技术内容：**

- 学习六轴力传感器的数据读取方式。
- 了解宇立六轴力传感器 M4313S2A2E 的使用方法。
- 学习 URCap 力控插件使用流程。
- 读取并记录力/力矩数据。
- 使用 rostopic 查看力传感器 topic 的消息类型、频率和时间戳。
- 同时记录 /joint_states、TF、末端位姿和力/力矩数据。
- 检查机械臂状态数据与力传感器数据的时间戳对应关系。
- 对 rosbag 数据进行回放，检查数据是否丢帧、频率是否稳定、时间戳是否连续。
- 设计简单接触任务中的柔顺控制实验。
- 设计简单力控 Demo 或实验方案。
- 观察接触过程中 F/T 阈值、Fz 峰值、切向力变化和扭矩变化。
- 记录不同接触动作下的机械臂状态、末端位姿和力/力矩变化。

**4. 参考资料：**

- [CSDN：机器人的阻抗控制器和导纳控制器](https://blog.csdn.net/modest_laowang/article/details/148100563)
- [B站：UR Caps SRI 宇立仪器力控插件应用演示视频](https://www.bilibili.com/video/BV1CvRQBQEgz/?spm_id_from=333.1387.upload.video_card.click)
- UR 力控相关用户手册或实验室 URCap 使用说明。
- 宇立六轴力传感器 M4313S2A2E 使用说明。

**5. 阶段产出：**

- 阻抗控制与导纳控制对比笔记。
- 六轴力传感器使用过程记录。
- 力传感器 topic 读取记录。
- URCap 力控插件使用过程记录。
- UR 机械臂状态与力传感器数据同步录制 rosbag 样例。
- 机械臂-力传感器数据同步检查说明。
- 简单接触任务柔顺控制实验方案。
- 简单力控 Demo 或实验方案。
- 接触实验力/力矩数据记录样例。

---

### 第五阶段：具身智能与视觉-触觉方法调研（时间安排：第 7 周）

**1. 学习目标：**

了解具身智能领域与本项目相关的代表性方法，掌握模仿学习数据采集、触觉信息使用和视觉-触觉融合的基本思想，分析其与 UR 机械臂接触实验数据采集、机械臂状态读取和力传感器同步记录之间的关系。

**2. 理论内容：**

- 模仿学习中的数据采集方法。
- demonstration data 的基本组成。
- 模仿学习中触觉信息的使用方式。
- 视觉-触觉融合特征提取方法。
- Diffusion Policy 基本思想。
- ACT（Action Chunking with Transformers）基本思想。
- 慢-快视觉触觉策略学习方法。
- 接触事件、接触阶段、滑移趋势、风险标签与模型输入输出之间的关系。
- UR 机械臂状态、末端位姿、力传感器数据与模仿学习观测量之间的关系。

**3. 技术内容：**

- 阅读 Diffusion Policy、ACT、RDP 和视觉-触觉融合相关论文的核心思想。
- 梳理各方法的输入、输出、网络结构与训练目标。
- 总结机械臂模仿学习数据采集方法。
- 总结触觉信息在模仿学习中的使用方式。
- 总结视觉-触觉融合特征提取方法。
- 分析接触事件、阶段切换、滑移风险和 TTF 标签如何作为模型监督信号。
- 整理 C1/C2 采集任务与模型输入输出之间的对应关系。
- 整理 UR 机械臂状态数据与力传感器数据在模仿学习数据集中的字段形式。

**4. 参考文献：**

- **Diffusion Policy 原论文**  
  Chi C, Xu Z, Feng S, et al. Diffusion Policy: Visuomotor Policy Learning via Action Diffusion[J]. The International Journal of Robotics Research, 2025, 44(10-11): 1684-1704.

- **ACT 原论文**  
  Zhao T Z, Kumar V, Levine S, et al. Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware[J]. arXiv preprint arXiv:2304.13705, 2023.

- **RDP 反应式扩散策略：慢-快视觉触觉策略学习**  
  Xue H, Ren J, Chen W, et al. Reactive Diffusion Policy: Slow-Fast Visual-Tactile Policy Learning for Contact-Rich Manipulation[J]. arXiv preprint arXiv:2503.02881, 2025.

- **视觉触觉融合特征提取 + Diffusion Policy 动作生成**  
  Zhu X, Huang B, Li Y. Touch in the Wild: Learning Fine-Grained Manipulation with a Portable Visuo-Tactile Gripper[J]. Advances in Neural Information Processing Systems, 2026, 38: 153783-153812.

**5. 阶段产出：**

- 模仿学习数据采集方法总结。
- 触觉信息使用方式总结。
- 视觉-触觉融合方法总结。
- Diffusion Policy / ACT / RDP 输入、输出与训练目标对比表。
- C1/C2 标签与模型输入输出对应表。
- UR 机械臂状态与力传感器数据字段整理表。

---

### 第六阶段：综合整理与总结汇报（时间安排：第 8 周）

**1. 学习目标：**

完成学习成果整理、代码归档、演示视频和总结汇报，形成面向 UR 机械臂实机使用、ROS 控制、示教器操作、机械臂-力传感器同步采集、接触实验与视觉-触觉模仿学习数据采集的阶段性成果。

**2. 理论内容：**

- UR 机械臂控制系统整体架构。
- 示教器控制、ROS 控制与 MoveIt! 控制之间的关系。
- 传统控制方法与学习策略的关系。
- 真实接触任务数据采集流程。
- 机械臂状态数据、力传感器数据与后续触觉 encoder 预训练、模仿学习之间的关系。

**3. 技术内容：**

- 整理代码仓库。
- 完善 README 与运行脚本。
- 统一代码运行流程。
- 整理 ROS、UR 实机、MoveIt、力控和接触实验相关 Demo。
- 整理 rosbag 数据样例。
- 整理 UR 机械臂状态与力传感器数据同步记录样例。
- 制作 UR 机械臂示教器操作与 ROS 控制演示视频。
- 制作机械臂控制与接触实验演示视频。
- 制作最终报告汇报 PPT。

**4. 阶段产出：**

- 完整代码仓库。
- ROS 数据记录 Demo。
- UR 示教器基础操作说明。
- UR ROS 控制 Demo。
- MoveIt 基础控制 Demo。
- 力控 / 接触实验 Demo。
- 机械臂状态与力传感器同步采集 rosbag 样例。
- UR 机械臂控制与接触实验演示视频。
- 最终汇报 PPT。