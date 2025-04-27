##  Git 停止追踪已跟踪的文件/目录


```
# 停止追踪单个文件 (文件仍存在于本地)
git rm --cached filename

# 停止追踪整个目录（递归操作）
git rm -r --cached directory/
```

## 常见使用场景
‌
1‌. 停止追踪已提交文件‌：例如将文件添加到 .gitignore 后，需执行 git rm --cached 以停止追踪.

‌2. 保留本地敏感文件‌：从版本库中移除配置文件（如密钥文件），但本地继续使用。

## 注意事项‌

‌批量操作需谨慎‌：使用 git rm -r --cached . 可能导致误删索引中的其他文件。

‌及时提交变更‌：未提交前可通过 git restore --staged <file> 撤销操作
