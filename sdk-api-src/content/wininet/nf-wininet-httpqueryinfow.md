---
UID: NF:wininet.HttpQueryInfoW
title: HttpQueryInfoW function (wininet.h)
description: Retrieves header information associated with an HTTP request. (Unicode)
helpviewer_keywords: ["HttpQueryInfo", "HttpQueryInfo function [WinINet]", "HttpQueryInfoW", "_inet_httpqueryinfo_function", "wininet.httpqueryinfo", "wininet/HttpQueryInfo", "wininet/HttpQueryInfoW"]
old-location: wininet\httpqueryinfo.htm
tech.root: wininet
ms.assetid: 5747ce19-5004-4eea-abe9-dd00abac1b3b
ms.date: 12/05/2018
ms.keywords: HttpQueryInfo, HttpQueryInfo function [WinINet], HttpQueryInfoA, HttpQueryInfoW, _inet_httpqueryinfo_function, wininet.httpqueryinfo, wininet/HttpQueryInfo, wininet/HttpQueryInfoA, wininet/HttpQueryInfoW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: HttpQueryInfoW (Unicode) and HttpQueryInfoA (ANSI)
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
 - HttpQueryInfoW
 - wininet/HttpQueryInfoW
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
 - HttpQueryInfo
 - HttpQueryInfoA
 - HttpQueryInfoW
---

# HttpQueryInfoW function


## -description

Retrieves header information associated with an HTTP request.

## -parameters

### -param hRequest [in]

A handle returned by 
a call to the <a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a> function.

### -param dwInfoLevel [in]

A combination of an attribute to be retrieved and flags that modify the request. For a list of possible attribute and modifier values, see 
<a href="/windows/desktop/WinInet/query-info-flags">Query Info Flags</a>.

### -param lpBuffer [in, out]

A pointer to a buffer to receive the requested information. This parameter must not be <b>NULL</b>.

### -param lpdwBufferLength [in, out]

A pointer to a variable that contains, on entry, the size in bytes of the buffer pointed to by <i>lpvBuffer</i>. 

When the function returns successfully, this variable contains the number of bytes of information written to the buffer. In the case of a string, the byte count does not include the string's terminating <b>null</b> character.

When the function  
					fails with an extended error code of <b>ERROR_INSUFFICIENT_BUFFER</b>, the variable pointed to by <i>lpdwBufferLength</i> contains on exit the size, in bytes, of a buffer large enough to receive the requested information. The calling application can then allocate a buffer of this size or larger, and call the function again.

### -param lpdwIndex [in, out]

A pointer to a zero-based header index used to enumerate multiple headers with the same name. When calling the function, this parameter is the index of the specified header to return. When the function returns, this parameter is the index of the next header. If the next index cannot be found, <b>ERROR_HTTP_HEADER_NOT_FOUND</b> is returned.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You can retrieve the following types of data from 
<b>HttpQueryInfo</b>:<ul>
<li>Strings (default)</li>
<li>
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> (for dates)</li>
<li><b>DWORD</b> (for <b>STATUS_CODE</b>, <b>CONTENT_LENGTH</b>, and so on, if <b>HTTP_QUERY_FLAG_NUMBER</b> has been used)</li>
</ul>


If your application requires that the data be returned as a data type other than a string, you must include the appropriate modifier with the attribute passed to 
<i>dwInfoLevel</i>.

The <b>HttpQueryInfo</b> function is available in Microsoft Internet Explorer 3.0 for ISO-8859-1 characters (<b>HttpQueryInfoA</b> function) and in Internet Explorer 4.0 or later for ISO-8859-1 characters (<b>HttpQueryInfoA</b> function)  and for ISO-8859-1  characters converted to UTF-16LE  characters.(the <b>HttpQueryInfoW</b> function). 

<div class="alert"><b>Note</b>  The <b>HttpQueryInfoA</b> function represents headers as ISO-8859-1 characters not ANSI characters. The <b>HttpQueryInfoW</b> function represents headers as ISO-8859-1 characters converted to UTF-16LE  characters.   As a result, it is never safe to use the <b>HttpQueryInfoW</b> function when the headers can contain non-ASCII characters.
Instead, an application can use the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a> functions with a <i>Codepage</i> parameter set to 28591 to map between ANSI characters and  UTF-16LE characters.
</div>
<div> </div>
See <a href="/windows/desktop/WinInet/retrieving-http-headers">Retrieving HTTP Headers</a> for an example code calling the <b>HttpQueryInfo</b> function.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines HttpQueryInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/http-sessions">HTTP Sessions</a>



<a href="/windows/desktop/WinInet/retrieving-http-headers">Retrieving HTTP Headers</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
