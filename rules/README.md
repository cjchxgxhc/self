# 域名白名单列表

这是从 anti-AD 项目的 `white_domain_list.php` 规则文件中提取的纯域名白名单。

## 📋 文件说明

- **domains.txt** - 纯域名列表，每行一个域名，按字母顺序排列
- **STATS.txt** - 统计信息，包含处理统计和更新时间
- **README.md** - 本说明文件

## 📊 统计信息

请查看 `STATS.txt` 获取最新的统计信息。

## 🔗 源项目

[privacy-protection-tools/anti-AD](https://github.com/privacy-protection-tools/anti-AD)

## 📝 规则说明

| Value | 含义 | 状态 |
|-------|------|------|
| 0 | 单条域名白名单 | ✅ 保留 |
| 1 | 包括子域名白名单 | ✅ 保留 |
| 2 | 主域名白名单 | ✅ 保留 |
| -1 | 失效/禁用规则 | ❌ 排除 |

## 🔄 更新频率

- 定时更新：每天中国时间 04:00 AM
- 自动推送：有变化时自动提交到 Git

## 💡 使用方式

### 直接下载
```bash
curl -L -o domains.txt \
  https://raw.githubusercontent.com/<用户>/<仓库>/main/rules/domains.txt
```

### 在脚本中使用
```bash
while IFS= read -r domain; do
  # 处理每个域名
  echo "$domain"
done < domains.txt
```

## 📞 支持

如有问题，请查看工作流日志或提交 Issue。
