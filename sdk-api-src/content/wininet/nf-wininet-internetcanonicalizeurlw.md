---
UID: NF:wininet.InternetCanonicalizeUrlW
title: InternetCanonicalizeUrlW function
author: windows-driver-content
description: Canonicalizes a URL, which includes converting unsafe characters and spaces into escape sequences.
old-location: wininet\internetcanonicalizeurl.htm
old-project: WinInet
ms.assetid: 3bfde980-e478-4960-b41f-e1c8105ef419
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: InternetCanonicalizeUrl, InternetCanonicalizeUrl function [WinINet], InternetCanonicalizeUrlA, InternetCanonicalizeUrlW, _inet_internetcanonicalizeurl_function, wininet.internetcanonicalizeurl, wininet/InternetCanonicalizeUrl, wininet/InternetCanonicalizeUrlA, wininet/InternetCanonicalizeUrlW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetCanonicalizeUrlW (Unicode) and InternetCanonicalizeUrlA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	InternetCanonicalizeUrl
-	InternetCanonicalizeUrlA
-	InternetCanonicalizeUrlW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetCanonicalizeUrlW function


## -description


Canonicalizes a URL, which includes converting unsafe characters and spaces into escape sequences.


## -parameters




### -param lpszUrl [in]

 A pointer to the string that contains the URL to canonicalize.


### -param lpszBuffer [out]

A pointer to the buffer that receives the resulting canonicalized URL.


### -param lpdwBufferLength [in, out]

A pointer to a variable that contains the size, in characters,  of the 
<i>lpszBuffer</i> buffer. If the function succeeds, this parameter receives the number of characters actually copied to the 
<i>lpszBuffer</i> buffer, which does not include the terminating null character. If the function fails, this parameter receives the required size of the 
buffer, in characters, which includes the terminating null character.


### -param dwFlags [in]

Controls canonicalization. If no flags are specified, the function converts all unsafe characters and meta sequences (such as \.,\ .., and \...) to escape sequences. 
This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_BROWSER_MODE</dt>
</dl>
</td>
<td width="60%">
Does not encode or decode characters after "#" or "?", and does not remove trailing white space after "?". If this value is not specified, the entire URL is encoded and trailing white space is removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_DECODE</dt>
</dl>
</td>
<td width="60%">
Converts all %XX sequences to characters, including escape sequences, before the URL is parsed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_ENCODE_PERCENT</dt>
</dl>
</td>
<td width="60%">
Encodes any percent signs encountered. By default, percent signs are not encoded. This value is available in Microsoft Internet Explorer 5 and later.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_ENCODE_SPACES_ONLY</dt>
</dl>
</td>
<td width="60%">
Encodes spaces only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_NO_ENCODE</dt>
</dl>
</td>
<td width="60%">
Does not convert unsafe characters to escape sequences.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_NO_META</dt>
</dl>
</td>
<td width="60%">
Does not remove meta sequences (such as "." and "..") from the URL.

</td>
</tr>
</table>
 


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. Possible errors include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PATHNAME</b></dt>
</dl>
</td>
<td width="60%">
The URL could not be canonicalized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The canonicalized URL is too large to fit in the buffer provided. The 
<i>lpdwBufferLength</i> parameter is set to the size, in bytes, of the buffer required to hold the canonicalized URL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERNET_INVALID_URL</b></dt>
</dl>
</td>
<td width="60%">
The format of the URL is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
There is an invalid string, buffer, buffer size, or flags parameter.

</td>
</tr>
</table>
 




## -remarks



In Internet Explorer 4.0 and later, 
<b>InternetCanonicalizeUrl</b> always functions as if the <b>ICU_BROWSER_MODE</b> flag is set. Client applications that must canonicalize the entire URL should use either 
<a href="https://msdn.microsoft.com/25f9b097-ee42-48df-8573-d6bf9a52f53b">CoInternetParseUrl</a> (with the action <b>PARSE_CANONICALIZE</b> and the flag <b>URL_ESCAPE_UNSAFE</b>) or 
<a href="https://msdn.microsoft.com/70802745-0611-4d37-800e-b50d5ea23426">UrlCanonicalize</a>.

<b>InternetCanonicalizeUrl</b> always encodes by default, even if the <b>ICU_DECODE</b> flag has been specified. To decode without reencoding, use <b>ICU_DECODE</b> | <b>ICU_NO_ENCODE</b>. If the <b>ICU_DECODE</b> flag is used without <b>ICU_NO_ENCODE</b>, the URL is decoded before being parsed; unsafe characters are then  re-encoded after parsing. This function  handles arbitrary protocol schemes, but to do so it must make inferences from the unsafe character set.

Applications that call 
<b>InternetCanonicalizeUrl</b> when using  Internet Explorer 3.0 (or when setting the <b>ICU_ENCODE_PERCENT</b> flag for Internet Explorer 5 and later) should track the usage of this function on a particular URL. If unsafe characters in a URL have been converted to escape sequences, using 
<b>InternetCanonicalizeUrl</b> again on the URL (with no flags)  causes the escape sequences to be converted to another escape sequence. For example, a blank space in a URL would be converted to the escape sequence %20. Calling 
<b>InternetCanonicalizeUrl</b> again on the URL would cause the escape sequence %20 to be converted to the escape sequence %2520, because the % sign is an unsafe character that is reserved for escape sequences and is replaced by the function with the escape sequence %25.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bb59ada6-f49f-412c-a32c-4fb9495b1222">Handling Uniform Resource Locators</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

