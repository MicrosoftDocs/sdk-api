---
UID: NF:wininet.HttpAddRequestHeadersA
title: HttpAddRequestHeadersA function (wininet.h)
description: Adds one or more HTTP request headers to the HTTP request handle. (HttpAddRequestHeadersA)
helpviewer_keywords: ["HTTP_ADDREQ_FLAG_ADD", "HTTP_ADDREQ_FLAG_ADD_IF_NEW", "HTTP_ADDREQ_FLAG_COALESCE", "HTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA", "HTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON", "HTTP_ADDREQ_FLAG_REPLACE", "HttpAddRequestHeadersA", "wininet/HttpAddRequestHeadersA"]
old-location: wininet\httpaddrequestheaders.htm
tech.root: wininet
ms.assetid: 636c3442-a2e6-4885-8fb4-1f6996ba6860
ms.date: 12/05/2018
ms.keywords: HTTP_ADDREQ_FLAG_ADD, HTTP_ADDREQ_FLAG_ADD_IF_NEW, HTTP_ADDREQ_FLAG_COALESCE, HTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA, HTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON, HTTP_ADDREQ_FLAG_REPLACE, HttpAddRequestHeaders, HttpAddRequestHeaders function [WinINet], HttpAddRequestHeadersA, HttpAddRequestHeadersW, _inet_httpaddrequestheaders_function, wininet.httpaddrequestheaders, wininet/HttpAddRequestHeaders, wininet/HttpAddRequestHeadersA, wininet/HttpAddRequestHeadersW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: HttpAddRequestHeadersW (Unicode) and HttpAddRequestHeadersA (ANSI)
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
 - HttpAddRequestHeadersA
 - wininet/HttpAddRequestHeadersA
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
 - HttpAddRequestHeaders
 - HttpAddRequestHeadersA
 - HttpAddRequestHeadersW
---

# HttpAddRequestHeadersA function


## -description

Adds one or more HTTP request headers to the HTTP request handle.

## -parameters

### -param hRequest [in]

A handle returned by a call to the 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> function.

### -param lpszHeaders [in]

A pointer to a string variable containing the headers to append to the request. Each header must be terminated by a CR/LF (carriage return/line feed) pair.

### -param dwHeadersLength [in]

The size of 
<i>lpszHeaders</i>, in <b>TCHARs</b>. If this parameter is -1L, the function assumes that 
<i>lpszHeaders</i> is zero-terminated (ASCIIZ), and the length is computed.

### -param dwModifiers [in]

A set of modifiers that control the semantics of this function. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_ADDREQ_FLAG_ADD"></a><a id="http_addreq_flag_add"></a><dl>
<dt><b>HTTP_ADDREQ_FLAG_ADD</b></dt>
</dl>
</td>
<td width="60%">
Adds the header if it does not exist. Used with <b>HTTP_ADDREQ_FLAG_REPLACE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_ADDREQ_FLAG_ADD_IF_NEW"></a><a id="http_addreq_flag_add_if_new"></a><dl>
<dt><b>HTTP_ADDREQ_FLAG_ADD_IF_NEW</b></dt>
</dl>
</td>
<td width="60%">
Adds the header only if it does not already exist; otherwise, an error is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_ADDREQ_FLAG_COALESCE"></a><a id="http_addreq_flag_coalesce"></a><dl>
<dt><b>HTTP_ADDREQ_FLAG_COALESCE</b></dt>
</dl>
</td>
<td width="60%">
Coalesces headers of the same name.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA"></a><a id="http_addreq_flag_coalesce_with_comma"></a><dl>
<dt><b>HTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA</b></dt>
</dl>
</td>
<td width="60%">
Coalesces headers of the same name. For example, adding "Accept: text/*" followed by "Accept: audio/*" with this flag results in the formation of the single header "Accept: text/*, audio/*". This causes the first header found to be coalesced. It is up to the calling application to ensure a cohesive scheme with respect to coalesced/separate headers.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON"></a><a id="http_addreq_flag_coalesce_with_semicolon"></a><dl>
<dt><b>HTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON</b></dt>
</dl>
</td>
<td width="60%">
Coalesces headers of the same name using a semicolon.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_ADDREQ_FLAG_REPLACE"></a><a id="http_addreq_flag_replace"></a><dl>
<dt><b>HTTP_ADDREQ_FLAG_REPLACE</b></dt>
</dl>
</td>
<td width="60%">
Replaces or removes a header. If the header value is empty and the header is found, it is removed. If not empty, the header value is replaced.

</td>
</tr>
</table>

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>HttpAddRequestHeaders</b> appends additional, free-format headers to the HTTP request handle and is intended for use by sophisticated clients that need detailed control over the exact request sent to the HTTP server.

Note that for basic 
<b>HttpAddRequestHeaders</b>, the application can pass in multiple headers in a single buffer. If the application is trying to remove or replace a header, only one header can be supplied in 
<i>lpszHeaders</i>.

<div class="alert"><b>Note</b>  The <b>HttpAddRequestHeadersA</b> function  represents headers as ISO-8859-1 characters not ANSI characters. The <b>HttpAddRequestHeadersW</b> function represents headers as ISO-8859-1 characters converted to UTF-16LE  characters.   As a result, it is never safe to use the <b>HttpAddRequestHeadersW</b> function when the headers to be added can contain non-ASCII characters.
Instead, an application can use the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a> functions with a <i>Codepage</i> parameter set to 28591 to map between ANSI characters and  UTF-16LE characters.
</div>
<div> </div>
Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines HttpAddRequestHeaders as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/http-sessions">HTTP Sessions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
