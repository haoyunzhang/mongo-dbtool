# mongo-dbtool
运用gopkg.in/mgo.v2包连接mongo数据库，对mongo数据库及集合会话进行循环使用，连接好后，简单的使用一个函数可以连接到相应的数据及集合。

# 使用方法
数据库的连接，获取一个handler。

DataBaseAddr, DataBaseUser, DataBasePassWord分别为数据库地址，用户名，密码
mongoHandler, err := mongo.NewHandler(DataBaseAddr, DataBaseUser, DataBasePassWord)

获取集合连接，其中dbName, colName 分别是数据库名和集合名
col := mongoHandler.Collection(dbName, colName)

col即为数据dbName的colName集合的连接。