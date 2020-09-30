---
UID: NF:winnls.IdnToNameprepUnicode
title: IdnToNameprepUnicode function (winnls.h)
description: Converts an internationalized domain name (IDN) or another internationalized label to the NamePrep form specified by Network Working Group RFC 3491, but does not perform the additional conversion to Punycode.
helpviewer_keywords: ["IdnToNameprepUnicode","IdnToNameprepUnicode function [Internationalization for Windows Applications]","_win32_IdnToNameprepUnicode","intl.idntonameprepunicode","winnls/IdnToNameprepUnicode"]
old-location: intl\idntonameprepunicode.htm
tech.root: Intl
ms.assetid: 25790685-9797-4cde-a530-94793b1245a0
ms.date: 12/05/2018
ms.keywords: IdnToNameprepUnicode, IdnToNameprepUnicode function [Internationalization for Windows Applications], _win32_IdnToNameprepUnicode, intl.idntonameprepunicode, winnls/IdnToNameprepUnicode
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
 - IdnToNameprepUnicode
 - winnls/IdnToNameprepUnicode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Normaliz.dll
 - API-MS-Win-Core-normalization-l1-1-0.dll
 - KernelBase.dll
api_name:
 - IdnToNameprepUnicode
---

# IdnToNameprepUnicode function


## -description

Converts an internationalized domain name (IDN) or another internationalized label to the NamePrep form specified by Network Working Group <a href="http://www.faqs.org/rfcs/rfc3491.html">RFC 3491</a>, but does not perform the additional conversion to Punycode. For more information and links to related draft standards, see <a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>.

## -parameters

### -param dwFlags [in]

Flags specifying conversion options. For detailed definitions, see the <i>dwFlags</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a>.

### -param lpUnicodeCharStr [in]

Pointer to a Unicode string representing an IDN or another internationalized label.

### -param cchUnicodeChar [in]

Count of Unicode characters in the input Unicode string indicated by <i>lpUnicodeCharStr</i>.

### -param lpNameprepCharStr [out, optional]

Pointer to a buffer that receives a version of the input Unicode string converted through NamePrep processing. Alternatively, the function can retrieve <b>NULL</b> for this parameter, if <i>cchNameprepChar</i> is set to 0. In this case, the function returns the size required for this buffer.

### -param cchNameprepChar [in]

Size, in characters, of the buffer indicated by <i>lpNameprepCharStr</i>. The application can set the size to 0 to retrieve <b>NULL</b> in <i>lpNameprepCharStr</i> and have the function return the required buffer size.

## -returns

Returns the number of characters retrieved in <i>lpNameprepCharStr</i> if successful. The retrieved string is null-terminated only if the input Unicode string is null-terminated.

If the function succeeds and the value of <i>cchNameprepChar</i> is 0, the function returns the required size, in characters including a terminating null character if it was part of the input buffer.

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
		


#### Examples


<a href="/windows/desktop/Intl/nls--internationalized-domain-name--idn--conversion-sample">NLS: Internationalized Domain Name (IDN) Conversion Sample</a> demonstrates the use of this function.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Intl/handling-internationalized-domain-names--idns">Handling Internationalized Domain Names (IDNs)</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntoascii">IdnToAscii</a>



<a href="/windows/desktop/api/winnls/nf-winnls-idntounicode">IdnToUnicode</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>