<div id="top"></div>

<h3 align="center">LinkedIn Username Harvester</h3>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#options">Options</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

The goal of this script was to replace [CrossLinked](https://github.com/m8sec/CrossLinked) as a tool for scraping employee names from LinkedIn. CrossLinked can currently only pull 300ish names as a result of Google/Bing's search result limits. The hope was that with Google's API and some creative work with the searches (such as appending random characters to the search critera), more than 300 names would have been able to be found. However, that was not the case.

While this script technically works, there is no reason to use it. CrossLinked should be used instead. This is only being uploaded as a code example or as a backup (since CrossLinked does not use Google's API, it could break if Google decides to crack down even more on search result scraping).

![Script Screenshot](https://github.com/LukeLauterbach/LinkedIn-Username-Harvester/blob/main/Images/ExampleImage.jpg)

### Built With

* [Python](https://www.python.org/)
* [Google Programmable Search Engine](https://programmablesearchengine.google.com/about/)


<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

This script relies on Google's Programmable Search Engine, which will require a short setup in order to get an ID and API key. After initial setup is complete, running the script is a simple command.

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/LukeLauterbach/LinkedIn-Username-Harvester.git
   ```
2. Get a free [Google Programmable Search Engine ID](https://programmablesearchengine.google.com/about/)
3. Enter your ID in `GoogleDorking.py`
   ```py
   searchEngineID = "INSERT_ID_HERE"
   ```
4. Get a free [Google Custom Search API key](https://developers.google.com/custom-search/v1/introduction). Note: Free keys can only run 100 searches per day. A paid account can be set up to run more than 100 searches per day. Multiple free API keys could also be generated and inserted into this list, which the script would then iterate through.
5. Enter your API key in `GoogleDorking.py`
   ```py
   keyList = ["INSERT_KEY_HERE", "INSERT_ADDITIONAL_KEY_HERE"]
   ```

<p align="right">(<a href="#top">back to top</a>)</p>

## Usage

```shell
python3 LinkedInHarvester.py [OPTIONAL OPTIONS] [Company Name]
```

A company name is the only required arugment. If the company name contains a space, the name should be encompassed in quotations.

<p align="right">(<a href="#top">back to top</a>)</p>

## Options
Options | Description
-|-
-c | Specify a company name
-m | Max Results (limit the number of names gathered)
-q | Quiet Mode (only outputs names)
-v | Verbose Mode (outputs Google APAI key alerts)
-vv | Extra Verbose Mode (outputs errors)
-db | Debug Mode (only runs one search)

<p align="right">(<a href="#top">back to top</a>)</p>
