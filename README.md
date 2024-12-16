# GitHub Topics Scraper

## Project Overview
This project involves web scraping GitHub's [topics page](https://github.com/topics) to extract valuable information about various topics and their repositories. The data is structured and saved into CSV files for further analysis. This project showcases the use of web scraping techniques using Beautiful Soup and Python's data handling capabilities.

---

## Project Outline

### Objectives
1. Scrape the [GitHub Topics Page](https://github.com/topics) to get:
   - Topic Title
   - Topic Page URL
   - Topic Description
2. For each topic, scrape its page to extract the top 25 repositories, including:
   - Repository Name
   - Username
   - Stars
   - Repository URL
3. Save the extracted data for each topic in a structured CSV file in the following format:

| Repo Name         | Username    | Stars     | Repo URL              |
|-------------------|-------------|-----------|-----------------------|
| Repo_1_Name       | User_1      | 5000      | https://github.com/...|
| Repo_2_Name       | User_2      | 3000      | https://github.com/...|

4. Organize the CSV files into a dedicated folder.

---

## Technologies Used

- **Programming Language:** Python
- **Libraries:**
  - Beautiful Soup (for web scraping)
  - Requests (to fetch web pages)
  - OS (to handle file and folder creation)
  - Pandas (for data handling and saving to CSV)

---

## Steps and Implementation

### 1. Fetch and Parse Topics Page
- **Scrape the GitHub Topics Page**:
  Use `requests` to fetch the HTML content of the topics page.
- **Parse HTML with Beautiful Soup**:
  Extract topic titles, URLs, and descriptions using CSS selectors.

### 2. Navigate to Topic Pages
- **Iterate through each topic**:
  Visit each topic's URL to extract details about repositories.

### 3. Extract Repository Information
- **Scrape top 25 repositories**:
  - Repo Name
  - Username
  - Star Count (converted to an integer format)
  - Repo URL
- **Handle data consistency and cleaning**:
  Ensure all extracted data is structured and complete.

### 4. Save Data to CSV Files
- **Create a dedicated folder**:
  Use the `os` library to organize CSV files for each topic.
- **Save data**:
  Write the repository information into CSV files using Pandas.

### 5. Error Handling and Optimization
- Handle cases where pages may fail to load or have missing data.
- Use logging to track the progress and debug issues.

---

## Folder Structure

```
github-topics-scraper/
│
├── data/
│   ├── topic_1.csv
│   ├── topic_2.csv
│   └── ...
│
├── scripts/
│   └── scraper.py
│
├── requirements.txt
└── README.md
```

---

## How to Run

1. **Clone this Repository**:
   ```bash
   git clone https://github.com/yourusername/github-topics-scraper.git
   cd github-topics-scraper
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Scraper**:
   ```bash
   python scripts/scraper.py
   ```

4. **View Output**:
   - CSV files for each topic will be saved in the `data/` folder.

---

## Future Enhancements
- Scrape additional details about repositories, such as:
  - Number of forks
  - Programming language
- Add a GUI interface for easier interaction.
- Implement parallel processing to speed up scraping.
- Export data to additional formats (e.g., JSON, Excel).

Feel free to explore, modify, and contribute to this project!
