根据提供的 `git diff` 记录，以下是针对 `.github/workflows/main-maven-jar.yml` 和 `.github/workflows/main-remote-jar.yml` 文件的代码评审：

### .github/workflows/main-maven-jar.yml

**更改点：**
1. `push` 事件触发分支从 `master-close` 更改为 `master`。
2. `pull_request` 事件触发分支从 `master-close` 更改为 `master`。

**评审意见：**
- **理由**：将触发分支从 `master-close` 更改为 `master` 可能是为了简化流程或反映代码库中的实际分支结构。
- **正面**：如果 `master-close` 分支已经不再需要，则更改是合理的，并且可以避免混淆。
- **负面**：如果没有明确的理由更改分支，可能需要文档说明这一变更的动机。
- **建议**：确保更改后的分支结构与项目团队的实际工作流程一致。

### .github/workflows/main-remote-jar.yml

**更改点：**
1. `push` 事件触发分支从 `master` 更改为 `master-close`。
2. `pull_request` 事件触发分支从 `master` 更改为 `master-close`。

**评审意见：**
- **理由**：与 `main-maven-jar.yml` 类似，这里的分支更改可能是为了反映代码库中的实际分支结构。
- **正面**：如果 `master-close` 分支是主要的开发分支，则更改是合理的。
- **负面**：如果没有明确的理由更改分支，可能需要文档说明这一变更的动机。
- **建议**：确保更改后的分支结构与项目团队的实际工作流程一致。

### 通用建议：
- **文档化**：无论分支结构如何更改，都应该在项目的文档中记录下来，以便团队成员了解当前的流程和分支策略。
- **一致性**：确保所有相关的 `.github/workflows` 文件都反映了相同的分支结构，以避免混淆和错误。
- **测试**：在更改分支后，应该对工作流进行测试，确保它们按预期工作。