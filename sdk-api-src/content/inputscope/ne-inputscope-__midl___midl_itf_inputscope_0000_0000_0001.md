---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_inputscope_0000_0000_0001 enumeration


## -description


The <a href="tsf.inputscope">InputScope</a> enumeration contains values that specify which input scopes are applied to a given field.


## -enum-fields




### -field IS_DEFAULT

Indicates the standard recognition bias. Treated as default and uses the default lexicon. If combined with another input scope, it does not force coercion on the other input scope.


### -field IS_URL

Indicates a URL, File, or FTP format. Examples include the following.

<ul>
<li>http://www.humongousinsurance.com/</li>
<li>ftp://ftp.microsoft.com</li>
<li>www.microsoft.com</li>
<li>file:///C:\templ.txt</li>
<li>$</li>
</ul>

### -field IS_FILE_FULLFILEPATH

Indicates a file path. The following conditions are enforced.

<ul>
<li>For server name and share name, allows all IS_ONECHAR characters except: * ? : &lt; &gt; |</li>
<li>For file name, allows all IS_ONECHAR characters except: \ / : &lt; &gt; |</li>
<li>Input must start with \\ or drive name or \ or ..\ or .\ or /</li>
<li>Spaces are allowed.</li>
</ul>
Examples include the following.

<ul>
<li>\\servername\sharename\filename.txt</li>
<li>C:\temp\current work.doc</li>
<li>../images/hank.jpg</li>
</ul>

### -field IS_FILE_FILENAME

Indicates a file name. The following conditions are enforced.

<ul>
<li>Accepts either extension or no extension.</li>
<li>Allows all IS_ONECHAR characters except: \ / : &lt; &gt; |</li>
<li>Spaces are allowed.</li>
</ul>
Examples include the following:

<ul>
<li>filename.txt</li>
<li>filename</li>
<li>file name.txt</li>
</ul>

### -field IS_EMAIL_USERNAME

Indicates email user names. Examples include the following.

<ul>
<li>jeffsm</li>
<li>JeffSm</li>
<li>Jsmith</li>
<li>JSmith</li>
<li>jeffsmith</li>
</ul>

### -field IS_EMAIL_SMTPEMAILADDRESS

Indicates a complete SMTP email address, for example, someone@example.com.


### -field IS_LOGINNAME

Indicates a log-in name and domain. The following conditions are enforced.

<ul>
<li>Allows all IS_ONECHAR characters.</li>
<li>Does not allow domain or username to start or end in a non-alphanumeric character.</li>
<li>Spaces are not allowed.</li>
</ul>
Examples include the following.

<ul>
<li>CHICAGO\JSMITH</li>
<li>JSMITH</li>
</ul>

### -field IS_PERSONALNAME_FULLNAME

Indicates a combination of first, middle, and last names. Examples include the following, formatted for English (United States).

<ul>
<li>Mr. Jeff A. Smith, Jr.</li>
<li>Jeff Smith</li>
<li>Smith, Jeff</li>
<li>Smith, Jeff A</li>
</ul>

### -field IS_PERSONALNAME_PREFIX

Indicates a honorific or title preceding a name. Examples include the following, formatted for English (United States).

<ul>
<li>Mr.</li>
<li>Dr.</li>
<li>Miss</li>
<li>Sir</li>
</ul>

### -field IS_PERSONALNAME_GIVENNAME

Indicates a first name or initial. Examples include the following, formatted for English (United States).

<ul>
<li>Jeff</li>
<li>J.</li>
<li>J.A.</li>
</ul>

### -field IS_PERSONALNAME_MIDDLENAME

Indicates a middle name or initial. Examples include the following.

<ul>
<li>Albert</li>
<li>A.</li>
</ul>

### -field IS_PERSONALNAME_SURNAME

Indicates a last name. Examples include the following, formatted for English (United States).

<ul>
<li>Smith</li>
<li>Smith Jones</li>
<li>Smith-Jones</li>
</ul>

