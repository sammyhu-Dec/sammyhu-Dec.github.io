# sammyhu-Dec Tools

这是一个通过 GitHub Pages 托管的个人工具站点，用来集中发布可以直接在浏览器中使用的静态网页工具。

线上地址：

- 站点首页：https://sammyhu-dec.github.io/
- HSBC 多币种余额计算器：https://sammyhu-dec.github.io/tools/hsbc-multi-currency-balance-calculator/

## 工具列表

### HSBC 多币种余额计算器

用于帮助 HSBC Hong Kong 客户估算在 HSBC One 或 HSBC Premier 账户规则下，为满足前三个完整历月平均「全面理财总值」（Total Relationship Balance, TRB）要求，还需要补充多少港币等值资产。

主要能力：

- 判断用户是否可能属于 HSBC One 低额结存服务费豁免或不受影响人群
- 支持 HSBC One、HSBC Premier 和自定义港币门槛
- 支持港币、人民币、美元、澳元、欧元等常见币种
- 根据实时汇率将外币折算为港币参与估算
- 支持汇款记录和支出记录
- 输出一次性存款建议和每日存款计划
- 支持下载计算结果图片

工具说明文档位于 `tools/hsbc-multi-currency-balance-calculator/README.md`。

## 项目结构

```text
sammyhu-Dec.github.io/
├── README.md
├── index.html
├── assets/
│   └── .gitkeep
├── hsbc-multi-currency-balance-calculator/
│   └── index.html
└── tools/
    └── hsbc-multi-currency-balance-calculator/
        ├── index.html
        ├── README.md
        └── HSBC_One_FAQ.pdf
```

说明：

- `index.html` 是网站首页和工具导航页。
- `assets/` 用于放置后续多个工具共用的静态资源。
- `tools/` 是所有独立小工具的主目录。
- `tools/hsbc-multi-currency-balance-calculator/` 是 HSBC 计算器工具目录。
- `hsbc-multi-currency-balance-calculator/index.html` 仅用于旧链接跳转，主项目代码不再放在该目录。

## 新增工具规范

后续新增工具时，建议继续使用小写英文和连字符作为目录名，例如：

```text
tools/example-tool/
├── index.html
└── README.md
```

如果某个工具需要单独的 PDF、图片或数据文件，可以放在该工具目录下；如果多个工具都会复用同一份资源，再放入根目录的 `assets/`。

## 本地预览

这是一个纯静态网页项目，可以直接部署到 GitHub Pages。若要本地预览：

```bash
python -m http.server 9090
```

然后访问：

```text
http://localhost:9090/
http://localhost:9090/tools/hsbc-multi-currency-balance-calculator/
```

## 部署

仓库名为 `sammyhu-Dec.github.io`，提交到 `main` 分支后由 GitHub Pages 自动发布。

## 免责声明

本项目中的金融计算工具仅用于个人估算和信息整理，不构成银行、税务、法律、投资或财务建议。具体费用规则、账户状态、资产计入范围、汇率和扣费安排，请以 HSBC Hong Kong 官方说明、账户月结单、HSBC HK App 及银行最终记录为准。
