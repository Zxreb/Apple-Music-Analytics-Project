# Apple-Music-Analytics-Project
End-to-end data analytics project using Google Cloud SQL and PostgreSQL to analyze over 10,000 Apple Music tracks. Includes SQL queries for insights on pricing, genres, artists, and release trends. Future work integrates Tableau and Power BI dashboards for interactive data visualization and reporting.

This project analyzes **10,000+ Apple Music tracks** using **Google Cloud SQL (PostgreSQL)** and **Google Cloud Storage**.  
It explores pricing, genre trends, release patterns, and artist statistics using advanced SQL queries.  
Future phases will include **Tableau** and **Power BI dashboards** for visual analytics.

Dataset: https://www.kaggle.com/datasets/kanchana1990/apple-music-dataset-10000-tracks-uncovered

---

## Tech Stack
- Google Cloud SQL (PostgreSQL)
- Google Cloud Storage
- SQL (Data Cleaning + Analytics)
- Tableau and Power BI for visualization

## Key SQL Analysis
1 Table Creation
The dataset was first structured in SQL by creating the apple_music_tracks table, defining each column with appropriate data types for artist, track, genre, price, and other metadata. This provided a clean schema for efficient querying and ensured that all 22 attributes — including identifiers, pricing, release date, and explicitness — were standardized before analysis. By using CREATE TABLE IF NOT EXISTS, the process maintained data integrity and prevented duplication when re-executing the import.

2️ Top 10 Genres by Song Count
This query grouped all records by primaryGenreName to determine which musical categories contained the most tracks. Results revealed that Pop, Country, and Rock dominate Apple Music’s catalog, highlighting their enduring popularity across user demographics. The high representation of mainstream genres indicates that Apple’s library is heavily driven by globally commercial music, aligning with listening trends seen in major streaming platforms.

3️ Average Track Price by Genre
This query calculated the average track price across all genres by converting text values to numeric types for price aggregation. The results showed that genres like Jazz, Classical, and Soundtrack tend to have higher average prices, reflecting niche demand and longer track durations. Conversely, popular genres such as Pop and Hip-Hop are priced lower on average, suggesting a volume-driven pricing model rather than exclusivity.

4️ Most Common Artists
Grouping the data by artistName revealed the artists with the largest number of available tracks. The analysis showed that prolific creators such as Taylor Swift, One Direction, and Michael Jackson occupy the top spots, indicating both high productivity and sustained popularity across multiple albums. This also validated the data’s representativeness by surfacing globally recognized names.

5️ Average Collection Price by Artist
This query focused on collectionPrice, averaging album-level costs per artist. It provided insight into pricing strategies for complete albums rather than individual songs. Artists with deluxe editions or compilation albums, such as The Beatles or Ed Sheeran, displayed higher average collection prices. The variation in results underscores how legacy and content volume influence pricing on streaming platforms.

6️ Yearly Song Release Distribution
By extracting years from releaseDate, this query tracked music production trends over time. Results showed a steady increase in song releases after 2010, reflecting both digital distribution’s growth and the rise of independent publishing. The trend visualized the industry’s technological evolution, with notable spikes corresponding to years of high streaming adoption.

7️ Explicit vs. Non-Explicit Content
This comparison of trackExplicitness counts revealed that the majority of tracks in the dataset were non-explicit, though explicit songs formed a substantial minority. Genres like Hip-Hop and R&B contributed disproportionately to explicit content, suggesting cultural and lyrical patterns specific to those styles. This analysis provided useful groundwork for understanding content labeling across genres.

8️ Average Track Duration by Genre
This query converted trackTimeMillis into minutes to determine which genres feature the longest songs. Classical and Jazz tracks ranked highest, consistent with their complex compositions and extended instrumental sections. In contrast, Pop and Electronic music maintained shorter durations tailored to commercial radio and streaming optimization.

9️ Top 5 Most Expensive Tracks by Artist
By sorting trackPrice values in descending order, this query identified the costliest individual songs on the platform. The results revealed premium-priced singles from legacy or limited-release artists, offering insight into how rarity and copyright factors influence pricing. This highlighted how certain catalog items maintain exclusivity within Apple Music’s ecosystem.

10️ Most Popular Genre by Year
Combining year extraction with genre grouping, this query identified the dominant genre for each release year. Pop maintained consistent leadership across the years, but genre diversity increased post-2015, showing the growing presence of Hip-Hop, Alternative, and EDM. This temporal view captured how audience preferences shifted alongside industry trends.

11️ Artist with Most Explicit Songs
Filtering for tracks labeled as explicit, this query ranked artists by explicit song count. The results confirmed Hip-Hop artists’ prominence in explicit content, while mainstream Pop artists had fewer such tracks. This finding aligns with lyrical and thematic conventions of these genres, offering cultural insight into musical expression.

12️ Price Differential by Explicitness
By calculating average prices separately for explicit and non-explicit songs, the analysis found minimal price differences between the two categories. This suggests that explicitness does not strongly influence pricing — Apple Music maintains consistent pricing structures regardless of lyrical content.

13️ Highest-Priced Genres
Using median pricing via PERCENTILE_CONT, this query avoided outlier bias to identify genres with the most expensive tracks. Classical and Jazz again topped the list, emphasizing that these genres retain higher average costs due to production complexity, artist reputation, and lower distribution volume.

14️ Longest Tracks by Artist
Averaging track durations for artists with multiple releases, this query identified creators known for long-form compositions. Artists specializing in Progressive Rock, Classical, or Ambient music ranked highest, reinforcing duration trends discovered at the genre level. This analysis also filtered out anomalies by requiring multiple tracks per artist.

15️ Distribution of Track Counts per Album
This aggregation examined how many songs typically appear on an album by counting frequency of trackCount values. The results showed most albums contain between 10–15 tracks, aligning with industry standards for commercial releases. This distribution offers a structural benchmark for future trend analysis.

16️ Average Album Price vs. Track Count
By comparing the average collection price against the number of tracks per album, this query explored economies of scale in pricing. Albums with more tracks exhibited a decreasing cost per song, suggesting bundle pricing strategies that incentivize full-album purchases.

17️ Yearly Average Track Duration
Aggregating average song lengths by release year revealed gradual changes in musical structure. Tracks from the 1980s and 1990s tended to be longer, while modern releases average under four minutes. This supports recent research on shrinking song lengths due to streaming optimization and audience attention spans.

18️ Genre Share by Explicitness
This query quantified the percentage of explicit tracks within each genre. Hip-Hop/Rap showed the highest explicit content ratio, followed by R&B and Alternative, while genres like Classical and Country remained nearly 0%. These insights reflect broader sociocultural influences on lyrical themes and audience targeting.

19️ Genre vs. Average Album Size
The final query measured trackCount averages per genre, showing that Rock and Classical albums typically include more songs than other genres. This finding reinforces earlier observations on album length and complexity, connecting musical structure to commercial format differences.
## Visualization Roadmap

## Insights Uncovered