### -field IS_PERSONALNAME_SUFFIX

Indicates a name suffix abbreviation or Roman numerals. Examples include the following.

<ul>
<li>Jr.</li>
<li>III</li>
</ul>

### -field IS_ADDRESS_FULLPOSTALADDRESS

Indicates a full address, including numbers. Examples include the following, formatted for English (United States).

<ul>
<li>123 Main Street, Anytown, WA 98989</li>
<li>PO Box 123 Anytown, WA 98989</li>
</ul>

### -field IS_ADDRESS_POSTALCODE

Indicates an alphanumeric postal code. The value is alphanumeric to support international zip codes. Examples include the following, formatted for English (United States).

<ul>
<li>98989</li>
<li>98989-1234</li>
</ul>

### -field IS_ADDRESS_STREET

Indicates a house number, street number, apartment name and number, and/or postal box. Examples include the following.

<ul>
<li>123 Main Street</li>
<li>P.O. Box 1234</li>
</ul>

### -field IS_ADDRESS_STATEORPROVINCE

Indicates a full name or abbreviation of state or province. Examples include the following, formatted for English (United States).

<ul>
<li>WA</li>
<li>Washington</li>
<li>Wa</li>
</ul>

### -field IS_ADDRESS_CITY

Indicates the name or abbreviation of a city. Examples include the following, formatted for English (United States).

<ul>
<li>New York</li>
<li>NYC</li>
</ul>

### -field IS_ADDRESS_COUNTRYNAME

Indicates the name of a country/region. Examples include the following, formatted for English (United States).

<ul>
<li>Italy</li>
<li>Japan</li>
<li>United States of America</li>
</ul>

### -field IS_ADDRESS_COUNTRYSHORTNAME

Indicates the abbreviation of the name of a country/region. Examples include the following, formatted for English (United States).

<ul>
<li>USA</li>
<li>U.S.A.</li>
</ul>

### -field IS_CURRENCY_AMOUNTANDSYMBOL

Indicates currency symbols and numbers. Examples include the following, formatted for English (United States).

<ul>
<li>$ 2,100.25</li>
<li>$.35</li>
<li>$1,234.50 USD</li>
</ul>

### -field IS_CURRENCY_AMOUNT

Indicates a numeric value for currency, excluding currency symbols. For example, 2,100.25.


### -field IS_DATE_FULLDATE

Indicates a full date, in a variety of formats. Examples include the following, formatted for English (United States).

<ul>
<li>07-17-2001</li>
<li>7/17/01</li>
<li>7/17</li>
<li>Dec. 12</li>
<li>July 17</li>
<li>July 17, 2001</li>
</ul>

### -field IS_DATE_MONTH

Indicates a numeric representation of months, constrained to 1-12. Examples include the following.

<ul>
<li>7</li>
<li>07</li>
<li>11</li>
</ul>

### -field IS_DATE_DAY

Indicates a numeric representation of days, constrained to 1-31. Examples include the following.

<ul>
<li>1</li>
<li>04</li>
<li>17</li>
</ul>

### -field IS_DATE_YEAR

Indicates a numeric representation of years. Examples include the following.

<ul>
<li>1988</li>
<li>2004</li>
<li>88</li>
<li>04</li>
<li>'88</li>
</ul>

### -field IS_DATE_MONTHNAME

Indicates a character representation of months. Examples include the following, formatted for English (United States).

<ul>
<li>December</li>
<li>Dec</li>
<li>Dec.</li>
</ul>

### -field IS_DATE_DAYNAME

Indicates a character representation of days. Examples include the following, formatted for English (United States).

<ul>
<li>Wednesday</li>
<li>Weds</li>
<li>Weds.</li>
</ul>

### -field IS_DIGITS

Indicates positive whole numbers, constrained to 0-9.


### -field IS_NUMBER

Indicates numbers, including commas, negative sign, and decimal. For United States locations, the following conditions are enforced.

