# 前端课程作业与 GitHub Pages 部署说明

学号：23307221029  
姓名：张妍

## 一、目录结构

```text
frontend-homework-23307221029/
├── index.html
├── README.md
├── .gitignore
├── homework1/
│   └── index.html
├── homework2/
│   ├── index.html
│   ├── flex_demo.html
│   ├── bdqn_course.html
│   ├── news_center.html
│   ├── free_trial.html
│   ├── team_show.html
│   └── css3_func.html
└── homework3/
    ├── index.html
    ├── jd_carousel.html
    ├── cosmetics_list.html
    ├── bdqn_reg.html
    ├── jd_homework.html
    ├── calculator.html
    └── images/
        └── README.md
```

作业二保留 6 个独立页面，因为每一页都有自己的 CSS 和页面结构。合并后会增加样式冲突和调试难度，独立保留更方便维护，并由 `homework2/index.html` 统一导航。

作业三的现有源文件同样是 5 个独立页面，因此也保留独立页面，并由 `homework3/index.html` 统一导航。

## 二、第一次上传到 GitHub

先在 GitHub 网页创建一个新仓库：

1. 打开 https://github.com/new 。
2. `Repository name` 填写 `frontend-homework-23307221029`。
3. 选择 `Public`。
4. 不要勾选 `Add a README file`、`.gitignore` 或 `license`。
5. 点击 `Create repository`。

然后打开终端，把下列命令逐行复制执行，并把 `你的用户名` 替换成真实 GitHub 用户名：

```bash
cd C:\Users\你的电脑用户名\Documents\frontend-homework-23307221029
git init
git add .
git commit -m "第一次提交：三次前端作业"
git branch -M main
git remote add origin https://github.com/你的用户名/frontend-homework-23307221029.git
git push -u origin main
```

如果 Git 提示没有配置身份信息，先执行下面两条，再重新提交：

```bash
git config --global user.name "张妍"
git config --global user.email "你的GitHub绑定邮箱"
```

如果推送时要求登录，可以使用 Git Credential Manager 弹出的浏览器登录，或使用 GitHub Personal Access Token 作为密码。

## 三、开启 GitHub Pages

1. 打开 `https://github.com/你的用户名/frontend-homework-23307221029`。
2. 点击 `Settings`。
3. 左侧点击 `Pages`。
4. 在 `Build and deployment` 中，`Source` 选择 `Deploy from a branch`。
5. `Branch` 选择 `main`，文件夹选择 `/ (root)`。
6. 点击 `Save`。
7. 等待 1 到 3 分钟，然后刷新 Pages 页面。

最终访问地址：

```text
https://你的用户名.github.io/frontend-homework-23307221029/
```

## 四、更新作业

以后修改任意 HTML 或图片后，只需要在 `frontend-homework-23307221029` 根目录执行：

```bash
git add .
git commit -m "更新前端作业"
git push
```

GitHub Pages 通常会在推送后 1 到 3 分钟内自动更新。

## 五、上传后验证清单

- [ ] GitHub 仓库是 `Public`
- [ ] `https://github.com/你的用户名/frontend-homework-23307221029` 能打开
- [ ] `https://你的用户名.github.io/frontend-homework-23307221029/` 能打开
- [ ] 首页 3 个作业链接都能打开
- [ ] 作业二 6 个页面链接都能打开
- [ ] 作业三 5 个页面链接都能打开
- [ ] 轮播、注册表单和计算器交互正常
- [ ] 图片没有裂图
- [ ] 关闭 Wi-Fi、使用手机流量后仍能访问