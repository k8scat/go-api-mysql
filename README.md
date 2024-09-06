## 使用 MySQL 的 Golang API

一个使用 Gin-Gonic 框架和 MySQL 的 Golang Restful API。此 API 允许您创建、读取、更新和删除日程。

## 设置 API

克隆仓库后，将 `.env.example` 文件复制到 `.env` 并根据您的 MySQL 配置更新值。确保您的 MySQL 服务器正在运行，并且具有必要的权限，并且已根据 `.env` 文件中提供的名称创建了数据库。

完成配置后，您可以运行以下命令来启动 API：

```sh
go run main.go
```

这将启动位于 http://localhost:8080 的 API。

现在，您可以使用 API 与 MySQL 数据库进行交互。请参阅 使用 API 以查看可用的端点。

## 使用 API
一旦 API 运行，您可以使用以下端点与 API 进行交互。 我们有 Get、Post、Patch 和 Delete 方法与 API 进行交互。


| Method | Endpoint | Description | Body |
| --- | --- | --- | --- |
| GET | /health | Check the health of the API | None |
| GET | /api/schedules | Get all the schedules | None |
| POST | /api/schedules | Create a new schedule | `{"content": "Schedule content"}` |
| PATCH | /api/schedules/:id | Update a schedule | `{"content": "Updated schedule content"}` |
| DELETE | /api/schedules/:id | Delete a schedule | None |
