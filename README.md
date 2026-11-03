# kernel-4.19.90-52.70.orig.v2207.a.ky10.loongarch64 五件套 RPM（无补丁对照构建）

`kernel-52.70-orig-core5.tar.gz`（109M，超 GitHub 单文件 100MB 限制，拆为 2 个分卷）。

## 重组方法

```bash
git clone https://github.com/NobelXun/tmp-copy-file.git
cd tmp-copy-file
cat kernel-52.70-orig-core5.tar.gz.part-* > kernel-52.70-orig-core5.tar.gz
sha256sum kernel-52.70-orig-core5.tar.gz
```

校验值（必须一致）：

```
574a35cf0b799c0fd337cbac05fe6199cffa45cd6e02fb892c5549fa8a8a3720  kernel-52.70-orig-core5.tar.gz
```

## 内容（5 个 RPM，来自 52.70.orig base-version）

- kernel（元包）
- kernel-core
- kernel-modules
- kernel-modules-extra
- kernel-modules-internal

## 安装

```bash
tar -xzf kernel-52.70-orig-core5.tar.gz
cd kernel-52.70-orig-core5
sudo rpm -ivh --force --nodeps ./*.rpm
```

## 网络不畅时的直链下载（断点续传）

```bash
wget -c https://ghproxy.net/https://github.com/NobelXun/tmp-copy-file/raw/main/kernel-52.70-orig-core5.tar.gz.part-01
wget -c https://ghproxy.net/https://github.com/NobelXun/tmp-copy-file/raw/main/kernel-52.70-orig-core5.tar.gz.part-02
```