<ul>
<li>The thousand separator is a comma.</li>
<li>The decimal separator is a period.</li>
<li>Negative numbers are represented with a hyphen without a space, not with parentheses.</li>
</ul>

### -field IS_ONECHAR

Indicates a single ANSI character, codepage 1252. For United States locations, this includes the following characters.

ABCDEFGHIJKLMNOPQRSTUVWXYZabcdEfghijklmnopqrstuvwxyz0123456789!\"#$%&amp;'()*+,-./:;&lt;=&gt;?@[\]^_`{|}~


### -field IS_PASSWORD

Indicates a password. <b>IS_PASSWORD</b> is not supported and may be altered or unavailable in the future.


<div class="alert"><b>Note</b>  <b>IS_PASSWORD</b> only indicates the password; it doesn't provide any security around the password. All passwords fields should have text services disabled to maintain password secrecy, and therefore it is not valid to have a password field with an <b>IS_PASSWORD</b> input scope.</div>
<div> </div>



### -field IS_TELEPHONE_FULLTELEPHONENUMBER

Indicates a telephone number. Alphabetical input is not allowed. Examples include the following, formatted for English (United States).

<ul>
<li>(206) 555-0123</li>
<li>555-0123</li>
<li>555.0123</li>
<li>206-555-0123</li>
<li>1-206-555-0123x1234</li>
<li>+1 (206) 555-1234</li>
</ul>

### -field IS_TELEPHONE_COUNTRYCODE

Indicates telephone country codes. Examples include the following, formatted for English (United States).

<ul>
<li>+1</li>
<li>+44</li>
<li>001</li>
<li>00 44</li>
</ul>

### -field IS_TELEPHONE_AREACODE

Indicates telephone area codes. Examples include the following, formatted for English (United States).

<ul>
<li>(206)</li>
<li>206</li>
</ul>

### -field IS_TELEPHONE_LOCALNUMBER

Indicates a telephone number, excluding country or area code. Examples include the following, formatted for English (United States).

<ul>
<li>555-0123</li>
<li>555 0123</li>
<li>555.0123</li>
</ul>

### -field IS_TIME_FULLTIME

Indicates hours, minutes, seconds, and alphabetical time abbreviations. US English uses the 12 hour clock. Leading zeros are optional for hours but required for minutes and seconds. Hours are constrained to 0-24; minutes and seconds are constrained to 0-59. Examples include the following, formatted for English (United States).

<ul>
<li>3:20</li>
<li>04:30</li>
<li>11:20:55</li>
<li>11:15 am</li>
<li>4:30 AM</li>
</ul>

### -field IS_TIME_HOUR

Indicates a numeric representation of hours, constrained to 0-24.


### -field IS_TIME_MINORSEC

Indicates a numeric representation of minutes or seconds, constrained to 0-59.


### -field IS_NUMBER_FULLWIDTH

Indicates full-width number, used for Japanese only. Constrained to full-width numbers and Kanji numbers.


### -field IS_ALPHANUMERIC_HALFWIDTH

Indicates half-width alphanumeric characters for East-Asian languages, constrained to half-width alphabetical characters and numbers.


### -field IS_ALPHANUMERIC_FULLWIDTH

Indicates full-width alphanumeric characters for East-Asian languages, constrained to full-width alphabet characters and numbers.


### -field IS_CURRENCY_CHINESE

Indicates Chinese currency.


### -field IS_BOPOMOFO

Indicates Bopomofo characters.


### -field IS_HIRAGANA

Indicates Hiragana characters.


### -field IS_KATAKANA_HALFWIDTH

Indicates half-width Katakana characters.


### -field IS_KATAKANA_FULLWIDTH

Indicates full-width Katakana characters.


### -field IS_HANJA

Indicates Hanja characters.


### -field IS_HANGUL_HALFWIDTH


### -field IS_HANGUL_FULLWIDTH


### -field IS_SEARCH

<b>Starting with Windows 8:</b> Indicates a search string.


### -field IS_FORMULA

