# TEZ-settings-for-BI
Using TEZ engine to speed up Hadoop data import into BI Tools (Tableau, Power BI)


You can either use the settings in the hive query directly. Please add the following lines to your hive ddl.

set hive.execution.engine=tez;
set hive.tez.java.opts=-XX:+UseNUMA -XX:+UseG1GC;
set hive.tez.auto.reducer.parallelism = true;
set hive.tez.dynamic.partition.pruning=true; 

To use TEZ in bi tools, in your odbc connection please add the settings by clicking advanced options > server side properties> add
