# 101 Artists Top 10 Songs Compared to Billboard Appearances
This project compares the top 10 songs of 101 artists from Spotify to their respective appearances on the Billboard charts based on release dates. The data integrates Spotify API data, Billboard chart data, and Amazon RDS for storage and analysis.

## Project Description
This project analyzes the relationship between Spotify's top tracks for artists and their Billboard Hot 100 chart performance. By merging data from Spotify and Billboard, the analysis explores trends in:

- Popularity and follower metrics for artists.
- Song performance on Billboard charts (e.g., peak position, weeks on chart).
- Genre distribution and its correlation with chart success.

## Data Sources
- Spotify API: Extracted artist information, top tracks, and metadata such as genres, release dates, and popularity.
- Billboard API: Fetched Hot 100 chart data to track performance metrics like peak position, weeks on chart, and ranking changes.
- Amazon RDS Database: Managed database instance for storing processed data.

## Technologies Used
- Programming Languages: Python
- Libraries:
  - Data processing: pandas, numpy
  - Spotify API: spotipy
  - Billboard API: billboard.py
  - Visualization: matplotlib, seaborn
- Database: Amazon RDS with MySQL
- Cloud Service: AWS for scalable and reliable database hosting.

## Data Pipeline
1. Spotify Data Extraction:
  - Retrieved artist metadata and top 10 songs for 101 artists using Spotify's API.
2. Billboard Data Extraction:
  - Queried Billboard charts to match songs based on release date, title, and artist.
3. Data Storage:
  - Stored processed data in Amazon RDS MySQL tables (artist_top_songs, billboard_songs_db, combined_db).
4. Data Cleaning:
  - Filtered out duplicates and ensured valid release date formats.
5. Analysis and Visualizations:
  - Merged Spotify and Billboard data to create comparative insights and visual trends.

## Setup Instructions
### Prerequisites:
- Install Python and configure Amazon RDS database.
- Obtain API keys for Spotify and Billboard.
- Configure an AWS account for database hosting.

### Steps
1. Amazon RDS Setup:
    - Create an Amazon RDS instance.
    - Configure security groups to allow external access.
2. Mount Google Drive (for Colab):
   ```python
    from google.colab import drive
    drive.mount('/content/mnt')
3. Install Dependencies:
   ```python
    pip install spotipy billboard.py mysql-connector-python
4. Set Up Spotify API:
    - Configure SpotifyClientCredentials with your API credentials.
5. Connect to Amazon RDS:
    - Replace database connection parameters (mysql_address, mysql_username, etc.) with your Amazon RDS credentials.
6. Run the Scripts:
    - Execute each section to extract, clean, and store data.


