# Fastlane

A theme for generating sites based on
[Fastlane](https://fastlane.tools/) metadata.  This makes it very
simple to generate a website for an app, using GitHub/GitLab Pages.

## Minimum Hugo version

Hugo version `0.54.0` or higher is required. View the [Hugo releases](https://github.com/gohugoio/hugo/releases) and download the binary for your OS.

**Note**: The extended version of Hugo is only required if you wish to edit style-related params in your config file. This is because this theme uses Hugo Pipes and SCSS. 

## Installation

From the root of your site:

```
git submodule add https://github.com/guardianproject/fastlane-hugo-theme.git themes/fastlane-hugo-theme
```

## Updating

From the root of your site:

```
git submodule update --remote --merge
```

## Setup


```yaml
theme: fastlane-hugo-theme

# set the Fastlane metadata dir as the contentDir
contentDir: fastlane/android/metadata

staticDirs:
 - app/src/main/res

# the title will serve as the default, when the title hasn't been translated
title: MyAwesomeApp

# some customizations
params:
  selfHosted: true
  fastlaneDir: metadata
  fallbackLanguageCode: en-US

# setup the languages supported by this site
defaultContentLanguage: en
defaultContentLanguageInSubdir: true
languages:
  ar:
    languageCode: ar
  de:
    languageCode: de
  en:
    languageCode: en-US

# it is possible to customize the Markdown parsing
blackfriday:
  extensions:
    - hardLineBreak
```

## Credits

Thank you to [Zachary Betz](https://zwbetz.com/) for creating the [Cayman-Hugo-Theme](https://github.com/zwbetz-gh/cayman-hugo-theme).  Thank you to [Jason Long](https://github.com/jasonlong) for creating the original Jekyll [Cayman Theme](https://github.com/jasonlong/cayman-theme). 

## License

[Creative Commons Attribution 4.0 International](http://creativecommons.org/licenses/by/4.0/). 
