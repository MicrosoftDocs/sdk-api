---
UID: NF:winnls.GetStringScripts
title: GetStringScripts function (winnls.h)
description: Provides a list of scripts used in the specified Unicode string.
helpviewer_keywords: ["GSS_ALLOW_INHERITED_COMMON","GetStringScripts","GetStringScripts function [Internationalization for Windows Applications]","_win32_GetStringScripts","intl.getstringscripts","winnls/GetStringScripts"]
old-location: intl\getstringscripts.htm
tech.root: Intl
ms.assetid: 82885feb-5d9b-49ea-bcbe-c71597584c59
ms.date: 12/05/2018
ms.keywords: GSS_ALLOW_INHERITED_COMMON, GetStringScripts, GetStringScripts function [Internationalization for Windows Applications], _win32_GetStringScripts, intl.getstringscripts, winnls/GetStringScripts
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
 - GetStringScripts
 - winnls/GetStringScripts
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
 - GetStringScripts
---

# GetStringScripts function


## -description

Provides a list of scripts used in the specified Unicode string.

## -parameters

### -param dwFlags [in]

Flags specifying options for script retrieval.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GSS_ALLOW_INHERITED_COMMON"></a><a id="gss_allow_inherited_common"></a><dl>
<dt><b>GSS_ALLOW_INHERITED_COMMON</b></dt>
</dl>
</td>
<td width="60%">
Retrieve "Qaii" (INHERITED) and "Zyyy" (COMMON) script information. This flag does not affect the processing of unassigned characters. These characters in the input string always cause a "Zzzz" (UNASSIGNED script) to appear in the script string.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>   By default, <b>GetStringScripts</b> ignores any inherited or common characters in the input string indicated by <i>lpString</i>. If GSS_ALLOW_INHERITED_COMMON is not set, neither "Qaii" nor "Zyyy" appears in the script string, even if the input string contains such characters. If GSS_ALLOW_INHERITED_COMMON is set, and if the input string contains inherited and/or common characters, "Qaii" and/or "Zyyy", respectively, appear in the script string. See the Remarks section.</div>
<div> </div>

### -param lpString [in]

Pointer to the Unicode string to analyze.

### -param cchString [in]

Size, in characters, of the Unicode string indicated by <i>lpString</i>. The application sets this parameter to -1 if the Unicode string is null-terminated. If the application sets this parameter to 0, the function retrieves a null Unicode string (L"\0") in <i>lpScripts</i> and returns 1.

### -param lpScripts [out, optional]

Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in <a href="http://www.unicode.org/iso15924/iso15924-codes.html">ISO 15924</a>. Each script name consists of four Latin characters, and the names are retrieved in alphabetical order. Each name, including the last, is followed by a semicolon.

Alternatively, this parameter contains <b>NULL</b> if <i>cchScripts</i> is set to 0. In this case, the function returns the required size for the script buffer.

### -param cchScripts [in]

Size, in characters, of the script buffer indicated by <i>lpScripts</i>.

Alternatively, the application can set this parameter to 0. In this case, the function retrieves <b>NULL</b> in <i>lpScripts</i> and returns the required size for the script buffer.

## -returns

Returns the number of characters retrieved in the output buffer, including a terminating null character, if successful and <i>cchScripts</i> is set to a nonzero value. The function returns 1 to indicate that no script has been found, for example, when the input string only contains COMMON or INHERITED characters and GSS_ALLOW_INHERITED_COMMON is not set. Given that each found script adds five characters (four characters + delimiter), a simple mathematical operation provides the script count as (return_code - 1) / 5.

If the function succeeds and the value of <i>cchScripts</i> is 0, the function returns the required size, in characters including a terminating null character, for the script buffer. The script count is as described above.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_BADDB. The function could not access the data. This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</li>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function is useful as part of a strategy to mitigate security issues related to <a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">internationalized domain names (IDNs)</a>.

The script determination is based on the script values published by the Unicode Consortium in <a href="http://www.unicode.org/Public/4.1.0/ucd/Scripts.txt">http://www.unicode.org/Public/4.1.0/ucd/Scripts.txt</a>, except that the unassigned characters have the value "Zzzz" (UNASSIGNED) instead of "Zyyy" (COMMON).

Here are some examples of the behavior of this function:

<table>
<tr>
<th colspan="2">Input string</th>
<th><i>dwFlags</i></th>
<th><i>lpScripts</i></th>
<th>Scripts</th>
</tr>
<tr>
<td colspan="2">Microsoft.com</td>
<td>0</td>
<td>Latn;</td>
<td>Latin</td>
</tr>
<tr>
<td colspan="2">Microsoft.com</td>
<td>GSS_ALLOW_INHERITED_COMMON</td>
<td>Latn;Zyyy;</td>
<td>Latin + Common</td>
</tr>
<tr>
<td rowspan="2">Niño</td>
<td>004E 0069 0241 006F</td>
<td rowspan="2">GSS_ALLOW_INHERITED_COMMON</td>
<td rowspan="2">Latn;</td>
<td rowspan="2">Latin</td>
</tr>
<tr>
<td>Uses LATIN SMALL LETTER N WITH TILDE</td>
</tr>
<tr>
<td rowspan="2">Niño</td>
<td>004E 0069 006E 0303 006F</td>
<td rowspan="2">GSS_ALLOW_INHERITED_COMMON</td>
<td rowspan="2">Latn;Qaii;</td>
<td rowspan="2">Latin + Inherited</td>
</tr>
<tr>
<td>Uses COMBINING TILDE</td>
</tr>
<tr>
<td rowspan="2">Spооf</td>
<td>0053 0070 043e 043e 0066</td>
<td rowspan="2">0</td>
<td rowspan="2">Latn;Cyrl;</td>
<td rowspan="2">Latin + Cyrillic</td>
</tr>
<tr>
<td>Uses CYRILLIC SMALL LETTER O</td>
</tr>
<tr>
<td></td>
<td>U+f000</td>
<td>0</td>
<td>Zzzz;</td>
<td>Unassigned</td>
</tr>
<tr>
<td></td>
<td>U+f000</td>
<td>GSS_ALLOW_INHERITED_COMMON</td>
<td>Zzzz;</td>
<td>Unassigned</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Intl/downlevelgetstringscripts">DownlevelGetStringScripts</a>



<a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-verifyscripts">VerifyScripts</a>