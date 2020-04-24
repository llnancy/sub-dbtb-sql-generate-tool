# sub-dbtb-sql-generate-tool
分库分表SQL生成工具

- 生成分库分表建表语句
- 生成分库分表删表语句

## 示例
建立`8库` 每库`8`表共`64`表

库名前缀：`userdb`，表名前缀：`user`。

模板库名：`userdb`，模板表名：`user`。

### `main`方法启动
`simple-main`项目下`com.sunchaser.sqltool.SqlGenerate`类中的`main`方法启动。

`IDEA`中启动参数输入：
```
CREATE userdb user userdb user 8 64
```

参数详解：
- `CREATE`：执行动作，可选`CREATE/DROP`。
- `userdb`：分库名前缀。
- `user`：分表名前缀。
- `userdb`：模板库名。
- `user`：模板表名。
- `8`：分库数量。
- `64`：分表数量。

控制台输出：
```
CREATE TABLE userdb_00.user_00 like userdb.user;
CREATE TABLE userdb_00.user_08 like userdb.user;
CREATE TABLE userdb_00.user_16 like userdb.user;
CREATE TABLE userdb_00.user_24 like userdb.user;
CREATE TABLE userdb_00.user_32 like userdb.user;
CREATE TABLE userdb_00.user_40 like userdb.user;
CREATE TABLE userdb_00.user_48 like userdb.user;
CREATE TABLE userdb_00.user_56 like userdb.user;

CREATE TABLE userdb_01.user_01 like userdb.user;
CREATE TABLE userdb_01.user_09 like userdb.user;
CREATE TABLE userdb_01.user_17 like userdb.user;
CREATE TABLE userdb_01.user_25 like userdb.user;
CREATE TABLE userdb_01.user_33 like userdb.user;
CREATE TABLE userdb_01.user_41 like userdb.user;
CREATE TABLE userdb_01.user_49 like userdb.user;
CREATE TABLE userdb_01.user_57 like userdb.user;

CREATE TABLE userdb_02.user_02 like userdb.user;
CREATE TABLE userdb_02.user_10 like userdb.user;
CREATE TABLE userdb_02.user_18 like userdb.user;
CREATE TABLE userdb_02.user_26 like userdb.user;
CREATE TABLE userdb_02.user_34 like userdb.user;
CREATE TABLE userdb_02.user_42 like userdb.user;
CREATE TABLE userdb_02.user_50 like userdb.user;
CREATE TABLE userdb_02.user_58 like userdb.user;

CREATE TABLE userdb_03.user_03 like userdb.user;
CREATE TABLE userdb_03.user_11 like userdb.user;
CREATE TABLE userdb_03.user_19 like userdb.user;
CREATE TABLE userdb_03.user_27 like userdb.user;
CREATE TABLE userdb_03.user_35 like userdb.user;
CREATE TABLE userdb_03.user_43 like userdb.user;
CREATE TABLE userdb_03.user_51 like userdb.user;
CREATE TABLE userdb_03.user_59 like userdb.user;

CREATE TABLE userdb_04.user_04 like userdb.user;
CREATE TABLE userdb_04.user_12 like userdb.user;
CREATE TABLE userdb_04.user_20 like userdb.user;
CREATE TABLE userdb_04.user_28 like userdb.user;
CREATE TABLE userdb_04.user_36 like userdb.user;
CREATE TABLE userdb_04.user_44 like userdb.user;
CREATE TABLE userdb_04.user_52 like userdb.user;
CREATE TABLE userdb_04.user_60 like userdb.user;

CREATE TABLE userdb_05.user_05 like userdb.user;
CREATE TABLE userdb_05.user_13 like userdb.user;
CREATE TABLE userdb_05.user_21 like userdb.user;
CREATE TABLE userdb_05.user_29 like userdb.user;
CREATE TABLE userdb_05.user_37 like userdb.user;
CREATE TABLE userdb_05.user_45 like userdb.user;
CREATE TABLE userdb_05.user_53 like userdb.user;
CREATE TABLE userdb_05.user_61 like userdb.user;

CREATE TABLE userdb_06.user_06 like userdb.user;
CREATE TABLE userdb_06.user_14 like userdb.user;
CREATE TABLE userdb_06.user_22 like userdb.user;
CREATE TABLE userdb_06.user_30 like userdb.user;
CREATE TABLE userdb_06.user_38 like userdb.user;
CREATE TABLE userdb_06.user_46 like userdb.user;
CREATE TABLE userdb_06.user_54 like userdb.user;
CREATE TABLE userdb_06.user_62 like userdb.user;

CREATE TABLE userdb_07.user_07 like userdb.user;
CREATE TABLE userdb_07.user_15 like userdb.user;
CREATE TABLE userdb_07.user_23 like userdb.user;
CREATE TABLE userdb_07.user_31 like userdb.user;
CREATE TABLE userdb_07.user_39 like userdb.user;
CREATE TABLE userdb_07.user_47 like userdb.user;
CREATE TABLE userdb_07.user_55 like userdb.user;
CREATE TABLE userdb_07.user_63 like userdb.user;
```

### `jar`包启动
命令行下进入`~/sub-dbtb-sql-generate-tool/simple-main`目录，使用命令`mvn clean package`对项目进行打包。

在生成的`target`目录下找到`simple-main-1.0-SNAPSHOT.jar`文件，命令行进入其所在目录，使用命令：

```
java -jar simple-main-1.0-SNAPSHOT.jar CREATE userdb user userdb user 8 64
```

按下回车后即可看到生成的建表语句。