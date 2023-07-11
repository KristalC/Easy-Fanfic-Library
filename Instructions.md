# Introduction

The Easy Fanfic Library project enables users to easily download works from AO3 and other fanfiction sites into a library in Calibre, a free e-book management application, with all the metadata (title, author, series, ratings, warnings, characters, relationships, additional tags, date posted, etc.) intact and in separate fields. This way you will be able to quickly download fanfiction and sort/filter downloaded works similarly to how you would filter on AO3 itself (including by your personal bookmark data and tags). This will work with fanfiction sites besides AO3, but the project was designed for AO3 works, and is optimized for the organization of AO3 works.

The objective of this project is an easy setup process for a fanfiction library on your computer. To set up a working fanfiction library, only four steps are required. If you wish to include your bookmark information in the metadata for AO3 works, just two more steps are needed. Any additional steps are optional and mainly involve personalizing how the library is displayed.

Calibre is a comprehensive free and open source e-book library management application which lets you organize your e-books by different metadata (such as title, author, series, and tags) within an e-book library. It comes with its own e-book viewer that can view most major e-book formats (such as EPUB), but you can also open files in another viewer if desired. It can connect to most e-book reading devices, tablets, and smartphones, so you can transfer your e-books to your mobile devices or set up the ability to view your libraries from a mobile browser. For more information on Calibre, see <https://calibre-ebook.com/>.

The Easy Fanfic Library is a sample Calibre library that users can download and import into the Calibre application on their own computer.

