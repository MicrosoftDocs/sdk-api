---
UID: NF:winhttp.WinHttpOpenRequest
title: WinHttpOpenRequest function (winhttp.h)
description: The WinHttpOpenRequest function creates an HTTP request handle.
helpviewer_keywords: ["WINHTTP_FLAG_BYPASS_PROXY_CACHE","WINHTTP_FLAG_ESCAPE_DISABLE","WINHTTP_FLAG_ESCAPE_DISABLE_QUERY","WINHTTP_FLAG_ESCAPE_PERCENT","WINHTTP_FLAG_NULL_CODEPAGE","WINHTTP_FLAG_REFRESH","WINHTTP_FLAG_SECURE","WinHttpOpenRequest","WinHttpOpenRequest function [WinHTTP]","http.winhttpopenrequest","winhttp.winhttpopenrequest_function","winhttp/WinHttpOpenRequest"]
old-location: http\winhttpopenrequest.htm
tech.root: http
ms.assetid: 9ecd035d-1abf-48ca-baf2-d9754f912c60
ms.date: 12/05/2018
ms.keywords: WINHTTP_FLAG_BYPASS_PROXY_CACHE, WINHTTP_FLAG_ESCAPE_DISABLE, WINHTTP_FLAG_ESCAPE_DISABLE_QUERY, WINHTTP_FLAG_ESCAPE_PERCENT, WINHTTP_FLAG_NULL_CODEPAGE, WINHTTP_FLAG_REFRESH, WINHTTP_FLAG_SECURE, WinHttpOpenRequest, WinHttpOpenRequest function [WinHTTP], http.winhttpopenrequest, winhttp.winhttpopenrequest_function, winhttp/WinHttpOpenRequest
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - WinHttpOpenRequest
 - winhttp/WinHttpOpenRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpOpenRequest
---

# WinHttpOpenRequest function


## -description

The <b>WinHttpOpenRequest</b> function creates an HTTP request handle.

## -parameters

### -param hConnect [in]

<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> connection handle to an HTTP session returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>.

### -param pwszVerb [in]

Pointer to a string that contains the <a href="/windows/desktop/WinHttp/glossary">HTTP verb</a> to use in the request. If this parameter is <b>NULL</b>, the function uses GET as the <i>HTTP verb</i>. <b>Note</b>  This string should be all uppercase. Many servers treat HTTP verbs as case-sensitive, and the Internet Engineering Task Force (IETF)  Requests for Comments (RFCs) spell these verbs using uppercase characters only.

### -param pwszObjectName [in]

Pointer to a <b>null</b>-terminated string that contains the name of the target resource of the specified HTTP verb. This is generally a file name, an executable module, or a search specifier.

### -param pwszVersion [in]

Pointer to a string that contains the HTTP version. If this parameter is <b>NULL</b>, the function uses HTTP/1.1.

### -param pwszReferrer [in]

Pointer to a string that specifies the URL of the document from which the URL in the request 
<i>pwszObjectName</i> was obtained. If this parameter is set to <b>WINHTTP_NO_REFERER</b>, no referring document is specified.

### -param ppwszAcceptTypes [in]

Pointer to a <b>null</b>-terminated array of string pointers that specifies media types accepted by the client. If this parameter is set to <b>WINHTTP_DEFAULT_ACCEPT_TYPES</b>, no types are accepted by the client. Typically, servers handle a lack of accepted types as indication that the client accepts only documents of type "text/*"; that is, only text documents—no pictures or other binary files. For a list of valid media types, see Media Types defined by IANA at http://www.iana.org/assignments/media-types/.

### -param dwFlags [in]

Unsigned long integer value that contains the Internet flag values. This can be one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_FLAG_BYPASS_PROXY_CACHE"></a><a id="winhttp_flag_bypass_proxy_cache"></a><dl>
<dt><b>WINHTTP_FLAG_BYPASS_PROXY_CACHE</b></dt>
</dl>
</td>
<td width="60%">
This flag provides the same behavior as 
<b>WINHTTP_FLAG_REFRESH</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_FLAG_ESCAPE_DISABLE"></a><a id="winhttp_flag_escape_disable"></a><dl>
<dt><b>WINHTTP_FLAG_ESCAPE_DISABLE</b></dt>
</dl>
</td>
<td width="60%">
Unsafe characters in the URL passed in for 
<i>pwszObjectName</i> are not converted to escape sequences.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_FLAG_ESCAPE_DISABLE_QUERY"></a><a id="winhttp_flag_escape_disable_query"></a><dl>
<dt><b>WINHTTP_FLAG_ESCAPE_DISABLE_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Unsafe characters in the query component of the URL passed in for 
<i>pwszObjectName</i> are not converted to escape sequences.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_FLAG_ESCAPE_PERCENT"></a><a id="winhttp_flag_escape_percent"></a><dl>
<dt><b>WINHTTP_FLAG_ESCAPE_PERCENT</b></dt>
</dl>
</td>
<td width="60%">
The string passed in for 
<i>pwszObjectName</i> is converted from an <b>LPCWSTR</b> to an <b>LPSTR</b>.  All unsafe characters are converted to an escape sequence including the percent symbol.  By default, all unsafe characters except the percent symbol are converted to an escape sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_FLAG_NULL_CODEPAGE"></a><a id="winhttp_flag_null_codepage"></a><dl>
<dt><b>WINHTTP_FLAG_NULL_CODEPAGE</b></dt>
</dl>
</td>
<td width="60%">
The string passed in for 
<i>pwszObjectName</i> is assumed to consist of valid ANSI characters represented by <b>WCHAR</b>.  No check are done for unsafe characters.


