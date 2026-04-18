# SPICE ROADS: 
# Analyzing Global Chili Trade Data and Influential Diaspora Cuisines
Team: Anwen, Edson, Mykyta

Overview: The Spice Roads Project investigates the correlation between shifting diaspora populations in Europe (we chose DE, UK, and PL as examples), and the corresponding shifts in chili imports, using mainly the UN Comtrade trade database. We can see that as global populations migrate, they influence local cuisines, consumer tastes and product availability.

Central research hypothesis: Changes in specific immigrant demographics directly influence the volume and type of chili products (fresh, dried, preserved, sauces) imported into European nations.


# Demographic Mapping & Culinary Correlation
    Goal: Merge Comtrade API import data with demographic population estimates
    Methodology: Isolate the top diaspora groups in DE, UK, and PL. Map these populations to popular chili products (eg. Germany: Turkish diaspora --> Aleppo Pulbiber/Crushed Chili)
    Further Visualisation: Create Country Profile Cards, to visualize how a country's immigrant makeup influences its culinary spice and hotness preferences

# Data Collection & Comtrade API Aggregation
    Goal: Extract targeted chili pepper import data for Germany (276), UK (826) and Poland (616)
    Methodology: Query UN Comtrade API for years 2020-2025 using specific HS codes covering fresh capsicum, dried/crushed chili, hot sauces, and preserves

# Further Research & Future Scope
Due to time limitations, we outlined the following  high-potential features for future development:

1. Dynamic Census API Integration
Current State: Diaspora population sizes are based on aggregated estimations and manual extracts from destatis, ONS, and GUS.
Future Goal: Build automated pipelines querying the official national census APIs to dynamically update immigrant and foreign-national population shifts annualy.

2. A "Global Heat Map" & Pungency Indexing
Current State: Import volumes are analyzed purely by weight and monetary value.
Future Goal: Codify a "Spiciness Index" algorithm by mapping HS codes to their dominant chili varieties and applying a Scoville heat multiplier. 
The theoretical equation for calculating a country's total "imported" heat index:

        ## Heat_Index = i = ∑n ​(Vi ​× Si​)
(Where Vi​ is the volume of import category i, and Si​ is the average Scoville rating of the dominant pepper in that category).

3. Extended Chili Varieties Lexicon

Current State: We have mapped the most popular varieties by trade volume corresponding to our target diasporas.
Future Goal: Complete the database of 3000+ botanically classified Capsicum varieties, plus standard HS codifications. 
Below is a snapshot of our targeted lexicon structure:

Variety	    Species	    Scoville (Avg)	    Typical HS Match	Key Diaspora / Cuisine

Jalapeno	C. annuum	5,000	            200190 (Preserved)	Latin American / Tex-Mex
Habanero	C. chinense	250,000	            070960 (Fresh)	Caribbean / West African
Pulbiber	C. annuum	10,000	            090422 (Crushed)	Turkish / Middle Eastern
Piri Piri	C. frut.	100,000	            210390 (Sauces)	Lusophone African / Portuguese
Bhut J.     	C. chinense	1,000,000	    090422 (Crushed)	Indian / South Asian


# Repo Structure:

    notebooks/
        README
        Comtrade API querying and dataset cleaning notebook for HS codes (070960, 090421, etc.) 
        Demographic data collection and analysis of population shifts and import trends
    data/ 
        CSV outputs and datasets
    charts/
        Chili Variety profile cards and and Dominant Diaspora mapping

