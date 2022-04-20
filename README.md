# Rust编程语言-中文

![Build Status](https://github.com/rust-lang/book/workflows/CI/badge.svg)

此存储库包含《Rust编程语言》一书的源代码。

[这本书在印刷出版上出售][nostarch].

[nostarch]: https://nostarch.com/rust

你也可以在网上免费阅读这本书。请查看随附的书最新的 [stable], [beta], 或 [nightly] Rust releases。 要意识到这些问题在这些版本中，可能已经在这个存储库中修复了版本更新的频率较低。

[stable]: https://doc.rust-lang.org/stable/book/
[beta]: https://doc.rust-lang.org/beta/book/
[nightly]: https://doc.rust-lang.org/nightly/book/

下载本书中出现的所有代码清单[releases] 。

[releases]: https://github.com/rust-lang/book/releases

## 必要条件

构建这本书需要[mdBook]，理想情况下与rust-lang/rust在[this file][rust-mdbook]中使用。要获得它请使用以下命令：

[mdBook]: https://github.com/rust-lang-nursery/mdBook
[rust-mdbook]: https://github.com/rust-lang/rust/blob/master/src/tools/rustbook/Cargo.toml

```bash
$ cargo install mdbook --vers [version-num]
```

## 构建

要构建该书，请使用以下命令：

```bash
$ mdbook build
```

输出将在"book"子目录中。要查看它，请在你的网络浏览器中打开它。

_Firefox:_
```bash
$ firefox book/index.html                       # Linux
$ open -a "Firefox" book/index.html             # OS X
$ Start-Process "firefox.exe" .\book\index.html # Windows (PowerShell)
$ start firefox.exe .\book\index.html           # Windows (Cmd)
```

_Chrome:_
```bash
$ google-chrome book/index.html                 # Linux
$ open -a "Google Chrome" book/index.html       # OS X
$ Start-Process "chrome.exe" .\book\index.html  # Windows (PowerShell)
$ start chrome.exe .\book\index.html            # Windows (Cmd)
```

要运行测试，请执行以下操作：

```bash
$ mdbook test
```

## 贡献

我们很想得到你的帮助！请参见[CONTRIBUTING.md][contrib]了解我们正在寻找的各种贡献。

[contrib]: https://github.com/rust-lang/book/blob/main/CONTRIBUTING.md

因为这本书是[印刷的](https://nostarch.com/rust),因为我们想要使在线版本的书与印刷版保持一致可能，我们解决您的问题可能需要比您习惯的时间更长的时间或拉请求。

到目前为止，我们一直在做一个更大的修订，以配合[Rust Editions](https://doc.rust-lang.org/edition-guide/)。在那些更大的修改后，我们只会纠正错误。如果您的问题或拉请求如果不是严格地修复错误，它可能会一直保留到下一次做一个大的修改：预计几个月或几年。非常感谢。感谢你的耐心！

### 翻译

我们很乐意帮忙翻译这本书！请参阅[Translations]标签以加入目前正在进行的努力。打开一个新问题开始工作一门新语言！我们正在等待多语言的[mdbook support]在我们合并之前，请随意开始！

[Translations]: https://github.com/rust-lang/book/issues?q=is%3Aopen+is%3Aissue+label%3ATranslations
[mdbook support]: https://github.com/rust-lang-nursery/mdBook/issues/5

## 拼写检查

要扫描源文件中的拼写错误，可以使用拼写检查。`spellcheck.sh`目录中找到。它需要一本有效单词的字典，这在`ci/dictionary.txt`中提供。如果脚本生成错误肯定（比如，你使用了脚本认为无效的单词`BTreeMap`），你需要把这个词加到`ci/dictionary.txt`字典里。（将排序顺序保留为一致性）。