* The sample library has the Calibre plugin FanFicFare pre-installed. FanFicFare (<https://github.com/JimmXinu/FanFicFare/wiki/CalibrePlugin>) is what enables you to download fanfiction and metadata directly into Calibre (from URLs). The sample library pre-configures FanFicFare to send fanfiction metadata to the appropriate columns/fields.
* The sample library has the Calibre plugin EpubMerge pre-installed. EpubMerge (<https://www.mobileread.com/forums/showthread.php?t=169744>) interfaces with the FanFicFare plugin and adds the option of downloading a group or series of works as a single EPUB anthology.

These instructions may seem overly specific to some, but they are designed to be easy to follow, even if you have no prior experience with the Calibre software and have never seen computer code in your life.

# Contact and Credits

If you wish to ask questions or leave feedback about the Easy Fanfic Library, you may fill out the feedback form (<https://forms.gle/h2KXYeDXaDDvsSky5>).

Easy Fanfic Library was created by Kristal C. (Dreamwidth: <https://thebiballerina.dreamwidth.org/>, Mastodon: <https://fandom.ink/@thebiballerina>, Tumblr: <https://thebiballerina.tumblr.com/>)

Calibre e-book manager software was developed by Kovid Goyal. Some of its contributors are listed at: <https://calibre-ebook.com/about#contributors>.

FanFicFare was developed by Jim Miller (AKA JimmXinu). For more information, see the GitHub repository <https://github.com/JimmXinu/FanFicFare> or the plugin forum <http://www.mobileread.com/forums/showthread.php?t=259221>.

EpubMerge was also developed by Jim Miller. For more information, see the GitHub repository <https://github.com/JimmXinu/EpubMerge> or the plugin forum <https://www.mobileread.com/forums/showthread.php?t=169744>.

# What The Sample Library Actually Does

This project makes use of existing tools (the Calibre application, FanFicFare plugin, and EpubMerge plugin). This section will explain what alterations the sample library makes to the default configurations of these tools.

## What the Sample Library Adds to Calibre

* custom columns/fields corresponding to fanfiction metadata fields (including every metadata field available on AO3 works)
* FanFicFare plugin, with customized general and AO3-specific settings (mainly with regards to which metadata goes to which columns)
  * customized general settings in the FanFicFare configuration menu
    * Most fanfiction metadata will be sent to the appropriate columns/fields with these settings.
  * customized AO3 settings in the FanFicFare personal.ini file
    * Every type of metadata included in AO3 works is pre-configured to be sent to the correct columns/fields in Calibre.
    * See **"FanFicFare Configuration personal.ini Additions"** and the [personal.ini settings.txt](https://github.com/KristalC/Easy-Fanfic-Library/blob/main/personal.ini%20settings.txt) file.
    * In the FanFicFare configuration personal.ini file, any code added by the Easy Fanfic Library project will be marked as "Easy Fanfic Library code". Any of the comments added by the Easy Fanfic Library project will be marked as “Easy Fanfic Library notes" or placed within "Easy Fanfic Library code". The remaining code comes from the FanFicFare plugin-defaults.ini file and its copyright belongs to FanFicFare contributors.
* EpubMerge plugin, which will automatically add anthology options to FanFicFare

## Columns/Fields in the Sample Library

* Calibre default columns/fields include:
  * title
  * authors
  * series
  * languages
  * publisher - site which the fanfiction was retrieved from
  * file size
  * last modified date
  * comments - this is where the work summary will be added
  * tags - Calibre's default tags section is hidden in the tag browser and book details, as it is redundant (it will get characters, relationships, and additional tags)
* Custom columns/fields for general fanfiction metadata include:
  * fandom
  * maturity rating
  * warnings
  * relationships
  * characters
  * additional tags
  * word count
  * current chapter number
  * status
  * date updated
  * date posted
  * genre - this section is set to include a "FanFiction" tag for works downloaded from fanfiction sites with FanFicFare
    * This could help you organize if you intend to include non-fanfiction works in your fanfiction library.
  * my tags - this section is not automatically populated with FanFicFare, but rather is intended for the user to add any of their own tags
* Custom columns/fields specifically for AO3 works include:
  * category
  * total chapter count
  * comment count
  * bookmark count
  * hit count, collections
  * additional series
  * restricted - whether the work is restricted to logged in users
  * bookmark status - whether you have bookmarked the work
  * private bookmark - whether your bookmark (if applicable) is private
  * bookmark rec - whether your bookmark (if applicable) is a rec
  * bookmark tags - (if applicable)
  * bookmark summary - (if applicable)

# Setup Instructions

1. Download the [sample library data file](part-0001.calibre-data?fileId=18701266).
2. Download Calibre from <https://calibre-ebook.com/download>, if you do not have it downloaded already. If you need any additional guidance on using Calibre, see the official help website at <https://calibre-ebook.com/help>.
3. Import the sample library into Calibre.
   * You may be offered this option automatically when you open Calibre the first time.
   * Alternatively, once you are in the Calibre program, you can select the library drop-down menu, "Export/import all calibre data", "Import previously selected data", and then choose the library data file you downloaded.
   * If you already have data in Calibre, it would be a good idea to export your Calibre data before importing the sample library template as a new library, as some users have reported that importing the new library erased their pre-existing Calibre configurations. 
4. (Optional) Personalize the columns in Calibre.
   * To personalize which columns are displayed, the order in which the columns are displayed, and to add any additional columns of your own, you may select the "Preferences" drop-down menu, then "Change calibre behavior", and then "Add your own columns". This will open the columns menu.
   * You can add additional series columns, if desired. The default settings will record series data from up to four series for any work on AO3. If you wish to record additional series data on works which are included in more than four series, you must add additional series columns. The process is described in **"Instructions to Record More Than 4 Series Fields"**.
   * If you choose to delete any of the columns, you must also be sure to delete any lines which reference the deleted column(s) in the personal.ini file **(see step 5.4)**. You cannot delete the columns which are Calibre default columns, but you can delete the columns which the sample library has added.
5. Personalize your options in FanFicFare.
   1. If you need any additional guidance on using the FanFicFare plugin, see the wiki at <https://github.com/JimmXinu/FanFicFare/wiki/CalibrePlugin> and the forum at <http://www.mobileread.com/forums/showthread.php?t=259221>.
   2. Go to the FanFicFare drop-down menu and select "Configure FanFicFare". Navigate to the "personal.ini" tab and select the "Edit personal.ini" option. Note that any of the comments added by the Easy Fanfic Library project in the file will be marked as an "Easy Fanfic Library notes" or placed within "Easy Fanfic Library code".
   3. Find the line [defaults] in the personal.ini file (it should be right near the top). Look at the section of code under the heading.
      * Confirm your status as an adult (or not).
        * If you are an adult and you wish to download age-restricted works from any of the sites FanFicFare is compatible with, you may uncomment (remove # from in front of) the line "is_adult:true".  Otherwise, keep the line commented out (with a # in front of it).
        * You can also do this specifically for age-restricted works from AO3 **(see step 5.4)**.
   4. Find the line [archiveofourown.org] in the personal.ini file. Look at the section of code under the heading.
      * Add your AO3 login information (or not).
        * To add your AO3 login credentials, uncomment (remove # from in front of) the username and password lines, and replace "XXXXXXXX" with your AO3 username and password in their respective lines.
        * If you don't wish to be logged in, keep the username and password lines commented out (with a # in front of them), and do the same for the "always_login:true" line. If you don't add your login info, and then you attempt to download a login-restricted fic, the program will prompt you for your login. Alternatively, you can download the login-restricted fic outside of Calibre, add it into your library from your files (using the "Add Books" menu), and update the metadata manually.
      * Retrieve your bookmark information (if you've added your login).
        * If you wish to include information from your bookmarks in your library, or to be able to retrieve an entire page of your bookmarked works at once, uncomment the line "always_login:true". Note that you will need to have added your AO3 login info, as described above, for this to work.
        * If you don't wish retrieve bookmark information, you may keep the line commented out.
      * Confirm your status as an adult (or not).
        * If you are an adult and you wish to download age-restricted works from AO3 specifically, you may uncomment the line "is_adult:true". Otherwise, keep the line commented out.
        * You can also do this under the [defaults] section of the personal.ini file, if you wish to access age-restricted works on any site you download from **(see step 5.3)**.
      * If you added additional series columns as mentioned in **step 4** and described in **"Instructions to Record More Than 4 Series Fields"**, remember you must also add the capability to record additional series from AO3 in the personal.ini file.
6. Add fanfiction to your library! Here are some options available to you.
   * If you already have fanfic downloaded (not in Calibre), you can add those to Calibre using the "Add Books" options. To properly reformat their metadata: select the items, go to the FanFicFare dropdown menu, "Actions by Update Modes", "Update Existing FanFiction Books", and then "Update Calibre Metadata from Web Site".
   * Use the "Download from URLs" option under the FanFicFare drop-down menu.
   * Use the "Get Story URLs from Web Page" option under the FanFicFare drop-down menu.
      * You can enter the URL of a series page.
      * You can enter the URL of a creator's page of works, or their works in a particular fandom.
      * You can enter the URL of your AO3 bookmarks or marked for later page (assuming you put in your log-in info and uncommented the "always_login:true" option). This will not work for any series you have bookmarked; you will have to enter the URLs from the series pages individually.
      * Note that if you want to download all works from a list with multiple pages, such as your bookmarks or marked for later, you will need to enter each individual page from the list separately. 
           * Alternatively, if you have many pages of bookmarks/marked-for-later and wish to avoid entering the URL for each individual page, [ao3downloader](https://github.com/nianeyna/ao3downloader) can handle multiple pages automatically. AO3downloader has an option to just retrieve links, so you can use it for that purpose, and then enter the list of URLs into the FanFicFare "Download from URLs" option to get the works into the library you set up with Easy Fanfic Library.
   * You can also download anthologies into a single EPUB from a web page (such as a series page) or a list of URLS. Check out "Anthology Options" under the FanFicFare drop-down menu. Note that the work will have some funky tags and metadata because it pulls from the info for every work in the anthology.
7. For additional guidance, see the troubleshooting section.

# Instructions to Record More Than 4 Series Fields

The default settings will record series data from up to four series for any work on AO3. The sample library has four custom series columns, and a composite column, "Series (All)" (#seriesall), which will list all those series which include the work as tags. If you wish to record additional series data on works which are included in more than four series, you must add additional series columns.

To record a 5th series:

1. Select the "Preferences" drop-down menu, then "Change calibre behavior", and then "Add your own columns". This will open the columns menu.
2. Add an additional custom column of the type "Text column for keeping series-like information", with the lookup name #series5.
3. Add "{#series5:|,|}" to the end of the template for the #seriesall column.
4. Go to the FanFicFare drop-down menu and select "Configure FanFicFare". Navigate to the "personal.ini" tab and select the "Edit personal.ini" option.
5. In the personal.ini file, under "[archiveofourown.org]", at the end of items under "extra_valid_entries:", add ",series04,series04Url,series04HTML".
6. In the personal.ini file, under "[archiveofourown.org]", at the end of items under "make_linkhtml_entries:", add ",series04"
7. In the personal.ini file, under "[archiveofourown.org]", at the end of lines under "custom_columns_settings:", add the line " series04=>#series5".

To record an additional series after that:

1. Repeat the steps for recording a 5th series, but now make the new column lookup name #series6, add "{#series6:|,|}" to the end of the template for the #seriesall column, add ",series05,series05Url,series05HTML" under "extra_valid_entries: in personal.ini, add ",series05" under "make_linkhtml_entries:" in personal.ini, and add ",series05=>#series6" under "custom_columns_settings:" in personal.ini.

Follow this pattern for any further additional series columns desired.

# Troubleshooting

## General Resources

If you are having issues with the Easy Fanfic Library and wish to ask questions or leave feedback, please submit feedback on GitHub (<https://github.com/KristalC/Fanfic-Library-Easy-Setup/issues>) or through the feedback form (<https://forms.gle/h2KXYeDXaDDvsSky5>). Before you do so, please look over the common issues below. In addition, please try to be sure that your issue is with the sample library itself, not with Calibre or its plugins.

The following resources may also be of use.

* Calibre official resources
  * Calibre help website: <https://calibre-ebook.com/help>
  * Calibre bug reporting: <https://calibre-ebook.com/bugs>
* FanFicFare official resources
  * FanFicFare wiki: <https://github.com/JimmXinu/FanFicFare/wiki>
  * FanFicFare Calibre plugin forum: <http://www.mobileread.com/forums/showthread.php?t=259221>
  * FanFicFare plugin-defaults.ini file (information on plugin defaults and how to customize behavior for individual fanfiction sites): To view the plugin-defaults.ini file, go to the FanFicFare drop-down menu, select "Configure FanFicFare", navigate to the "personal.ini" tab, and select the "View Defaults (plugin-defaults.ini)" option.
* EpubMerge official resources:
  * EpubMerge Calibre plugin forum: <https://www.mobileread.com/forums/showthread.php?t=169744>
  * EpubMerge GitHub repository: <https://github.com/JimmXinu/EpubMerge>

## Error Downloading from Fanfiction.net, Fictionpress.com, and/or Ficbook.net

Some users may find that FanFicFare gives an error (due to CloudFlare) when attempting to download stories from fanfiction.net, fictionpress.com, or ficbook.net. FanFicFare offers a workaround browser cache feature, which is explained at <https://github.com/JimmXinu/FanFicFare/wiki/BrowserCacheFeature>.

## Metadata Not Properly Organized in Columns

### For works from AO3

The sample library settings are designed to add metadata to the proper columns for AO3 works. If this is not the case:

* Check your personal.ini file (FanFicFare drop-down menu => "Configure FanFicFare" => "personal.ini" tab => "Edit personal.ini"). Ensure that you did not unintentionally alter or remove lines in the personal.ini file under "custom_columns\*_\*settings:".
* If the above suggestion does not help, submit feedback on GitHub (<https://github.com/KristalC/Fanfic-Library-Easy-Setup/issues>) or using the feedback form (<https://forms.gle/h2KXYeDXaDDvsSky5>).

### For works from sites other than AO3

The sample settings should correctly add the metadata to any columns which are not AO3-specific, but there may be some variation. Some sites record the fandom or additional tags of a work differently from others.

* You can customize the settings for specific sites in the personal.ini file, just as this project has done for AO3. The plugin-defaults.ini file includes information on how to customize behavior for individual fanfiction sites, and has individual sections for many of the compatible fanfiction sites. Each site's section may include commented instructions on settings specific to that site, as well as code which can be copied and pasted into your personal.ini file. To view the plugin-defaults.ini file, go to the FanFicFare drop-down menu and select "Configure FanFicFare". Navigate to the "personal.ini" tab and select the "View Defaults (plugin-defaults.ini)" option.

# FanFicFare personal.ini Additions

Below are the major additions to the personal.ini file in the Easy Fanfic Library. The complete personal.ini settings can be found in the personal.ini settings file.

```
[defaults]
## BEGIN Fanfic Library Easy Setup code 
## This orders and lists the metadata on the file's title page in a similar order to the default listing on AO3 (for works downloaded from sites other than AO3).
titlepage_entries: publisher,rating,warnings,ships,characters,category,genre,language,seriesHTML,datePublished,dateUpdated,dateCreated,numWords,numChapters,status,description
## END Fanfic Library Easy Setup code
```
```
# The following section under the [archiveofourown.org] header
# was adapted for the Easy Fanfic Library project.
# Adapted from the plugin-defaults.ini file available on
# the personal.ini tab of the FanFicFare plugin configuration.
# plugin-defaults.ini copyright 2015 Fanficdownloader team, 2021 FanFicFare team
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

[archiveofourown.org]
use_basic_cache:true
## Some sites require login (or login for some rated stories) The
## program can prompt you, or you can save it in config.  In
## commandline version, this should go in your personal.ini, not
## defaults.ini.
#username:XXXXXXXX
#password:XXXXXXXX
## BEGIN Easy Fanfic Library Notes
## Saving your AO3 login will enable the program to access
## information from your bookmarks and save it to the appropriate
## custom columns. It will also enable the program to access any
## stories which require login, without having to prompt you. If you
## wish to save your login, add your username and password to the above 
## lines, and uncomment them. If you don't wish to be logged in,
## keep the username and password lines commented out.
## END Easy Fanfic Library Notes

## In order to get bookmarktags and bookmarksummary, you need to login
## all the time.  This defaults to off to save time and network
## traffic.  Requires valid AO3 username and password when true.
#always_login:true
## BEGIN Easy Fanfic Library Notes
## If you wish to include information from your bookmarks in your 
## library, or to be able to retrieve an entire page of your 
## bookmarked works at once, uncomment the line "always_login:true" 
## above. If you don't wish to retrieve bookmark information,
## keep the line commented out. 
## END Easy Fanfic Library Notes

## Some sites also require the user to confirm they are adult for
## adult content.  In commandline version, this should go in your
## personal.ini, not defaults.ini.
#is_adult:true
## Easy Fanfic Library Notes: If you are an adult, uncomment the above line.

## Some adapters collect additional meta information beyond the
## standard ones.  They need to be defined in extra_valid_entries to
## tell the rest of the FanFicFare system about them.  They can be
## used in include_subject_tags, titlepage_entries,
## extra_titlepage_entries, logpage_entries, extra_logpage_entries,
## and include_in_* config items.  You can also add additional entries
## here to build up composite metadata entries.
## archiveofourown.org, for example, fills genre (a standard
## entry) as the composite offreeformtags, ao3categories in
## include_in_genre.  If there's ever more than 4 series, add
## series04,series04Url etc.
extra_valid_entries:fandoms, freeformtags, freefromtags,
 ao3categories, comments, chapterslashtotal, chapterstotal, kudos,
 hits, bookmarks, collections, byline, bookmarked, bookmarktags,
 bookmarksummary, bookmarkprivate, bookmarkrec, restricted, series00,
 series01, series02, series03, series00Url, series01Url, series02Url,
 series03Url, series00HTML, series01HTML, series02HTML, series03HTML
fandoms_label:Fandoms
freeformtags_label:Freeform Tags
freefromtags_label:Freeform Tags
ao3categories_label:AO3 Categories
comments_label:Comments
chapterslashtotal_label:Chapters/Total Chapters
chapterstotal_label:Total Chapters
kudos_label:Kudos
hits_label:Hits
collections_label:Collections
## Count of bookmarks on story by all users
bookmarks_label:Bookmarks
## Tags & Summary from *your* bookmark on the story.  Only collected
## if always_login:true
bookmarked_label:Bookmarked
bookmarktags_label:Bookmark Tags
bookmarksummary_label:Bookmark Summary
bookmarkprivate_label:Bookmark Private
bookmarkrec_label:Bookmark Rec
restricted_label:Restricted to Registered Users
series00HTML_label:Series
series01HTML_label:Additional Series
series02HTML_label:Additional Series
series03HTML_label:Additional Series

## Assume entryUrl, apply to "<a class='%slink' href='%s'>%s</a>" to
## make entryHTML.
make_linkhtml_entries:series00,series01,series02,series03

## BEGIN Easy Fanfic Library code 
## This replaces any total chapter count which contains a noninteger 
## with an empty field. This way, all total chapter counts will be integers, 
## as the column requires, or or left blank.
replace_metadata:
 chapterstotal=>[0-9]*[^0-9]+[0-9]*=>

## This orders and lists the metadata on the file's title page in a similar order to the default listing on AO3.
titlepage_entries: publisher,rating,warnings,ao3categories,fandoms,ships,characters,freeformtags,language,series00HTML,series01HTML,series02HTML,series03HTML,collections,datePublished,dateUpdated,dateCreated,numWords,numChapters,chapterslashtotal,status,comments,kudos,bookmarks,hits,restricted,description,bookmarked,bookmarktags,bookmarksummary,bookmarkprivate,bookmarkrec
## END Easy Fanfic Library code
```
    
```
## BEGIN Easy Fanfic Library code
## This populates the custom columns from the sample library with AO3 metadata.
custom_columns_settings:
## These first few lines of metadata are not AO3-specific, but I've
## included the column settings here for easy setup. If you will be 
## downloading from any other sites, you may want to assign metadata for 
## these custom columns in FanFicFare's Custom Columns configuration tab. 
 characters=>#characters
 ships=>#relationships
 rating=>#maturityrating
 warnings=>#warnings
 numChapters=>#currentchapters
 numWords=>#wordcount
 status=>#status
 datePublished=>#dateposted
 dateUpdated=>#dateupdated
## The following lines deal with the AO3-specific metadata. 
 fandoms=>#fandom
 freeformtags=>#additionaltags
## Original freeformtags label had a typo- this ensures compatibility.
 freefromtags=>#additionaltags
 ao3categories=>#category
 comments=>#comments
 chapterslashtotal=>#chapterslashtotal
 chapterstotal=>#totalchapters
 kudos=>#kudos
 hits=>#hits
 bookmarks=>#bookmarks
 collections=>#collection
 restricted=>#restricted
## Information about your bookmark, if you are logged in.
 bookmarked=>#bookmarked
 bookmarktags=>#bookmarktags
 bookmarksummary=>#bookmarksummary
 bookmarkprivate=>#bookmarkprivate
 bookmarkrec=>#bookmarkrec
## Add a "fanfiction" tag to the genre column for every work from AO3.
 "FanFiction"=>#genre 
## Record series information.
 series00=>#series1
 series01=>#series2
 series02=>#series3
 series03=>#series4
## If you are using more than 4 series columns, add additional lines here.
## END Easy Fanfic Library code
 ```
