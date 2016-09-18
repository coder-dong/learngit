Git is a distributed version control system.
Git is free software under the GPL.

kjava.lang.Exception: org.springframework.dao.DataIntegrityViolationException: 
### Error updating database.  Cause: com.mysql.jdbc.MysqlDataTruncation: Data truncation: Data too long for column 'order_id' at row 1
### The error may involve com.jd.jr.cf.statistics.dao.CfBizserviceExceptionLogDao.insert-Inline
### The error occurred while setting parameters
### SQL: insert into cf_bizservice_exception_log (order_id, loan_id,       merchant_order_id, seq_no_interface, class_name,        method_name, error_code, error_info,        create_date)     values (?, ?,       ?, ?, ?,        ?, ?, ?,        now())
### Cause: com.mysql.jdbc.MysqlDataTruncation: Data truncation: Data too long for column 'order_id' at row 1
; SQL []; Data truncation: Data too long for column 'order_id' at row 1; nested exception is com.mysql.jdbc.MysqlDataTruncation: Data truncation: Data too long for column 'order_id' at row 1
	at com.jd.jmq.client.consumer.TopicConsumer.dispatchMessages(TopicConsumer.java:616)
	at com.jd.jmq.client.consumer.TopicConsumer$TopicMessageDispatcher.dispatch(TopicConsumer.java:679)
	at com.jd.jmq.client.consumer.GroupConsumer.pull(GroupConsumer.java:285)
	at com.jd.jmq.client.consumer.GroupConsumer$QueueConsumer.run(GroupConsumer.java:445)
	at java.lang.Thread.run(Thread.java:745)
Caused by: org.springframework.dao.DataIntegrityViolationException: 
### Error updating database.  Cause: com.mysql.jdbc.MysqlDataTruncation: Data truncation: Data too long for column 'order_id' at row 1
### The error may involve com.jd.jr.cf.statistics.dao.CfBizserviceExceptionLogDao.insert-Inline
### The error occurred while setting parameters
### SQL: insert into cf_bizservice_exception_log (order_id, loan_id,       merchant_order_id, seq_no_interface, class_name,        method_name, error_code, error_info,        create_date)     values (?, ?,       ?, ?, ?,        ?, ?, ?,        now())
### Cause: com.mysql.jdbc.MysqlDataTruncation: Data truncation: Data too long for column 'order_id' at row 1
; SQL []; Data truncation: Data too long for column 'order_id' at row 1; nested exception is com.mysql.jdbc.MysqlDataTruncation: Data truncation: Data too long for column 'order_id' at row 1
	at org.springframework.jdbc.support.SQLStateSQLExceptionTranslator.doTranslate(SQLStateSQLExceptionTranslator.java:100)
	at org.springframework.jdbc.support.AbstractFallbackSQLExceptionTranslator.translate(AbstractFallbackSQLExceptionTranslator.java:72)
	at org.springframework.jdbc.support.AbstractFallbackSQLExceptionTranslator.translate(AbstractFallbackSQLExceptionTranslator.java:80)
	at org.springframework.jdbc.support.AbstractFallbackSQLExceptionTranslator.translate(AbstractFallbackSQLExceptionTranslator.java:80)
	at org.mybatis.spring.MyBatisExceptionTranslator.translateExceptionIfPossible(MyBatisExceptionTranslator.java:73)
	at org.mybatis.spring.SqlSessionTemplate$SqlSessionInterceptor.invoke(SqlSessionTemplate.java:368)
	at com.sun.proxy.$Proxy29.insert(Unknown Source)
	at org.mybatis.spring.SqlSessionTemplate.insert(SqlSessionTemplate.java:240)
	at org.apache.ibatis.binding.MapperMethod.execute(MapperMethod.java:46)
	at org.apache.ibatis.binding.MapperProxy.invoke(MapperProxy.java:43)
	at com.sun.proxy.$Proxy35.insert(Unknown Source)
	at com.jd.jr.cf.statistics.mq.BizAppRuntimeExceptionTipHandler.onMessage(BizAppRuntimeExceptionTipHandler.java:74)
	at com.jd.jr.cf.statistics.mq.AbstractMessageListener.onMessage(AbstractMessageListener.java:27)
	at com.jd.jmq.client.consumer.TopicConsumer$1.call(TopicConsumer.java:589)
	at com.jd.jmq.client.consumer.TopicConsumer$1.call(TopicConsumer.java:546)
	at com.jd.registry.util.RetryLoop.execute(RetryLoop.java:30)
	at com.jd.jmq.client.consumer.TopicConsumer.dispatchMessages(TopicConsumer.java:546)
	... 4 more
Caused by: com.mysql.jdbc.MysqlDataTruncation: Data truncation: Data too long for column 'order_id' at row 1
	at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:4094)
	at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:4028)
	at com.mysql.jdbc.MysqlIO.sendCommand(MysqlIO.java:2490)
	at com.mysql.jdbc.MysqlIO.sqlQueryDirect(MysqlIO.java:2651)
	at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2683)
	at com.mysql.jdbc.PreparedStatement.executeInternal(PreparedStatement.java:2144)
	at com.mysql.jdbc.PreparedStatement.execute(PreparedStatement.java:1379)
	at org.apache.commons.dbcp.DelegatingPreparedStatement.execute(DelegatingPreparedStatement.java:172)
	at org.apache.commons.dbcp.DelegatingPreparedStatement.execute(DelegatingPreparedStatement.java:172)
	at sun.reflect.GeneratedMethodAccessor104.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:606)
	at org.apache.ibatis.logging.jdbc.PreparedStatementLogger.invoke(PreparedStatementLogger.java:55)
	at com.sun.proxy.$Proxy47.execute(Unknown Source)
	at org.apache.ibatis.executor.statement.PreparedStatementHandler.update(PreparedStatementHandler.java:41)
	at org.apache.ibatis.executor.statement.RoutingStatementHandler.update(RoutingStatementHandler.java:66)
	at org.apache.ibatis.executor.SimpleExecutor.doUpdate(SimpleExecutor.java:45)
	at org.apache.ibatis.executor.BaseExecutor.update(BaseExecutor.java:100)
	at org.apache.ibatis.executor.CachingExecutor.update(CachingExecutor.java:75)
	at sun.reflect.GeneratedMethodAccessor505.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:606)
	at org.apache.ibatis.plugin.Plugin.invoke(Plugin.java:59)
	at com.sun.proxy.$Proxy76.update(Unknown Source)
	at org.apache.ibatis.session.defaults.DefaultSqlSession.update(DefaultSqlSession.java:148)
	at org.apache.ibatis.session.defaults.DefaultSqlSession.insert(DefaultSqlSession.java:137)
	at sun.reflect.GeneratedMethodAccessor226.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:606)
	at org.mybatis.spring.SqlSessionTemplate$SqlSessionInterceptor.invoke(SqlSessionTemplate.java:358)
	... 15 more
