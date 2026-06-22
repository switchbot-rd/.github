# switchbot-rd 组织默认 issue / PR 模板

本仓存放**组织级默认**的 issue 与 PR 模板。

## 这是什么 / 谁会看到
issue 与 PR 两类模板**各自独立**判断：某个仓**就某一类**而言，自己没有该类模板就自动套用这里的默认、自己有就用自己的（仓内优先）。所以同一个仓可能 issue 用自己的、PR 仍套 org 默认——例如只建了 `.github/ISSUE_TEMPLATE/`、没建 `PULL_REQUEST_TEMPLATE.md` 的仓，开 PR 时仍会套用这里的 PR 模板。这些是**轻量引导**默认：只帮你把信息写全，不强制；空白 issue 仍可开。

## 怎么覆盖成你自己仓的
在你的仓里放对应文件即可顶掉默认，但**两种覆盖语义不同**：

- **issue 模板是「整文件夹」覆盖**：仓里一旦建了 `.github/ISSUE_TEMPLATE/`（哪怕只放一个文件），org 默认的 **全部** issue 模板（bug/feature/task）都不再出现——要把你想保留的模板**一并自带齐**。
- **PR 模板是「单文件」覆盖**：`.github/PULL_REQUEST_TEMPLATE.md` 只顶掉默认 PR 模板，与 issue 模板互不影响。

        你的仓/
        └── .github/
            ├── ISSUE_TEMPLATE/              # 一旦存在，org 默认 issue 模板整组失效，需自带齐
            │   ├── bug.md
            │   └── …（你要的其余模板）
            └── PULL_REQUEST_TEMPLATE.md     # 仅顶掉默认 PR 模板

## 标签 / type 含义
- **Issue type**（Bug / Feature / Task / Epic / Chore）：工作性质，新建 issue 时选；Bug/Feature/Task 模板已预设。
- **`area:*`**：归属团队 / 领域，按你仓所属自行打（取值见组织标签集）。
- **优先级 P0–P3**：P0 最紧急，按需打。

## 反馈 / 维护
模板有问题或想改？在本仓开个 issue，或联系组织维护者。
