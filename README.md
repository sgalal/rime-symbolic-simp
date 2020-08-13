# rime-symbolic-simp

rime 符号输入方案（简化字版）

繁体字版：[sgalal/rime-symbolic](https://github.com/sgalal/rime-symbolic)

## 用法

在 rime 用户文件夹中加入 `symbolic_simp.dict.yaml`。

在常用方案的 `*.schema.yaml` 中加入：

1. `switches` 中加入

```yaml
  - name: symbolic_simp
    reset: 1
    states: [ 无符号, 有符号 ]
```

2. `engine` 的 `filters` 中加入：

```yaml
  - simplifier@symbolic_simp
```

3. 在文件末尾加入：

```yaml
symbolic_simp:
  opencc_config: symbolic_simp
  option_name: symbolic_simp
  tips: all
```

在常用方案的 `*.dict.yaml` 中加入：

```yaml
import_tables:
  - symbolic_simp
```

将 `opencc` 文件夹中的文件放入 rime 用户文件夹中的 `opencc` 文件夹中。

重新部署即可。
