# ZSW Books Evaluation

为非凡精读馆（帆书平台）生成专业的书籍选书评估报告。

## 功能

- 完整阅读PDF/Word/TXT格式电子书
- 生成包含9大要素的专业选书评估报告
- 自动创建飞书云文档并开通管理权限
- 支持社交媒体热点分析
- 支持用户痛点调研

## 安装

```bash
clawhub install zsw-books-evaluation
```

或从 GitHub 安装：

```bash
# 克隆到本地
git clone https://github.com/yourusername/zsw-books-evaluation.git

# 复制到 OpenClaw 技能目录
cp -r zsw-books-evaluation ~/.openclaw/workspace/skills/
```

## 配置

首次使用时需要配置飞书 open_id，以便创建文档时自动开通管理权限。

### 方式1：通过飞书对话（推荐）

如果你通过飞书与 OpenClaw 对话，系统可以自动获取你的 open_id。

### 方式2：手动配置

创建配置文件 `~/.openclaw/workspace/skills/zsw-books-evaluation/config.yaml`：

```yaml
feishu:
  owner_open_id: "ou_xxxxxxxx"  # 你的飞书 open_id
```

### 方式3：运行时配置

首次使用时会提示你选择配置方式，并引导你完成设置。

## 获取 open_id 方法

1. 打开飞书 → 点击左上角头像
2. 进入「设置」→「账号与安全」
3. 找到「open_id」并复制

## 使用

发送书籍文件（PDF/Word/TXT）并告知需要评估，例如：

```
帮我评估这本书 [上传文件]
生成这本书的选书报告
分析一下这本书是否适合讲书
```

## 报告内容

生成的报告包含9大要素：

1. 书籍基本信息
2. 是否适合非凡精读馆选入（赛道分析、竞品分析）
3. 整本书的知识框架结构
4. 近半年社交媒体相关热点
5. 豆瓣/微信读书用户痛点
6. 可补充的相关知识
7. 讲书大纲建议（含时长分配）
8. 综合评估与建议
9. 附录

## 工作原则

- ✅ 完整阅读全书，绝不只看目录
- ✅ 覆盖全书所有章节
- ✅ 详略得当，核心内容详讲
- ✅ 信息准确，不确定则标注"待核实"
- ✅ 自动开通飞书文档管理权限

## 依赖

- OpenClaw >= 2.20.0
- feishu_doc 技能
- OCR 技能（用于扫描版PDF）

## License

MIT

## 作者

周玉玉 / 周珅玮
