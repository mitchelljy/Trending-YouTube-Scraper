# Trending YouTube Video Scraper

Originally used to build [this dataset](https://www.kaggle.com/datasnaek/youtube-new) on Kaggle, which has about 6 months worth of trending YouTube videos on it. This script will scrape the most relevant information from videos that are currently trending on YouTube in a specified set of countries. You can find example output files in the output directory.

Trending YouTube videos for whatever country you are in currently can be found [here](https://www.youtube.com/feed/trending).

## Prerequisites

### API Key

In order to use this script, you will need a valid API key for the YouTube Data API. It is free and the instructions for doing so are [here](https://developers.google.com/youtube/registering_an_application). It is slightly awkward to get a key, but if you follow the instructions you should be ok.

Once you have the key, put it inside a text file named `api_key.txt` in the same directory as the script, or if it's not in the same directory you can target it with the `--key_path` parameter.

### Modules

The only module needed that is not in the standard library is the `requests` module.

### Country Codes

In order to run, the script needs country codes for the countries to collect trending videos from. These are 2 letter country abbreviations according to ISO 3166-1. A list of all existing ones can be found [here](https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes), however not all of these are assured to work with the YouTube API. This project comes with a list of 10 inside the `country_codes.txt` file.

## Running the Script

The script is fairly simple to run, it takes the following optional parameters:

* `--key_path` which takes a path argument that targets the text file containing your API key. By default this is `api_key.txt` in the current directory.
* `--country_code_path` which takes a path argument that targets the text file containing the list of country codes to target. By default this is `country_codes.txt` in the current directory.
* `--output_dir` which takes a path argument that specifies the folder to create the output CSV files for each country. By default this is `output/` in the current directory.

## License

This project is licensed under the BSD 2-Clause License - see the LICENSE.md file for details
