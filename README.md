# 构建一个工程化的前端库，并结合 Github Actions，自动发布到 Github 和 NPM 的整个详细流程

## 摘自微信收藏

## 相关配置清单

1. Eslint
2. Prettier
3. Commitlint
4. Husky
5. Jest
6. GitHub Actions
7. Semantic Release

## 初始化

### 在 Github 上创建一个 repo,拉下来之后通过npm init -y初始化。然后创建src文件夹，写入index.ts

### 我们将项目定义为ESM规范,前端社区正逐渐向ESM标准迁移，从Node v12.0.0开始，只要设置了 "type": "module", Node 会将整个项目视为ESM规范，我们就可以直接写裸写import/export

### publishConfig.access表示当前项目发布到NPM的访问级别，它有 restricted和public两个选项,restricted表示我们发布到NPM上的是私有包（收费），访问级别默认为restricted,因为我们是开源项目所以标记为public

## 配置

### 创建项目之后，我们开始安装工程化相关的依赖，因为我们是 TypeScript 项目，所以也需要安装 TypeScript 的依赖
