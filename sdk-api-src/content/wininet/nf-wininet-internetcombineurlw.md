---
UID: NF:wininet.InternetCombineUrlW
title: InternetCombineUrlW function (wininet.h)
description: Combines a base and relative URL into a single URL. The resultant URL is canonicalized (see InternetCanonicalizeUrl). (Unicode)
helpviewer_keywords: ["InternetCombineUrl", "InternetCombineUrl function [WinINet]", "InternetCombineUrlW", "_inet_internetcombineurl_function", "wininet.internetcombineurl", "wininet/InternetCombineUrl", "wininet/InternetCombineUrlW"]
old-location: wininet\internetcombineurl.htm
tech.root: wininet
ms.assetid: 2efcf28a-e82b-47f2-8e8c-95fee70a87e4
ms.date: 12/05/2018
ms.keywords: InternetCombineUrl, InternetCombineUrl function [WinINet], InternetCombineUrlA, InternetCombineUrlW, _inet_internetcombineurl_function, wininet.internetcombineurl, wininet/InternetCombineUrl, wininet/InternetCombineUrlA, wininet/InternetCombineUrlW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetCombineUrlW (Unicode) and InternetCombineUrlA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetCombineUrlW
 - wininet/InternetCombineUrlW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetCombineUrl
 - InternetCombineUrlA
 - InternetCombineUrlW
---

# InternetCombineUrlW function


## -description

Combines a base and relative URL into a single URL. The resultant URL is canonicalized (see 
<a href="/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla">InternetCanonicalizeUrl</a>).

## -parameters

### -param lpszBaseUrl [in]

Pointer to a null-terminated string  that contains the base URL.

### -param lpszRelativeUrl [in]

Pointer to a null-terminated string  that contains the relative URL.

### -param lpszBuffer [out]

Pointer to a buffer that receives the combined URL.

### -param lpdwBufferLength [in, out]

Pointer to a variable that contains the size of the 
<i>lpszBuffer</i> buffer, in characters. If the function succeeds, this parameter receives the size of the combined URL, in characters, not including the null-terminating character. If the function fails, this parameter receives the size of the required buffer, in characters (including the null-terminating character).

### -param dwFlags [in]

Controls the operation of the function. This parameter can be one of the following values.

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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible errors include the following.

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
The URLs could not be combined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer supplied to the function was insufficient or <b>NULL</b>. The value indicated by the 
<i>lpdwBufferLength</i> parameter will contain the number of bytes required to hold the combined URL.

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

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetCombineUrl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/handling-uniform-resource-locators">Handling Uniform Resource Locators</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
