# RISC-V IOMMU 移植与测试工作规划

## 1. 准备阶段

**目标**：熟悉项目背景，准备开发环境。

**任务**：

- 学习 RISC-V IOMMU 架构和 Linux 内核中 IOMMU 的实现。
- 获取并研究 [`tjeznach/linux`](https://github.com/tjeznach/linux) 的 `riscv_iommu_v7` 分支和 Zong Li 的补丁系列。
- Fork [`OpenEuler/OLK-6.6`](https://gitee.com/openeuler/kernel) 仓库，搭建开发环境。

**时间**：1-2 天(5.28-5.29)

---

## 2. 代码移植阶段

**目标**：将 RISC-V IOMMU 核心功能、`nested-iommu` 和 `riscv-iommu-hpm` 移植到 `OpenEuler/OLK-6.6`。

**任务**：

- 克隆 `tjeznach/linux` 的 `riscv_iommu_v7` 分支。
- 应用 Zong Li 的补丁系列。
- 将代码使用 `cherry-pick` 或手动方式移植到 `OpenEuler/OLK-6.6`。
- 解决代码冲突和兼容性问题。

**时间**：3-5 天(5.30-6.3)

---

## 3. 测试阶段

**目标**：验证移植后的功能在 `OpenEuler/OLK-6.6` 上正常运行。

**任务**：

- 使用 QEMU 搭建 RISC-V 模拟环境。
- 编译并启动移植后的内核。
- 测试核心 IOMMU 功能、`nested-iommu` 和 `riscv-iommu-hpm`。

**时间**：2-3 天(6.4-6.7)

---

## 4. 文档编写阶段

**目标**：整理移植过程、测试结果和架构分析。

**任务**：

- 编写移植报告，记录步骤、问题和解决方案。
- 对比 RISC-V IOMMU 与 x86/ARM IOMMU 的软硬件实现差异。
- 提出 RISC-V IOMMU 的优化建议。

**时间**：1-2 天(6.8)

---

## 5. 扩展任务

**目标**：深入分析架构差异并完善 RISC-V IOMMU 实现。

**任务**：

- 研究 x86（VT-d）、ARM（SMMU）和 RISC-V IOMMU 的硬件特性。
- 对比 Linux 内核中各架构的 IOMMU 驱动。
- 撰写详细分析报告并提出改进建议。

**时间**：3-5 天 (before 6.8 视完成情况)

