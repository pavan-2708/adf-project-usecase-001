# adf-project-usecase-001
1. read the orders.csv from HTTP and ingest the data to landing layer (ADLS Gen2).
2. customers.csv file avaiable in landing layer (data lake) ingest that in Azure SQL Datasabe.
3. Create mapping dataflow apply transformation on the data and store the result to final datastore.we 2 sources ADLS and Az SQL db
   Perform join transformation,
   select transformation remove column(customer_email,customer_password,order_customer_id) and unncessary columns,
   Perform filter on customer_city == "caguas"
   Sort on customer_fname
   Use sink adls gen2 .csv
