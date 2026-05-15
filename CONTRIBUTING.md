# 贡献指南

感谢您对项目的兴趣！我们欢迎各种形式的贡献，包括但不限于：

- 报告错误
- 提出新功能建议
- 提交代码改进
- 改进文档

在开始之前，请确保您已阅读并同意我们的[行为准则](CODE_OF_CONDUCT.md)。

## 目录

- [如何贡献](#如何贡献)
  - [报告错误](#报告错误)
  - [提出新功能建议](#提出新功能建议)
  - [提交代码改进](#提交代码改进)
- [开发环境设置](#开发环境设置)
- [分支策略](#分支策略)
- [提交信息规范](#提交信息规范)
- [代码风格](#代码风格)
- [测试要求](#测试要求)
- [Pull Request 流程](#pull-request-流程)
- [许可证](#许可证)
- [联系方式](#联系方式)

## 如何贡献

### 报告错误

如果您发现了错误，请：

1. 检查[现有问题](../../issues)以确保错误尚未被报告。
2. 如果错误未被报告，请使用[错误报告模板](.github/ISSUE_TEMPLATE/bug_report.md)创建新问题。
3. **请务必提供详细的日志信息**：
   - 进入设置 → 日志/调试 → 将日志等级调整为 `Debug`
   - 复现问题
   - 导出日志并粘贴到 issue 中
   - 将日志等级调回 `Info` 或 `Warning`

### 提出新功能建议

如果您有新功能建议，请：

1. 检查[现有问题](../../issues)以确保类似功能尚未被建议。
2. 如果功能未被建议，请使用[功能请求模板](.github/ISSUE_TEMPLATE/feature_request.md)创建新问题。
3. 请尽可能详细地描述使用场景和期望效果。

### 提交代码改进

如果您想提交代码改进，请：

1. Fork 此仓库。
2. 为您的功能创建一个新分支 (`git checkout -b feature/amazing-feature`)。
3. 提交您的更改 (`git commit -m 'feat: 添加一些惊人的功能'`)。
4. 推送到分支 (`git push origin feature/amazing-feature`)。
5. 创建一个[拉取请求](../../pull/new)。

## 开发环境设置

### 前置要求

- Git
- [您的开发工具]

### 克隆仓库

```bash
# 克隆您的 Fork
git clone https://github.com/your-username/.github.git
cd .github

# 添加上游仓库
git remote add upstream https://github.com/Silentely/.github.git

# 保持 Fork 同步
git fetch upstream
git merge upstream/main
```

### 分支命名规范

| 分支类型 | 命名格式 | 示例 |
|----------|----------|------|
| 功能开发 | `feature/<功能名称>` | `feature/add-login` |
| 问题修复 | `fix/<问题描述>` | `fix/fix-button-style` |
| 文档更新 | `docs/<文档内容>` | `docs/update-readme` |
| 重构 | `refactor/<重构内容>` | `refactor/optimize-query` |

## 提交信息规范

请遵循 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Type 类型

| 类型 | 说明 |
|------|------|
| `feat` | 新功能 |
| `fix` | Bug 修复 |
| `docs` | 文档更新 |
| `style` | 代码格式（不影响代码运行的变动） |
| `refactor` | 重构（既不是新增功能，也不是修改 bug 的代码变动） |
| `test` | 增加测试 |
| `chore` | 构建过程或辅助工具的变动 |

### 示例

```bash
git commit -m "feat: 添加用户登录功能"
git commit -m "fix: 修复按钮样式问题"
git commit -m "docs: 更新 README 安装说明"
```

## 代码风格

### 通用规则

- 使用 UTF-8 编码
- 使用一致的缩进（根据项目类型：2 或 4 个空格）
- 使用描述性的变量和函数名
- 避免过长的函数（建议不超过 50 行）
- 保持函数简洁和专注

### 注释规范

- 所有注释使用简体中文
- 避免无意义的注释（如 `// 增加变量`）
- 复杂逻辑必须添加注释解释设计意图
- 公共 API 必须添加文档注释

## 测试要求

### 测试原则

- 新功能必须包含相应的测试用例
- Bug 修复必须包含回归测试
- 测试应覆盖正常流程、边界条件和错误情况

### 运行测试

```bash
# 根据项目类型运行相应的测试命令
# 例如：
# npm test
# pytest
# go test ./...
```

## Pull Request 流程

### 提交前检查清单

- [ ] 代码遵循项目编码规范
- [ ] 已进行自我审查
- [ ] 已添加/更新相关测试用例
- [ ] 所有现有测试通过
- [ ] 已更新相关文档
- [ ] 提交信息符合规范

### PR 描述要求

1. **清晰描述变更内容**：做了什么、为什么做
2. **关联 Issue**：使用 `Fixes #123` 或 `Closes #123`
3. **提供测试信息**：测试步骤、截图/录屏、测试覆盖率
4. **说明性能影响**：如有，请提供对比数据
5. **提供回滚方案**：说明如果出现问题如何回滚

### Review 流程

1. 至少需要 1 个维护者批准
2. 所有 CI 检查必须通过
3. 根据反馈进行修改，直到获得批准
4. 合并后删除特性分支

## 许可证

通过贡献您的代码，您同意您的贡献将在与项目相同的许可证下授权。

## 联系方式

如果您有任何问题，请通过以下方式联系我们：

- 创建一个 [Issue](../../issues)
- 发送电子邮件至 [Abner@cosr.eu.org](mailto:Abner@cosr.eu.org)

再次感谢您的贡献！🎉