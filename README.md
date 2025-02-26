# Spotify Top Songs & Artists
A data analysis project based on an open-source dataset of Spotify's Top 50 Songs across different countries.
## Overview
This project made use of various data analysis steps such as data gathering, data exploration, data cleaning and manipulation, and data visualization. The Jupyter notebook file, as well as the Power BI PBIX file are all provided within this repository. I didn't get the chance to include the cleaned dataset since it's too large for GitHub, and the shareable link to the dashboard since the free version of Power BI Desktop has no means of sharing dashboards online as far as I know.
## Tools
This analysis made use of Python with the Pandas library for data exploration and data cleaning; since the dataset used is too large for Excel to handle, and Power BI for data visualization and some dataset modification, such as adding calculated columns.
## Objectives
This analysis aims to determine the following:
* Which artists and songs garnered the most popularity?
* Which artists and songs were the most popular across different countries?
* How do the ranks of artists and their songs change overtime?
## Dashboard
The final dashboard looks something like this:
![image](https://github.com/user-attachments/assets/7bc61ab6-bf65-4598-9158-545fd01b4733)
It contains a display of how many entries are in the dataset, bar charts to display the most popular artists and songs, a line graph to show the trends on the changes in artist and song rankings over time, and a couple of filters to filter countries and year.
## Findings
After plotting the data into charts using Power BI, the following answers were found:
### Artist and song popularity
![image](https://github.com/user-attachments/assets/225a0c6a-1849-4a1a-b2f8-e857a428f371) <br>
According to our data, the collaboration between Bruno Mars and Lady Gaga garnered the highest average popularity score of 98.58, followed by Mitski, iñigo quintero, Jack Harlow, and the collaboration among artists ¥$, Kanye West, Ty Dolla $ign, Rich The Kid, and Playboi Carti. <br><br>
![image](https://github.com/user-attachments/assets/ad0f3516-f984-4237-9ec1-2c9e1076841e) <br>
As for the songs, the most popular song was from our most popular artists, titled Die With A Smile, with the same average popularity score of 98.58. This is closely followed by GREEDY by Tate McRae, BIRDS OF A FEATHER by Billie Eilish, Cruel Summer by Taylor Swift, and My Love Mine All Mine by Mitski.
### Artist and song popularity by country
To find the answers to this, we can apply our country filters on the upper-right portion of our dashboard to see which artist and songs are popular in a specific country. 

For example, this is what our charts would look like if we were to see which artists and songs are popular in the Philippines according to our data:
![image](https://github.com/user-attachments/assets/cb83ef8d-b4ff-4d7d-a0b4-7cb828e4c544)
### Artist and songs trend
For this, we can simply select an artist or a song from our bar charts to filter our line chart. 

For example, for the song Die With A Smile, this is what its daily ranking looked like throughout the years:
![image](https://github.com/user-attachments/assets/b9b34bed-1ad5-4ef2-8766-2001cd0d13ee) <br>
Interpreting this line chart, we can see that it steadily rose to the number one spot around September of 2024 and never really left the top 10 ever since.

As for artists, if we select an artist as a filter instead, we can see the graph of all their songs and their rankings in the line chart. Here's what Billie Eilish's songs looked like in our chart:
![image](https://github.com/user-attachments/assets/352d0af9-f63d-4d4e-b65f-3f19c7de878d)
## Possible Improvements
While performing data exploration and analysis on this dataset, I noticed a couple of gaps from the dataset.
1. **Some data are missing from certain songs.** Although they were only composed of a miniscule percentage of the data (I only found 27 rows with missing song information), it would still be nice to be able to see how their stats would compare to the rest of our data. A possible solution to this would be to use Spotify's API to scrape information regarding these songs since the Song ID was provided in the dataset. But this is outside the scope for this analysis. <br>
2. Other notable lack of data is from the *countries* and *album name* columns. I opted to just mark these as 'Unknown'. As well as some blanks in the *album release date* column. However for this specific column, I intentionally left them blank so that the data type wouldn't be affected. Better approaches could of course be applied here such as data imputation using predictive algorithms to infer what these missing data would possibly look like. This would eliminate any blanks from our data which may (or may not) help with the accuracy of the analysis. <br>
3. I decided to not include columns which contain various metadata about a song properties such as acousticness, danceability, time signature, tempo, etc. However, these properties could be used to further investigate how the tonal qualities of music may influence their popularity, or other metrics like that.
# Credits
Credit goes to [this Kaggle repository](https://www.kaggle.com/datasets/anandshaw2001/top-spotify-songs-in-73-countries) for providing the original dataset utilized in this project.
