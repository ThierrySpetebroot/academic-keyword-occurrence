# Historic word occurrence in academic papers

## Summary

This script extracts the historic word occurrence of a search term in
academic papers (from Google Scholar). It allows for spotting trends
in research and analyzing the relevance of a topic over time.

## Usage

`python extract_occurrences.py '<keyword>' <start date> <end date>`

This command lists the number of publications for every year using
this keyword. The script just searches for articles and excludes
patents and citations.

## Example

- Search term: 'bitcoin'
- Desired time span: 2000 to 2015
- Command: `python term_frequency.py 'bitcoin' 2000 2015`
- Output: `out.csv`, with the following contents:

| year | results |
|------|---------
| ...  |    ...  |	|
| 2011 |    141  |
| 2012 |    292  |
| 2013 |    889  |
| 2014 |    2370 |
| 2015 |    2580 |


![bitcoin chart](https://raw.githubusercontent.com/Pold87/academic-keyword-occurrence/master/bitcoin_chart.png "bitcoin chart")

## Troubleshooting
_OSX only_: Python 3.6 does not include any SSL certificates, therefore `https`
request will fail due to the impossibility to verify the URL.

This will lead to the following error:

```
urllib.error.URLError: <urlopen error [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed
```

_Fix_: Execute `/Applications/Python\ 3.6/Install\ Certificates.command` to
install the `certifi` package. (More details: https://stackoverflow.com/a/42334357)

## Credits
Created by Volker Strobel - volker.strobel87@gmail.com

Modifications for Python 3 version made by Patrick Hofmann
