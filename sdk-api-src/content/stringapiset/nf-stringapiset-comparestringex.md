---
UID: NF:stringapiset.CompareStringEx
title: CompareStringEx function
author: windows-sdk-content
description: Compares two Unicode (wide character) strings, for a locale specified by name.Caution  Using CompareStringEx incorrectly can compromise the security of your application.
old-location: intl\comparestringex.htm
old-project: Intl
ms.assetid: 264c67b6-848d-48ef-9bfa-4990bfa2fbf5
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: CompareStringEx, CompareStringEx function [Internationalization for Windows Applications], LINGUISTIC_IGNORECASE, LINGUISTIC_IGNOREDIACRITIC, NORM_IGNORECASE, NORM_IGNOREKANATYPE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREWIDTH, NORM_LINGUISTIC_CASING, SORT_DIGITSASNUMBERS, SORT_STRINGSORT, _win32_CompareStringEx, _win32_CompareStringEx_cpp, intl.comparestringex, stringapiset/CompareStringEx, winui._win32_CompareStringEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: stringapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MPR50_SERVICE_CHARACTERISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-String-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CompareStringEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# CompareStringEx function


## -description


Compares two Unicode (wide character) strings, for a <a href="https://msdn.microsoft.com/8214c00d-4ec6-4597-8088-7819a160f0dc">locale</a> specified by name.
<div class="alert"><b>Caution</b>  Using <b>CompareStringEx</b> incorrectly can compromise the security of your application. Strings that are not compared correctly can produce invalid input. Test strings to make sure they are valid before using them, and provide error handlers. For more information, see <a href="https://msdn.microsoft.com/4034f479-ad29-4c6f-82c6-977f420c4d4d">Security Considerations: International Features</a>.</div><div> </div><div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> if designed to run only on Windows Vista and later.</div><div> </div>

## -parameters




### -param lpLocaleName [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param dwCmpFlags [in]

Flags that indicate how the function compares the two strings. By default, these flags are not set. This parameter can specify a combination of any of the following values, or it can be set to 0 to obtain the default behavior.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LINGUISTIC_IGNORECASE"></a><a id="linguistic_ignorecase"></a><dl>
<dt><b>LINGUISTIC_IGNORECASE</b></dt>
</dl>
</td>
<td width="60%">
Ignore case, as linguistically appropriate.

</td>
</tr>
<tr>
<td width="40%"><a id="LINGUISTIC_IGNOREDIACRITIC"></a><a id="linguistic_ignorediacritic"></a><dl>
<dt><b>LINGUISTIC_IGNOREDIACRITIC</b></dt>
</dl>
</td>
<td width="60%">
Ignore nonspacing characters, as linguistically appropriate.

<div class="alert"><b>Note</b>  This flag does not always produce predictable results when used with decomposed characters, that is, characters in which a base character and one or more nonspacing characters each have distinct code point values.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORECASE"></a><a id="norm_ignorecase"></a><dl>
<dt><b>NORM_IGNORECASE</b></dt>
</dl>
</td>
<td width="60%">
Ignore case. For many scripts (notably Latin scripts), NORM_IGNORECASE coincides with LINGUISTIC_IGNORECASE.

<div class="alert"><b>Note</b>  NORM_IGNORECASE ignores any tertiary distinction, whether it is actually linguistic case or not. For example, in Arabic and Indic scripts, this distinguishes alternate forms of a character, but the differences do not correspond to linguistic case. LINGUISTIC_IGNORECASE causes the function to ignore only actual linguistic casing, instead of ignoring the third sorting weight.</div>
<div> </div>
<div class="alert"><b>Note</b>  With this flag set, the function ignores the distinction between the wide and narrow forms of the CJK compatibility characters.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREKANATYPE"></a><a id="norm_ignorekanatype"></a><dl>
<dt><b>NORM_IGNOREKANATYPE</b></dt>
</dl>
</td>
<td width="60%">
Do not differentiate between hiragana and katakana characters. Corresponding hiragana and katakana characters compare as equal.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORENONSPACE"></a><a id="norm_ignorenonspace"></a><dl>
<dt><b>NORM_IGNORENONSPACE</b></dt>
</dl>
</td>
<td width="60%">
Ignore nonspacing characters. For many scripts (notably Latin scripts), NORM_IGNORENONSPACE coincides with LINGUISTIC_IGNOREDIACRITIC.

