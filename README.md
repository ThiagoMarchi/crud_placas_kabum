<h1 align="center"> CRUD Python + Selenium </h1>

<p align="center"> CRUD using MySQL, Selenium and Python </p>

## :rocket: About the project 

This project uses the **Selenium** library to perform web scraping on a video card page from the Kabum website. The script collects information about video cards, including image, name, and price, create and send to MySQL.

## :thinking:  Why?

Just practice my skills.

## :warning: Prerequisites

Before running the script, you need to have the following installed:

- [Python](https://www.python.org/downloads/)
- [Selenium](https://pypi.org/project/selenium/)
- [ChromeDriver](https://developer.chrome.com/docs/chromedriver/downloads) (make sure the version of ChromeDriver matches your Chrome browser version)
- [MySQL](https://dev.mysql.com/downloads/)

## Code Description

- **URL**: The script accesses the URL https://www.kabum.com.br/hardware/placa-de-video-vga.
- **Selenium Configuration**: The Chrome browser is set up to run in headless mode.
- **Data Extraction**: The script collects the image `src`, name, and price of up to 20 products and saves this information in a CSV file named `Placas_Kabum.csv`.
- **Error Handling**: If the information cannot be extracted, the script prints an error message.
- **Database Insertion**:
  - Constructs and executes an SQL `INSERT` command to store the extracted data in the `produtos2` table of the `bdplacas` database.
  - Commits the transaction with `conexao.commit()`.
- **Close Resources**: 
   - Closes the database cursor and connection with `cursor.close()` and `conexao.close()`.

