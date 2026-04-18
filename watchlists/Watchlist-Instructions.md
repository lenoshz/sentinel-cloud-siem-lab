# GeoIP Watchlist Information

For this lab, a customized geographic IP routing dataset (`geoip-summarized.csv`) containing over 54,000 subnets was utilized. 

Due to file size constraints, the full database is not hosted in this repository. 

**Implementation Details:**
1. The CSV was imported into Microsoft Sentinel via **Configuration -> Watchlists**.
2. The `SearchKey` was mapped to the `network` column.
3. Sentinel utilizes this underlying dataset via the `_GetWatchlist("geoip")` function to enrich raw IP addresses with Latitude, Longitude, City, and Country metrics for the Workbook visualization.