<div class="alert"><b>Note</b>  NORM_IGNORENONSPACE ignores any secondary distinction, whether it is a diacritic or not. Scripts for Korean, Japanese, Chinese, and Indic languages, among others, use this distinction for purposes other than diacritics. LINGUISTIC_IGNOREDIACRITIC causes the function to ignore only actual diacritics, instead of ignoring the second sorting weight.</div>
<div> </div>
<div class="alert"><b>Note</b>  NORM_IGNORENONSPACE only has an effect for locales in which accented characters are sorted in a second pass from main characters. Normally all characters in the string are first compared without regard to accents and, if the strings are equal, a second pass over the strings is performed to compare accents. This flag causes the second pass to not be performed. For locales that sort accented characters in the first pass, this flag has no effect.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORESYMBOLS"></a><a id="norm_ignoresymbols"></a><dl>
<dt><b>NORM_IGNORESYMBOLS</b></dt>
</dl>
</td>
<td width="60%">
Ignore symbols and punctuation.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREWIDTH"></a><a id="norm_ignorewidth"></a><dl>
<dt><b>NORM_IGNOREWIDTH</b></dt>
</dl>
</td>
<td width="60%">
Ignore the difference between half-width and full-width characters, for example, C a t == cat. The full-width form is a formatting distinction used in Chinese and Japanese scripts.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_LINGUISTIC_CASING"></a><a id="norm_linguistic_casing"></a><dl>
<dt><b>NORM_LINGUISTIC_CASING</b></dt>
</dl>
</td>
<td width="60%">
Use the default linguistic rules for casing, instead of file system rules. Note that most scenarios for <b>CompareStringEx</b> use this flag. This flag does not have to be used when your application calls <a href="https://msdn.microsoft.com/6a457076-7992-4912-8ac5-2258f9651a8c">CompareStringOrdinal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SORT_DIGITSASNUMBERS"></a><a id="sort_digitsasnumbers"></a><dl>
<dt><b>SORT_DIGITSASNUMBERS</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 7:</b> Treat digits as numbers during sorting, for example, sort "2" before "10".

</td>
</tr>
<tr>
<td width="40%"><a id="SORT_STRINGSORT"></a><a id="sort_stringsort"></a><dl>
<dt><b>SORT_STRINGSORT</b></dt>
</dl>
</td>
<td width="60%">
Treat punctuation the same as symbols.

</td>
</tr>
</table>
 


### -param lpString1 [in]

Pointer to the first string to compare.


### -param cchCount1 [in]

Length of the string indicated by <i>lpString1</i>, excluding the terminating null character. The application can supply a negative value if the string is null-terminated. In this case, the function determines the length automatically.


### -param lpString2 [in]

Pointer to the second string to compare.


### -param cchCount2 [in]

Length of the string indicated by <i>lpString2</i>, excluding the terminating null character. The application can supply a negative value if the string is null-terminated. In this case, the function determines the length automatically.


### -param lpVersionInformation [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a> structure that contains the version information about the relevant NLS capability; usually retrieved from <a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a>.

<b>Windows Vista, Windows 7:</b> Reserved; must set to <b>NULL</b>.


### -param lpReserved [in, optional]

Reserved; must set to <b>NULL</b>.


### -param lParam [in, optional]

Reserved; must be set to 0.


## -returns



Returns one of the following values if successful. To maintain the C runtime convention of comparing strings, the value 2 can be subtracted from a nonzero return value. Then, the meaning of &lt;0, ==0, and &gt;0 is consistent with the C runtime.

<ul>
<li>CSTR_LESS_THAN. The string indicated by <i>lpString1</i> is less in lexical value than the string indicated by <i>lpString2</i>.</li>
<li>CSTR_EQUAL. The string indicated by <i>lpString1</i> is equivalent in lexical value to the string indicated by <i>lpString2</i>. The two strings are equivalent for sorting purposes, although not necessarily identical.</li>
<li>CSTR_GREATER_THAN. The string indicated by <i>lpString1</i> is greater in lexical value than the string indicated by <i>lpString2</i>.</li>
</ul>
The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were invalid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid. </li>
</ul>



## -remarks



Both <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> and <b>CompareStringEx</b> are optimized to run at the highest speed when <i>dwCmpFlags</i> is set to 0 or NORM_IGNORECASE, <i>cchCount1</i> and <i>cchCount2</i> are set to -1, and the locale does not support any linguistic compressions, as when traditional Spanish sorting treats "ch" as a single character.

Both <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> and <b>CompareStringEx</b> ignore Arabic kashidas during the comparison. Thus, if two strings are identical except for the presence of kashidas, the function returns CSTR_EQUAL.
      

When the application uses the NORM_IGNORENONSPACE and NORM_IGNORECASE flags with the sorting function, the flags can sometimes interfere with string comparisons. This situation might result for a locale that does not support non-spacing characters or case, but uses equivalent weight levels to handle other important operations. In such cases, your application should use the LINGUISTIC_IGNOREDIACRITIC and LINGUISTIC_IGNORECASE flags. These flags provide linguistically appropriate results for sorting code points that use case and diacritic marks, and have no impact on other code points.

<b>Beginning in Windows Vista: </b> Both <a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a> and <b>CompareStringEx</b> can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.
      

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.

<b>Beginning in Windows 8: </b><b>CompareStringEx</b>  is declared in Stringapiset.h. Before Windows 8, it was declared in Winnls.h.

<div class="alert"><b>Note</b>  The behavior of sorting can change between Windows releases. For example, there may be new Unicode code points created. Use <a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNlsVersionEx</a> to discover if the sort version has changed.</div>
<div> </div>

#### Examples

An example showing the use of this function can be found in <a href="https://msdn.microsoft.com/0502dba0-a26f-4238-b68e-bb41ef17ff08">NLS: Name-based APIs Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a>



<a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">Custom Locales</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/4034f479-ad29-4c6f-82c6-977f420c4d4d">Security Considerations: International Features</a>



<a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>
 

 

