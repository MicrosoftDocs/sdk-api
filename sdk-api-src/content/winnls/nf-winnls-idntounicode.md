---
UID: NF:winnls.IdnToUnicode
title: IdnToUnicode function (winnls.h)
description: Converts the Punycode form of an internationalized domain name (IDN) or another internationalized label to the normal Unicode UTF-16 encoding syntax.
helpviewer_keywords: ["IdnToUnicode","IdnToUnicode function [Internationalization for Windows Applications]","_win32_IdnToUnicode","intl.idntounicode","winnls/IdnToUnicode"]
old-location: intl\idntounicode.htm
tech.root: Intl
ms.assetid: 90707414-aef7-4265-bc2b-d48ac79db099
ms.date: 12/05/2018
ms.keywords: IdnToUnicode, IdnToUnicode function [Internationalization for Windows Applications], _win32_IdnToUnicode, intl.idntounicode, winnls/IdnToUnicode
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
req.redist: Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2 and later, orWindows Server 2003 with SP1
ms.custom: 19H1
f1_keywords:
 - IdnToUnicode
 - winnls/IdnToUnicode
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
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-normaliz-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - IdnToUnicode
---

# IdnToUnicode function


## -description

Converts the Punycode form of an internationalized domain name (IDN) or another internationalized label to the normal <a href="/windows/desktop/Intl/unicode">Unicode</a> UTF-16 encoding syntax.         <div class="alert"><b>Caution</b>  This function implements the <a href="http://www.faqs.org/rfcs/rfc3490.html">RFC 3490: Internationalizing Domain Names in Applications (IDNA)</a> standard algorithms for the Punycode encoding of Unicode. The standard introduces some security issues. One issue is that glyphs representing certain characters from different scripts might appear similar or even identical. For example, in many fonts, Cyrillic lowercase A ("а") is indistinguishable from Latin lowercase A ("a"). There is no way to tell visually that "example.com" and "exаmple.com" are two different domain names, one with a Latin lowercase A in the name, the other with a Cyrillic lowercase A. For more information about IDN-related security concerns, see <a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>.</div>
<div> </div>

## -parameters

### -param dwFlags [in]

Flags specifying conversion options. For detailed definitions, see the <i>dwFlags</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a>.

### -param lpASCIICharStr [in]

Pointer to a string representing the Punycode encoding of an IDN or another internationalized label. This string must consist only of ASCII characters, and can include Punycode-encoded Unicode. The function decodes Punycode values to their UTF-16 values.

### -param cchASCIIChar [in]

Count of characters in the input string indicated by <i>lpASCIICharStr</i>.

### -param lpUnicodeCharStr [out, optional]

Pointer to a buffer that receives a normal Unicode UTF-16 encoding equivalent to the Punycode value of the input string. Alternatively, the function can retrieve <b>NULL</b> for this parameter, if <i>cchUnicodeChar</i> set to 0. In this case, the function returns the size required for this buffer.

### -param cchUnicodeChar [in]

Size, in characters, of the buffer indicated by <i>lpUnicodeCharStr</i>. The application can set the size to 0 to retrieve <b>NULL</b> in <i>lpUnicodeCharStr</i> and have the function return the required buffer size.

## -returns

Returns the number of characters retrieved in <i>lpUnicodeCharStr</i> if successful. The retrieved string is null-terminated only if the input string is null-terminated.

If the function succeeds and the value of <i>cchUnicodeChar</i> is 0, the function returns the required size, in characters including a terminating null character if it was part of the input buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_NAME. An invalid name was supplied to the function. Note that this error code catches all syntax errors. </li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_NO_UNICODE_TRANSLATION. Invalid Unicode was found in a string.</li>
</ul>

## -remarks

See Remarks for <a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a>.

## -see-also

<a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntonameprepunicode">IdnToNameprepUnicode</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>