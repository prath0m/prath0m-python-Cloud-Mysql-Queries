# MySQL Configuration on Clever Cloud

This guide will help you configure a MySQL database on Clever Cloud and verify the connection using the MySQL shell.

## Prerequisites

Before you begin, ensure you have the following:
- A Clever Cloud account
- MySQL client installed on your local machine

## Step 1: Create a MySQL Add-on on Clever Cloud

1. **Log in to Clever Cloud:**
   - Go to [Clever Cloud](https://www.clever-cloud.com/) and log in.

2. **Create a MySQL Add-on:**
   - Navigate to the "Add-ons" section in your Clever Cloud dashboard.
   - Click on "Add an Add-on" and select "MySQL" from the available options.
   - Choose your preferred region and plan.
   - Click "Create Add-on" to provision the MySQL instance.

## Step 2: Retrieve MySQL Connection Details

Once the MySQL add-on is created:

1. **Get Connection Details:**
   - Go to the "Add-ons" section and select your MySQL instance.
   - Navigate to the "Information" tab to find the following connection details:
     - **Host:** `<your-mysql-host>`
     - **Port:** `3306`
     - **Database Name:** `<your-database-name>`
     - **User:** `<your-username>`
     - **Password:** `<your-password>`

## Step 3: Verify the Connection Using MySQL Shell

To verify the connection, use the MySQL shell:

1. **Open MySQL Shell:**
   - Open your terminal or command prompt.

2. **Connect to MySQL:**
   - Run the following command, replacing the placeholders with your actual connection details:
     ```bash
     mysql -h <your-mysql-host> -P 3306 -u <your-username> -p<your-password> <your-database-name>
     ```
   - Example:
     ```bash
     mysql -h mysql-1234.clever-cloud.com -P 3306 -u user123 -pMySecretPassword database_name
     ```

3. **Check the Connection:**
   - If the connection is successful, you should see the MySQL prompt:
     ```bash
     mysql>
     ```
   - You can now run SQL commands to interact with your database.

## Step 4: Testing the Connection

To ensure everything is working:

1. **Show Databases:**
   ```sql
   SHOW DATABASES;
