title: JSBox的SQLite数据库笔记
date: 2022-06-18 16:00:00
tags:
- 编程
- JSBox
---

1. 创建数据库

```javascript
try {
    const db = $sqlite.open(DATABASEFILE),
         sql = `CREATE TABLE IF NOT EXISTS ${TABLE_ID}(id TEXT PRIMARY KEY NOT NULL, value TEXT, timestamp INTEGER ,data BLOB)`;
    db.update({ sql: sql, args: undefined });
    db.close();
} catch (error) {
    $console.error(error);
}
```