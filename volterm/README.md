# VOLTERM · 波动率终端

Bloomberg 风格的 A股/港股 历史波动率分析工具。

## 功能
- 实时行情数据（Yahoo Finance）
- 历史波动率 HV（自定义窗口：10/20/30日）
- 60日滚动 Beta（相对大盘）
- 波动率历史分位数
- 风险等级评估

## 支持的代码格式
| 输入 | 解析结果 |
|------|----------|
| `300476` | 300476.SZ（深交所） |
| `600519` | 600519.SS（上交所） |
| `0700` | 0700.HK（港交所） |

## 部署到 Vercel（免费）

1. 安装 Vercel CLI（可选）或直接拖拽部署
2. 注册 [vercel.com](https://vercel.com)
3. 点击 **Add New Project** → **Import** 或拖拽整个文件夹
4. 无需任何配置，直接 Deploy
5. 部署完成后获得 `https://xxx.vercel.app` 链接

## 本地运行

```bash
npm i -g vercel
vercel dev
# 访问 http://localhost:3000
```

## 项目结构

```
volterm/
├── index.html        # 前端页面
├── api/
│   └── proxy.js      # Vercel 服务端代理（转发 Yahoo Finance）
├── vercel.json       # Vercel 路由配置
└── README.md
```

## 技术栈
- 纯 HTML/CSS/JS 前端
- Chart.js 4.x 图表
- Vercel Serverless Functions（Node.js）代理
