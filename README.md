# Resume Skills（简历求职技能库）

一套专注于简历优化、岗位申请与职业发展的 AI 智能体技能合集。面向求职者、转行人群和希望借助 Claude Code / Cursor 等 AI 助手完成简历撰写、ATS 优化、面试准备与求职策略的专业人士。

## 什么是技能（Skills）？

技能是 Markdown 文件，为 AI 智能体提供完成特定任务所需的专业知识与工作流。把这些技能加到你的项目里后，AI 助手就能识别出你正在处理简历与求职相关的任务，并自动套用对应的方法论与最佳实践。

## 可用技能

| 技能（Skill） | 说明 |
|-------|-------------|
| [using-resume-skills](/skills/using-resume-skills) | ⭐ 技能路由入口——根据你的请求自动判断应使用哪个技能 |
| [resume-ats-optimizer](/skills/resume-ats-optimizer) | 针对简历筛选系统（ATS）优化简历，检查 ATS 兼容性，分析关键词匹配度 |
| [resume-bullet-writer](/skills/resume-bullet-writer) | 将平淡的经历条目改写成有数据、有亮点、聚焦成果的表述 |
| [resume-quantifier](/skills/resume-quantifier) | 为简历寻找可量化的机会，数字未知时帮你合理估算 |
| [job-description-analyzer](/skills/job-description-analyzer) | 分析岗位招聘信息，计算匹配度评分，识别差距，制定申请策略 |
| [resume-tailor](/skills/resume-tailor) | 在保持真实的前提下，将简历定制到具体岗位 |
| [cover-letter-generator](/skills/cover-letter-generator) | 根据简历 + 岗位描述生成个性化、有说服力的求职信 |
| [linkedin-profile-optimizer](/skills/linkedin-profile-optimizer) | 使简历与 LinkedIn 领英主页保持同步，优化搜索曝光度与吸引力 |
| [interview-prep-generator](/skills/interview-prep-generator) | 根据简历生成 STAR 故事、模拟面试题与答题要点 |
| [salary-negotiation-prep](/skills/salary-negotiation-prep) | 调研市场薪资水平，制定谈判策略，编写反向报价话术 |
| [tech-resume-optimizer](/skills/tech-resume-optimizer) | 针对软件工程、产品经理及技术类岗位优化简历 |
| [executive-resume-writer](/skills/executive-resume-writer) | 为 C 级高管与 VP 级别撰写突出战略领导力的简历 |
| [career-changer-translator](/skills/career-changer-translator) | 将技能从原行业迁移到目标行业，识别可迁移能力 |
| [resume-formatter](/skills/resume-formatter) | 确保 ATS 友好的排版格式，打造干净易扫读的版面 |
| [resume-section-builder](/skills/resume-section-builder) | 针对不同资历与岗位，创建有针对性的简历板块 |
| [portfolio-case-study-writer](/skills/portfolio-case-study-writer) | 将简历上的条目扩写成详细的作品集案例 |
| [academic-cv-builder](/skills/academic-cv-builder) | 为学术岗位排版 CV，涵盖出版物、基金、教学经历 |
| [reference-list-builder](/skills/reference-list-builder) | 规范整理推荐人列表，准备背调相关材料 |
| [offer-comparison-analyzer](/skills/offer-comparison-analyzer) | 多维度对比多个录用 offer，含总薪酬分析 |
| [resume-version-manager](/skills/resume-version-manager) | 管理不同版本的简历，维护母版简历，跟踪定制版本 |
| [creative-portfolio-resume](/skills/creative-portfolio-resume) | 在创意类岗位中平衡视觉设计与 ATS 兼容性 |
| [application-form-filler](/skills/application-form-filler) | 高效填写岗位申请表/网申表单 |
| [cold-email-writer](/skills/cold-email-writer) | 撰写触达招聘方、猎头或内推人的冷邮件 |

## 安装

### 方式一：CLI 安装（推荐）

```bash
# 全局安装全部 23 个技能（对所有项目生效）
npx skills add Paramchoudhary/ResumeSkills -g -y

# 仅安装到当前项目
npx skills add Paramchoudhary/ResumeSkills -y

# 查看已安装的技能
npx skills list

# 查看全局安装的技能
npx skills list --global
```

### 方式二：手动安装

```bash
# 克隆仓库并复制到技能目录
git clone https://github.com/Paramchoudhary/ResumeSkills.git
mkdir -p ~/.cursor/skills
cp -r ResumeSkills/skills/* ~/.cursor/skills/
```

### 方式三：直接下载

从 `/skills` 目录单独下载所需技能文件，放入你 AI 助手的技能目录即可。

### 卸载

```bash
# 按名称移除单个技能
npx skills remove resume-ats-optimizer
npx skills remove resume-bullet-writer

# 或按目录批量移除
rm -rf ~/.agents/skills/resume-*
rm -rf ~/.cursor/skills/resume-*
```

## 支持的 AI 助手

这些技能支持多种 AI 编程助手：

