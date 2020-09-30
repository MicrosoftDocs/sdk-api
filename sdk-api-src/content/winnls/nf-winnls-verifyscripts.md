---
UID: NF:winnls.VerifyScripts
title: VerifyScripts function (winnls.h)
description: Compares two enumerated lists of scripts.
helpviewer_keywords: ["VS_ALLOW_LATIN","VerifyScripts","VerifyScripts function [Internationalization for Windows Applications]","_win32_VerifyScripts","intl.verifyscripts","winnls/VerifyScripts"]
old-location: intl\verifyscripts.htm
tech.root: Intl
ms.assetid: 4780aa9f-6df0-4901-8de4-3f9118320e1b
ms.date: 12/05/2018
ms.keywords: VS_ALLOW_LATIN, VerifyScripts, VerifyScripts function [Internationalization for Windows Applications], _win32_VerifyScripts, intl.verifyscripts, winnls/VerifyScripts
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VerifyScripts
 - winnls/VerifyScripts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-normalization-l1-1-0.dll
 - KernelBase.dll
api_name:
 - VerifyScripts
---

# VerifyScripts function


## -description

Compares two enumerated lists of scripts.

## -parameters

### -param dwFlags [in]

Flags specifying script verification options.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VS_ALLOW_LATIN"></a><a id="vs_allow_latin"></a><dl>
<dt><b>VS_ALLOW_LATIN</b></dt>
</dl>
</td>
<td width="60%">
Allow "Latn" (Latin script) in the test list even if it is not in the locale list.

</td>
</tr>
</table>

### -param lpLocaleScripts [in]

Pointer to the locale list, the enumerated list of scripts for a given locale. This list is typically populated by calling <a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a> with <i>LCType</i> set to <a href="/windows/desktop/Intl/locale-sscripts">LOCALE_SSCRIPTS</a>.

### -param cchLocaleScripts [in]

Size, in characters, of the string indicated by <i>lpLocaleScripts</i>. The application sets this parameter to -1 if the string is null-terminated. If this parameter is set to 0, the function fails.

### -param lpTestScripts [in]

Pointer to the test list, a second enumerated list of scripts. This list is typically populated by calling <a href="/windows/desktop/api/winnls/nf-winnls-getstringscripts">GetStringScripts</a>.

### -param cchTestScripts [in]

Size, in characters, of the string indicated by <i>lpTestScripts</i>. The application sets this parameter to -1 if the string is null-terminated. If this parameter is set to 0, the function fails.

## -returns

Returns <b>TRUE</b> if the test list is non-empty and all items in the list are also included in the locale list. The function still returns <b>TRUE</b> if the locale list contains more scripts than the test list, but all the test list scripts must be contained in the locale list. If VS_ALLOW_LATIN is specified in <i>dwFlags</i>, the function behaves as if "Latn;" is always in the locale list.

In all other cases, the function returns <b>FALSE</b>. This return can indicate that the test list contains an item that is not in the locale list, or it can indicate an error. To distinguish between these two cases, the application should call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_SUCCESS. The action completed successfully but yielded no results.</li>
</ul>

## -remarks

This function compares strings, such as "Latn;Cyrl;", that consist of a series of 4-character script names, with each script name followed by a semicolon. It also has a special case to account for the fact that the Latin script is often used in languages and locales for which it is not native.

This function is useful as part of a strategy to mitigate security issues related to <a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">internationalized domain names (IDNs)</a>.

The following are examples of the return of this function and a subsequent call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> in various scenarios. The last two examples illustrate, respectively, a case in which the test list lacks a terminating semicolon (malformed string) and a case in which the test list is empty.

<table>
<tr>
<th>Locale string</th>
<th>Test string</th>
<th><i>dwFlags</i></th>
<th>Return value</th>
<th><b>GetLastError</b> return</th>
</tr>
<tr>
<td>Hani;Hira;Kana;</td>
<td>Hani;</td>
<td>*</td>
<td><b>TRUE</b></td>
<td>(unchanged)</td>
</tr>
<tr>
<td>Hani;Hira;Kana;</td>
<td>Hani;Latn;</td>
<td>0</td>
<td><b>FALSE</b></td>
<td>ERROR_SUCCESS</td>
</tr>
<tr>
<td>Hani;Hira;Kana;</td>
<td>Hani;Latn;</td>
<td>VS_ALLOW_LATIN</td>
<td><b>TRUE</b></td>
<td>(unchanged)</td>
</tr>
<tr>
<td>Hani;Hira;Kana;</td>
<td>Cyrl;</td>
<td>*</td>
<td><b>FALSE</b></td>
<td>ERROR_SUCCESS</td>
</tr>
<tr>
<td>Hani;</td>
<td>Hani;Hira;Kana;</td>
<td>*</td>
<td>FALSE</td>
<td>ERROR_SUCCESS</td>
</tr>
<tr>
<td>Hani;Hira;Kana;</td>
<td>Cyrl</td>
<td>*</td>
<td><b>FALSE</b></td>
<td>ERROR_INVALID_PARAMETER</td>
</tr>
<tr>
<td>Hani;Hira;Kana;</td>
<td></td>
<td>*</td>
<td>TRUE</td>
<td>(unchanged)</td>
</tr>
</table>
 

* Results are the same whether VS_ALLOW_LATIN is passed in the <i>dwFlags</i> parameter or no flags are supplied.


#### Examples


<a href="/windows/desktop/Intl/nls--internationalized-domain-name--idn--mitigation-sample">NLS: Internationalized Domain Name (IDN) Mitigation Sample</a> demonstrates the use of this function.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Intl/downlevelverifyscripts">DownlevelVerifyScripts</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getstringscripts">GetStringScripts</a>



<a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>