# NSS capstone: Trends in Children's Literature  
  
One day, reminiscing with friends about our favorite childhood book series, we became curious – which of our favorites from the 90s and early 2000s are still popular among kids?  Which ones were just a fad?  What new series will Generations Z and Alpha be nostalgic for?  
  
Using data from the Seattle Public Library (SPL), I intend to analyze trends in children's literature from 2006 – 2025 to determine which titles and series have had staying power over the last 20 years, and which had only brief moments in the spotlight.  
  

## Data Questions  
- Which books have been the most popular children's titles during the covered time period?
- Which titles had moments of popularity that they did not retain?
- Which titles have been consistently popular?
- Do "classics" remain popular, or do young readers favor new releases?  
  
  
## Discoveries  
Young readers in the twenty-first century overwhelmingly prefer books written and published for their generation, not their older siblings or parents.  While the Harry Potter series has a strong presence in the most popular children's books at the library, series like Jeff Kinney's *Diary of a Wimpy Kid* have more checkouts in a typical month, and the list of most popular books each year experiences regular turnover instead of frequently featuring the same titles.  
  
  
## Data  
Data was sourced from the [Checkouts by Title](https://data.seattle.gov/Community-and-Culture/Checkouts-by-Title/tmmm-ytt6/about_data) dataset available from SPL at data.seattle.gov  
  
  
## Tools  
Data was imported, cleaned, analysed, and visualized using Python in Jupyter notebooks.  
  
  
## Challenges  
The biggest challenges for this project involved different types of data cleanliness.  
1. **Narrowing the data set**: I filtered for terms similar to 'juvenile fiction' or 'juvenile non-fiction' to identify and extract children's literature, but (a) I can't guarantee that all children's titles were correctly and consistently tagged in the first place, and (b) these tags were used for a variety of types of items, from picture books to some young adult titles, which may experience distinct behaviors but were not distinctly identified within this data set.  
2. **What's in a name?**: Some books are listed under many different "titles" in the original data set, as the title string may include format information ("Large Print Edition" or "Unabridged") or identify which series a title belongs to, and those choices may have changed over time, or with different formats of the same book.  In order to count the total number of checkouts for a given book, I cleaned these extra phrases out of book titles as much as possible.  I added cleaning steps to account for consistent patterns I noticed, but it's very likely I missed cases given the size of the data set.  My cleaning also did *not* provide a way to merge different-language versions of the same book.
  

## Future exploration
This data could also be used to explore questions such as:
* Which *authors* are the most popular overall?  Most consistently popular?  
  * What about when normalized for their number of publications?
* How does the analysis change when normalized for the number of copies of each title available in SPL's catalog?
* How does releasing a new book impact the popularity of an author's other titles?
* How does winning an award impact a book's popularity?