<b>Windows 7:  </b>This option is obsolete.





</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_FLAG_REFRESH"></a><a id="winhttp_flag_refresh"></a><dl>
<dt><b>WINHTTP_FLAG_REFRESH</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the request should be forwarded to the originating server rather than sending a cached version of a resource from a proxy server.  When this flag is used, a "Pragma: no-cache" header is added to the request handle.  When creating an HTTP/1.1 request header, a "Cache-Control: no-cache" is also added.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_FLAG_SECURE"></a><a id="winhttp_flag_secure"></a><dl>
<dt><b>WINHTTP_FLAG_SECURE</b></dt>
</dl>
</td>
<td width="60%">
Uses secure transaction semantics. This translates to using Secure Sockets Layer (SSL)/Transport Layer Security (TLS).

</td>
</tr>
</table>

## -returns

Returns a valid HTTP request handle if successful, or <b>NULL</b> if not. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of handle supplied is incorrect for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INVALID_URL</b></dt>
</dl>
</td>
<td width="60%">
The URL is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_OPERATION_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_UNRECOGNIZED_SCHEME</b></dt>
</dl>
</td>
<td width="60%">
The URL specified a scheme other than "http:" or "https:".

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The 
<b>WinHttpOpenRequest</b> function creates a new HTTP request handle and stores the specified parameters in that handle. An HTTP request handle holds a request to send to an HTTP server and contains all <a href="https://www.ietf.org/rfc/rfc0822.txt">RFC822</a>/MIME/HTTP headers to be sent as part of the request.

If 
<i>pwszVerb</i> is set to "HEAD", the Content-Length header is ignored.

If a status callback function has been installed with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>, then a <b>WINHTTP_CALLBACK_STATUS_HANDLE_CREATED</b> notification indicates that 
<b>WinHttpOpenRequest</b> has created a request handle.

After the calling application finishes using the 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<b>WinHttpOpenRequest</b>, it must be closed using the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a> function.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

This example shows how to obtain an 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle, open an HTTP
                session, create a request header, and send that header to the server.


```cpp

    BOOL  bResults = FALSE;
    HINTERNET hSession = NULL,
              hConnect = NULL,
              hRequest = NULL;

    // Use WinHttpOpen to obtain a session handle.
    hSession = WinHttpOpen(  L"A WinHTTP Example Program/1.0", 
                             WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                             WINHTTP_NO_PROXY_NAME, 
                             WINHTTP_NO_PROXY_BYPASS, 0);

    // Specify an HTTP server.
    if (hSession)
        hConnect = WinHttpConnect( hSession, L"www.wingtiptoys.com",
                                   INTERNET_DEFAULT_HTTP_PORT, 0);

    // Create an HTTP Request handle.
    if (hConnect)
        hRequest = WinHttpOpenRequest( hConnect, L"PUT", 
                                       L"/writetst.txt", 
                                       NULL, WINHTTP_NO_REFERER, 
                                       WINHTTP_DEFAULT_ACCEPT_TYPES,
                                       0);

    // Send a Request.
    if (hRequest) 
        bResults = WinHttpSendRequest( hRequest, 
                                       WINHTTP_NO_ADDITIONAL_HEADERS,
                                       0, WINHTTP_NO_REQUEST_DATA, 0, 
                                       0, 0);

    // PLACE ADDITIONAL CODE HERE.

    // Report any errors.
    if (!bResults)
        printf( "Error %d has occurred.\n", GetLastError());

    // Close any open handles.
    if (hRequest) WinHttpCloseHandle(hRequest);
    if (hConnect) WinHttpCloseHandle(hConnect);
    if (hSession) WinHttpCloseHandle(hSession);

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>
