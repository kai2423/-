# 项目开发

dao层放送sql

```java
StringBuilder sql = new StringBuilder(200);
    	sql.append("select max(to_number(serialNo)) from GSAccountAdminFee where intermediaryCode=?'");
    	sql.append(intermediaryCode);
    	sql.append("'");
//		HibernateSQLQuery hql = new HibernateSQLQuery(sql.toString());
//	     Object in = this.queryUniqueObject(hql);
    	List<Param> list = new ArrayList<Param>();
    	list.add(new Param(intermediaryCode, Hibernate.STRING));
    	PreparedSQLQuery psq = new PreparedSQLQuery(sql.toString(), list);
		return this.queryUniqueObject(psq);
```

## web层

​	

***

## service

## dao





文件修改

com.sinosoft.application.sales.web.ctrl.GSTestController

sales/test/test.jsp