<b>Starting with Windows 8:</b> Indicates a formula control, for example, a spreadsheet field.


### -field IS_SEARCH_INCREMENTAL

<b>Starting with Windows 10:</b> Indicates input scope is intended for search boxes where incremental results are displayed as the user types.


### -field IS_CHINESE_HALFWIDTH

<b>Starting with Windows 10:</b> Indicates input scope is intended for Chinese half-width characters.


### -field IS_CHINESE_FULLWIDTH

<b>Starting with Windows 10:</b> Indicates input scope is intended for Chinese full-width characters.


### -field IS_NATIVE_SCRIPT

<b>Starting with Windows 10:</b> Indicates input scope is intended for native script.


### -field IS_YOMI

<b>Starting with Windows 10:</b> Indicates input scope is intended for Japanese names.


### -field IS_TEXT

<b>Starting with Windows 10:</b> Indicates input scope is intended for working with text.


### -field IS_CHAT

<b>Starting with Windows 10:</b> Indicates input scope is intended for chat strings.


### -field IS_NAME_OR_PHONENUMBER

<b>Starting with Windows 10:</b> Indicates input scope is intended for working with a name or telephone number.


### -field IS_EMAILNAME_OR_ADDRESS

<b>Starting with Windows 10:</b> Indicates input scope is intended for working with an email name or full email address.


### -field IS_PRIVATE

<b>Starting with Windows 10:</b> Indicates input scope is intended for working with private data.


### -field IS_MAPS

<b>Starting with Windows 10:</b> Indicates input scope is intended for working with a map location.


### -field IS_NUMERIC_PASSWORD

<b>Starting with Windows 10:</b> Indicates expected input is a numeric password, or PIN.


### -field IS_NUMERIC_PIN

<b>Starting with Windows 10:</b> Indicates expected input is a numeric PIN.


### -field IS_ALPHANUMERIC_PIN

<b>Starting with Windows 10:</b> Indicates expected input is an alphanumeric PIN.


### -field IS_ALPHANUMERIC_PIN_SET

<b>Starting with Windows 10:</b> Indicates expected input is an alphanumeric PIN for lock screen.


### -field IS_FORMULA_NUMBER

<b>Starting with Windows 10:</b> Indicates expected input is a mathematical formula.


### -field IS_CHAT_WITHOUT_EMOJI

<b>Starting with Windows 10:</b> Indicates expected input does not include emoji. 


### -field IS_PHRASELIST

Indicates a phrase list.


### -field IS_REGULAREXPRESSION

Indicates a regular expression.


### -field IS_SRGS

Indicates an XML string that conforms to the Speech Recognition Grammar Specification (SRGS) standard. Information on SRGS can be found at <a href="http://go.microsoft.com/fwlink/p/?linkid=161740">http://www.w3.org/TR/speech-grammar</a>.


### -field IS_XML

Indicates a custom xml string.


### -field IS_ENUMSTRING

The scope contains the IEnumString interface pointer. The Text Input Processor (TIP) can call <a href="https://msdn.microsoft.com/89379dab-6f96-4a86-8433-b6b0a8e45516">ITfInputScope2::EnumWordList</a> to retrieve it.


#### - IS_HANJA_FULLWIDTH

Indicates Hanja characters.


#### - IS_HANJA_HALFWIDTH

Indicates Hanja characters.


## -remarks



Whether a given input scope value is supported can vary across technologies.




## -see-also




<a href="https://msdn.microsoft.com/b2a045dd-dc2c-489d-bcb9-80710faef9c2">
        ITfInputScope
      </a>



<a href="https://msdn.microsoft.com/4098525c-8d29-419a-9484-9e70420416bc">SetInputScope</a>



<a href="https://msdn.microsoft.com/bd770852-412a-4097-b22f-02f240516770">SetInputScopeXML</a>



<a href="https://msdn.microsoft.com/28c0be9b-f42c-4ab1-a3af-9c591a5192dd">SetInputScopes</a>
 

 

