# Baseline 文件目录

此目录用于存放需要上传到 Git 仓库 `release/baseline/{基线号}/` 目录下的文件。

## 使用说明

1. **将需要上传的文件放到此目录下**
   - 可以直接放文件
   - 也可以创建子目录来组织文件

2. **支持的文件类型**
   - 任何类型的文件都可以上传
   - 常见文件类型：`.txt`, `.pdf`, `.docx`, `.xlsx`, `.json`, `.xml` 等

3. **目录结构会被保留**
   - 如果你在此目录下创建了子目录，上传到 Git 时会保持相同的目录结构
   - 例如：`baseline_files/docs/readme.txt` 会被上传到 `release/baseline/{基线号}/docs/readme.txt`

## 示例

```
baseline_files/
├── README.md           # 此说明文件（上传时会被包含）
├── deployment.yaml     # 部署配置文件
├── release_notes.txt   # 发版说明
└── docs/               # 文档子目录
    ├── manual.pdf      # 使用手册
    └── changelog.md    # 变更日志
```

## 注意事项

- 如果此目录为空或不存在，程序会跳过上传步骤并给出警告
- 每次发版都会上传此目录下的所有文件到对应的基线目录
- 建议在发版前清理不需要的文件，避免上传无关文件
