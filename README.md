<img src="https://img.shields.io/github/issues/WikiMovimentoBrasil/brazilian_laws?style=for-the-badge"/> <img src="https://img.shields.io/github/license/WikiMovimentoBrasil/brazilian_laws?style=for-the-badge"/> <img src="https://img.shields.io/github/languages/top/WikiMovimentoBrasil/brazilian_laws?style=for-the-badge"/>
# Brazilian Laws

This project contains a set of Jupyter Notebooks used to scrape data in Brazilian laws contained on LexML and Palácio do Planalto's websites. Parts of these scripts were used as a base for the project https://github.com/WikiMovimentoBrasil/brazilianlaws, which resulted in the creation of a tool in Toolforge, http://brazilianlaws.toolforge.org. 

More information on the WikiProject Brazilian Laws can be found at: https://www.wikidata.org/wiki/Wikidata:WikiProject_Brazilian_Laws

## Installation

There are several packages needed for to this application to function. All of them are listed in the <code>requeriments.txt</code> file. To install them, use

```bash
pip install -r requirements.txt
```

## Scripts
A thorough explanation on each of the scripts can be found on: https://www.wikidata.org/wiki/Wikidata:WikiProject_Brazilian_Laws/Scripts#LexML_API_scraper

### lexml_scraper
This scraper extracts the information retrieved from the LexML API and writes it on a <code>.txt</code> file separated by \*. It is also possible to generate a lexicon file, containing all the main subject (P921) listed under each legislation item, and how frequently they've are used as keyword. 

### legislacao_scraper
This script visits the presidency's website and parses it, page by page, scraping the links to the record page and full text page of each law and decree-law listed on it. A few manual steps are required. After running the first two blocks of code, 

1. Click on "Pesquisa Avançada" (Advanced Search);
2. Pick the options to filter the legislations you are interested in. Currently, on the Palácio do Planalto website, you can query them by their type, current status, date, President in Office, person who signed it, it's Referenda Ministerial, where it originated from and which official publication it was published in;
3. Click on "Pesquisar" (Search);
4. The content of the page will be loaded, showing the legislation from the most recent to the oldest, 10 per page.

Then run the third and final block to scrape the website's content. 


### presidencia_scraper
This script opens a <code>.txt</code> file generated by <code>legislacao_scrapper</code>, visits the URLs listed on it one by one, scrapes its content and saves the output to <code>saida.txt</code>. 


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.


## License
[GNU General Public License v3.0](https://github.com/WikiMovimentoBrasil/wikimotivos/blob/master/LICENSE)


## Credits
This application was developed by the Wiki Movimento Brasil User Group, supported by WikiCite.