- **Cursor**（IDE）
- **Claude Code**（CLI）
- **OpenCode**
- **Windsurf**
- **Codex**
- **Gemini CLI**
- **Amp、Antigravity、Augment** 等 30+ 其他工具

## 使用方法

安装后，直接用中文向 AI 助手提出求职相关的请求即可：

```
"帮我把简历优化一下，要能过 ATS 筛选"
→ 使用 resume-ats-optimizer 技能

"我这几条经历写得太水了"
→ 使用 resume-bullet-writer 技能

"这个岗位我该不该投？" + 粘贴岗位描述
→ 使用 job-description-analyzer 技能

"帮我为这个岗位写一封求职信"
→ 使用 cover-letter-generator 技能

"我下周要去 Google 面试"
→ 使用 interview-prep-generator 技能

不知道用哪个技能也没关系——路由技能 using-resume-skills 会自动帮你判断
```

## 技能分类

### 路由入口
- `using-resume-skills` - 根据用户请求自动判断并路由到合适的技能

### 简历优化
- `resume-ats-optimizer` - 通过 ATS 筛选系统
- `resume-bullet-writer` - 撰写聚焦成果的经历条目
- `resume-quantifier` - 补充指标与数字
- `resume-formatter` - 干净易扫读的排版
- `resume-section-builder` - 有针对性的板块撰写

### 求职策略
- `job-description-analyzer` - 匹配度分析与策略
- `resume-tailor` - 针对具体岗位定制
- `resume-version-manager` - 多版本追踪
- `offer-comparison-analyzer` - offer 对比分析

### 配套材料
- `cover-letter-generator` - 个性化求职信
- `linkedin-profile-optimizer` - LinkedIn 领英主页优化
- `portfolio-case-study-writer` - 作品集内容
- `reference-list-builder` - 推荐人/背调材料
- `application-form-filler` - 申请表/网申表单
- `cold-email-writer` - 冷邮件触达

### 面试与谈判
- `interview-prep-generator` - STAR 故事与模拟练习
- `salary-negotiation-prep` - 谈薪策略

### 特定人群与岗位
- `tech-resume-optimizer` - 技术/工程/产品经理
- `executive-resume-writer` - 高管/VP
- `academic-cv-builder` - 学术岗位
- `creative-portfolio-resume` - 设计/创意类岗位
- `career-changer-translator` - 跨行转行

## 为什么这些技能重要

**问题所在：**
- 75% 的简历在人工看到之前就被 ATS 系统筛掉
- 每个岗位平均收到 250 份申请
- 大多数简历的经历条目平淡、缺少量化数据
- 求职者盲目投递不匹配的岗位，浪费时间

**解决方案：**
- 用优化的格式和关键词通过 ATS 筛选
- 用聚焦成果的经历条目脱颖而出
- 通过匹配度分析，只投真正适合的岗位
- 定制化申请让你更快拿到面试

**能带来什么：**
- 单份投递命中率提高 2~3 倍
- 回复质量更高
- 更快结束求职（平均节省约 2 个月）
- 薪资谈判收获更好（offer 往往多出上万元）

## 快速上手示例

### 示例一：简历全面优化

```
用户：这是我的简历【粘贴内容】，我想投数据科学家岗位，帮我优化一下。

AI 助手将：
1. 执行 ATS 兼容性检查
2. 对照数据科学家岗位的常见要求分析
3. 为经历条目补充量化指标
4. 建议补充的岗位关键词
5. 按 ATS 友好格式重新排版
```

### 示例二：针对具体岗位定制

```
用户：这是岗位描述【粘贴】和我的简历【粘贴】，我该投吗？

AI 助手将：
1. 计算匹配度评分
2. 找出差距与优势
3. 指出岗位信息中的任何红旗信号
4. 给出简历定制策略
5. 生成求职信的答题要点
```

### 示例三：面试准备

```
用户：我下周要去【公司】面试【岗位】，这是我的简历，帮我准备一下。

AI 助手将：
1. 根据你的经历生成 STAR 故事
2. 预测可能的面试问题
3. 为每条经历准备讲述要点
4. 补充该公司相关的准备建议
5. 准备好你要问回对方的问题
```

## 参与贡献

发现了可以改进某个技能的方式？有新技能的建议？欢迎提交 PR 和 issue！

请参阅 [CONTRIBUTING.md](CONTRIBUTING.md) 了解贡献规范。

### 贡献方向
- 改进现有技能的指引内容
- 补充行业专属示例
- 为细分场景创建新技能
- 修正错别字或让表述更清晰
- 补充翻译（本仓库中文版即由此而来）

## 许可证

MIT 许可证——这些技能想怎么用都可以。

详见 [LICENSE](LICENSE)。

## 关于

面向 Claude Code 的简历与求职技能库。涵盖 ATS 优化、经历条目撰写、岗位匹配、面试准备与职业发展。

**关键词：** 简历、CV、ATS、找工作、求职、跳槽、面试、求职信、领英、薪资谈判、岗位申请、resume、job search、career

---

*为每一位求职者用心打造。祝求职顺利！*
