---
UID: NF:winnls.IdnToAscii
title: IdnToAscii function (winnls.h)
description: Converts an internationalized domain name (IDN) or another internationalized label to a Unicode (wide character) representation of the ASCII string that represents the name in the Punycode transfer encoding syntax.
helpviewer_keywords: ["IDN_ALLOW_UNASSIGNED","IDN_EMAIL_ADDRESS","IDN_RAW_PUNYCODE","IDN_USE_STD3_ASCII_RULES","IdnToAscii","IdnToAscii function [Internationalization for Windows Applications]","intl.idntoascii","winnls/IdnToAscii"]
old-location: intl\idntoascii.htm
tech.root: Intl
ms.assetid: e39aa5c2-3f76-40b2-9948-bbd795c6c525
ms.date: 12/05/2018
ms.keywords: IDN_ALLOW_UNASSIGNED, IDN_EMAIL_ADDRESS, IDN_RAW_PUNYCODE, IDN_USE_STD3_ASCII_RULES, IdnToAscii, IdnToAscii function [Internationalization for Windows Applications], intl.idntoascii, winnls/IdnToAscii
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
req.lib: Normaliz.lib
req.dll: Normaliz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2 and later,Windows Server 2003 with SP1
ms.custom: 19H1
f1_keywords:
 - IdnToAscii
 - winnls/IdnToAscii
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Normaliz.dll
 - kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-normaliz-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - IdnToAscii
---

## -description

Converts an internationalized domain name (IDN) or another internationalized label to a Unicode (wide character) representation of the ASCII string that represents the name in the Punycode transfer encoding syntax. 
        <div class="alert"><b>Caution</b>  This function implements the <a href="http://www.faqs.org/rfcs/rfc3490.html">RFC 3490: Internationalizing Domain Names in Applications (IDNA)</a> standard algorithm for converting an IDN to Punycode. The standard introduces some security issues. One issue is that glyphs representing certain characters from different scripts might appear similar or even identical. For example, in many fonts, Cyrillic lowercase A ("а") is indistinguishable from Latin lowercase A ("a"). There is no way to tell visually that "example.com" and "exаmple.com" are two different domain names, one with a Latin lowercase A in the name, the other with a Cyrillic lowercase A. For more information about IDN-related security concerns, see <a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>.</div>
<div> </div>

## -parameters

### -param dwFlags [in]

Flags specifying conversion options. The following table lists the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDN_ALLOW_UNASSIGNED"></a><a id="idn_allow_unassigned"></a><dl>
<dt><b>IDN_ALLOW_UNASSIGNED</b></dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  An application can set this value if it is just using a query string for normal lookup, as in a compare operation. However, the application should not set this value for a stored string, which is a string being prepared for storage.</div>
<div> </div>
Allow unassigned code points to be included in the input string. The default is to not allow unassigned code points, and fail with an extended error code of ERROR_INVALID_NAME.

This flag allows the function to process characters that are not currently legal in IDNs, but might be legal in later versions of the IDNA standard. If your application encodes unassigned code points as Punycode, the resulting domain names should be illegal. Security can be compromised if a later version of IDNA makes these names legal or if an application filters out the illegal characters to try to create a legal domain name. For more information, see <a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="IDN_USE_STD3_ASCII_RULES"></a><a id="idn_use_std3_ascii_rules"></a><dl>
<dt><b>IDN_USE_STD3_ASCII_RULES</b></dt>
</dl>
</td>
<td width="60%">
Filter out ASCII characters that are not allowed in STD3 names. The only ASCII characters allowed in the input Unicode string are letters, digits, and the hyphen-minus. The string cannot begin or end with the hyphen-minus. The function fails if the input Unicode string contains ASCII characters, such as "[", "]", or "/", that cannot occur in domain names.<div class="alert"><b>Note</b>  Some local networks can allow some of these characters in computer names.</div>
<div> </div>


The function fails if the input Unicode string contains control characters (U+0001 through U+0020) or the "delete" character (U+007F). In either case, this flag has no effect on the non-ASCII characters that are allowed in the Unicode string.

</td>
</tr>
<tr>
<td width="40%"><a id="IDN_EMAIL_ADDRESS"></a><a id="idn_email_address"></a><dl>
<dt><b>IDN_EMAIL_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
<b>Starting with Windows 8:</b> Enable EAI algorithmic fallback for the local parts of email addresses (such as <i>&lt;local&gt;</i>@microsoft.com). The default is for this function to fail when an email address has an invalid address or syntax.

An application can set this flag to enable Email Address Internationalization (EAI) to return a discoverable fallback address, if possible. For more information, see the IETF <a href="https://datatracker.ietf.org/wg/eai/charter/">Email Address Internationalization (eai) Charter</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="IDN_RAW_PUNYCODE"></a><a id="idn_raw_punycode"></a><dl>
<dt><b>IDN_RAW_PUNYCODE</b></dt>
</dl>
</td>
<td width="60%">
<b>Starting with Windows 8:</b> Disable the validation and mapping of Punycode.

</td>
</tr>
</table>

### -param lpUnicodeCharStr [in]

Pointer to a Unicode string representing an IDN or another internationalized label.

### -param cchUnicodeChar [in]

Count of characters in the input Unicode string indicated by <i>lpUnicodeCharStr</i>.

### -param lpASCIICharStr [out, optional]

Pointer to a buffer that receives a Unicode string consisting only of characters in the ASCII character set. On return from this function, the buffer contains the ASCII string equivalent of the string provided in <i>lpUnicodeCharStr</i> under Punycode. Alternatively, the function can retrieve <b>NULL</b> for this parameter, if <i>cchASCIIChar</i> is set to 0. In this case, the function returns the size required for this buffer.

### -param cchASCIIChar [in]

Size of the buffer indicated by <i>lpASCIICharStr</i>. The application can set the parameter to 0 to retrieve <b>NULL</b> in <i>lpASCIICharStr</i>.

## -returns

Returns the number of characters retrieved in <i>lpASCIICharStr</i> if successful. The retrieved string is null-terminated only if the input Unicode string is null-terminated.

If the function succeeds and the value of <i>cchASCIIChar</i> is 0, the function returns the required size, in characters including a terminating null character if it was part of the input buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_NAME. An invalid name was supplied to the function. Note that this error code catches all syntax errors. </li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_NO_UNICODE_TRANSLATION. Invalid Unicode was found in a string.</li>
</ul>

## -remarks

The function does not null-terminate an output string if the input string length is explicitly specified without a terminating null character. To null-terminate an output string for this function, the application should supply -1 for the <i>cchUnicodeChar</i> parameter or explicitly count the terminating null character for the input string.

Note that the function always fails if the input string contains control characters (U+0001 through U+0020) or the "delete" character (U+007F). Since the character U+0000 can appear only as a terminating null character, the function always fails if U+0000 appears anywhere else in the input string.

<b>Windows XP, Windows Server 2003</b>: 

No longer supported.

The required header file and DLL are part of the Microsoft Internationalized Domain Name (IDN) Mitigation APIs, which are no longer available for download.

## -see-also

<a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntonameprepunicode">IdnToNameprepUnicode</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntounicode">IdnToUnicode</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support </a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
