# spacemacs 安装及使用

## 安装

```bash
# 安装emacs
sudo apt install emacs
# 为git 配置代理
git config --global http.proxy http://127.0.0.1:12345
# 安装spacemacs
git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d
# 安装source-code-pro字体
[ -d /usr/share/fonts/opentype ] || sudo mkdir /usr/share/fonts/opentype
sudo git clone --depth 1 --branch release https://github.com/adobe-fonts/source-code-pro.git /usr/share/fonts/opentype/scp
sudo fc-cache -f -v
# 启动emacs加载配置
emacs
# 更新插件源
# .spacemacs内dotspacemacs/user-init()
(setq configuration-layer--elpa-archives
    '(("melpa-cn" . "http://mirrors.tuna.tsinghua.edu.cn/elpa/melpa/")
      ("org-cn"   . "http://mirrors.tuna.tsinghua.edu.cn/elpa/org/")
      ("gnu-cn"   . "http://mirrors.tuna.tsinghua.edu.cn/elpa/gnu/")))
# emacsclient -t 模式下state-line有些字符显示不全
# 安装telephone line
# ~/.spacemacs 在additional packages下设置包
# user-config下设置其他
# C+q+R重启emacs

# 安装themes
# emacs.d/themes下放置主题文件
# emacs.d/init.l设置自动加载themes目录和相关主题
# emacs内部M-x => load-theme => enable-theme 
```

link:

- <https://github.com/syl20bnr/spacemacs>
- <https://github.com/adobe-fonts/source-code-pro/issues/17#issuecomment-8967116>
- <https://mirror.tuna.tsinghua.edu.cn/help/elpa/>
- <https://github.com/dbordak/telephone-line>
