+++
title = "सङ्गणक-व्यवस्था"
unicode_script = "devanagari"
+++
For English instructions [go here](../computer-setup_en/) ।

## समानं कर्म
- अधः XYZ इति यद् अस्ति, तस्य स्थाने स्वीयं github-नाम प्रयुङ्क्ताम्।
- https://github.com/XYZ/AgamaH इति पूर्वम् एव वर्तते चेन् निष्कासयतु browser-उपयोगेन।
- https://github.com/vishvAsa/AgamaH इत्यत्र गत्वा पुनः fork इति करोतु। https://github.com/XYZ/AgamaH इति किञ्चिल् लभ्यते।

## सङ्गणके समीचीनस्थानप्राप्तिः
- ततः समीचीनस्थाने terminal/ command-prompt इत्य् उद्घाट्य गच्छतु। यथा
  - `cd F:\Git\` इति windows पक्षे
  - `cd ~` इति linux पक्षे

## सञ्चिकाप्राप्तिः
- सङ्गणके समीचीनस्थानप्राप्तिः इति भागे यद् उक्तं तत् कृत्वा

```
git clone --single-branch --depth 1 --branch master https://github.com/XYZ/AgamaH.git AgamaH-master
cd AgamaH-master
git remote add upstream https://github.com/vishvAsa/AgamaH.git
git submodule update --init  themes/sanskrit-documentation-theme-hugo
cd ..

git clone --single-branch --depth 1 --branch content https://github.com/XYZ/AgamaH.git AgamaH-content
cd AgamaH-content
git remote add upstream https://github.com/vishvAsa/AgamaH.git
git pull upstream content
cd ..

```

## hugo-चालनम्
- सङ्गणके समीचीनस्थानप्राप्तिः इति भागे यद् उक्तं तत् कृत्वा

```
cd AgamaH-master
git pull upstream master
cd themes/sanskrit-documentation-theme-hugo/
git pull origin master
cd ../.. 
hugo server --renderToDisk --config ./config_dev.toml
```

## सञ्चिकासु प्राप्तासु सत्सु कार्यम्
- यदि कार्यम् AgamaH-content इत्यस्मिन् क्रियते
    - `git pull upstream content` इति परिवर्तनानि लभ्यानि।
    - ततो नुदित्वाकर्षणाभ्यर्थनं https://github.com/XYZ/AgamaH/tree/content इत्यत्र गत्वा प्रेषणीयम्।
- यदि कार्यम् AgamaH-static इत्यस्मिन् क्रियते
    - `git pull upstream static_files` इति परिवर्तनानि लभ्यानि।
    - ततो नुदित्वाकर्षणाभ्यर्थनं https://github.com/XYZ/AgamaH/tree/static_files इत्यत्र गत्वा प्रेषणीयम्।

