---
UID: NF:winhttp.WinHttpAddRequestHeaders
title: WinHttpAddRequestHeaders function (winhttp.h)
description: Adds one or more HTTP request headers to the HTTP request handle. (WinHttpAddRequestHeaders)
helpviewer_keywords: ["WINHTTP_ADDREQ_FLAG_ADD","WINHTTP_ADDREQ_FLAG_ADD_IF_NEW","WINHTTP_ADDREQ_FLAG_COALESCE","WINHTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA","WINHTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON","WINHTTP_ADDREQ_FLAG_REPLACE","WinHttpAddRequestHeaders","WinHttpAddRequestHeaders function [WinHTTP]","http.winhttpaddrequestheaders","winhttp/WinHttpAddRequestHeaders","winhttp_winhttpaddrequestheaders_function"]
old-location: http\winhttpaddrequestheaders.htm
tech.root: http
ms.assetid: 16cab68c-a802-43cc-87cd-60fcecb6a751
ms.date: 12/05/2018
ms.keywords: WINHTTP_ADDREQ_FLAG_ADD, WINHTTP_ADDREQ_FLAG_ADD_IF_NEW, WINHTTP_ADDREQ_FLAG_COALESCE, WINHTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA, WINHTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON, WINHTTP_ADDREQ_FLAG_REPLACE, WinHttpAddRequestHeaders, WinHttpAddRequestHeaders function [WinHTTP], http.winhttpaddrequestheaders, winhttp/WinHttpAddRequestHeaders, winhttp_winhttpaddrequestheaders_function
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
 - WinHttpAddRequestHeaders
 - winhttp/WinHttpAddRequestHeaders
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
 - WinHttpAddRequestHeaders
---

# WinHttpAddRequestHeaders function


## -description

The <b>WinHttpAddRequestHeaders</b> function adds one or more HTTP request headers to the HTTP request handle.

## -parameters

### -param hRequest [in]

A <a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by a call to the 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a> function.

### -param lpszHeaders [in]

A pointer to a string variable that contains the headers to append to the request. Each header except the last must be terminated by a carriage return/line feed (CR/LF).

### -param dwHeadersLength [in]

An unsigned long integer value that contains the length, in characters, of 
<i>pwszHeaders</i>. If this parameter is -1L, the function assumes that 
<i>pwszHeaders</i> is zero-terminated (ASCIIZ), and the length is computed.

### -param dwModifiers [in]

An unsigned long integer value that contains the flags used to modify the semantics of this function. Can be one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_ADD"></a><a id="winhttp_addreq_flag_add"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_ADD</b></dt>
</dl>
</td>
<td width="60%">
Adds the header if it does not exist. Used with 
<b>WINHTTP_ADDREQ_FLAG_REPLACE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_ADD_IF_NEW"></a><a id="winhttp_addreq_flag_add_if_new"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_ADD_IF_NEW</b></dt>
</dl>
</td>
<td width="60%">
Adds the header only if it does not already exist; otherwise, an error is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_COALESCE"></a><a id="winhttp_addreq_flag_coalesce"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_COALESCE</b></dt>
</dl>
</td>
<td width="60%">
Merges headers of the same name.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA"></a><a id="winhttp_addreq_flag_coalesce_with_comma"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_COALESCE_WITH_COMMA</b></dt>
</dl>
</td>
<td width="60%">
Merges headers of the same name using a comma. For example, adding "Accept: text/*" followed by "Accept: audio/*" with this flag results in a single header "Accept: text/*, audio/*". This causes the first header found to be merged. The calling application must  to ensure a cohesive scheme with respect to merged and separate headers.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON"></a><a id="winhttp_addreq_flag_coalesce_with_semicolon"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_COALESCE_WITH_SEMICOLON</b></dt>
</dl>
</td>
<td width="60%">
Merges headers of the same name using a semicolon.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_ADDREQ_FLAG_REPLACE"></a><a id="winhttp_addreq_flag_replace"></a><dl>
<dt><b>WINHTTP_ADDREQ_FLAG_REPLACE</b></dt>
</dl>
</td>
<td width="60%">
Replaces or removes a header. If the header value is empty and the header is found, it is removed. If the value is not empty, it is replaced.

</td>
</tr>
</table>

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned are the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The requested operation cannot be performed because the handle supplied is not in the correct state.

</td>
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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation.

</td>
</tr>
</table>

## -remarks

Headers are transferred across redirects. This can be a security issue. To avoid having headers transferred when a redirect occurs, use the  <a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a> callback to correct the specific headers when a  redirect occurs.

Even when WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The 
<b>WinHttpAddRequestHeaders</b> function appends additional free-format headers to the HTTP request handle and is intended for use by sophisticated clients that require detailed control over the exact request sent to the HTTP server.

The name and value of request headers added with this function are validated.  Headers must be well formed. For more information about valid HTTP headers, see 
<a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.  If an invalid header is used, this function fails and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
<a href="/windows/desktop/WinHttp/error-messages">ERROR_INVALID_PARAMETER</a>.  The invalid header is not added.

If you are sending a Date: request header, you can use the <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttptimefromsystemtime">WinHttpTimeFromSystemTime</a> function to create structure for the header.

For basic 
<b>WinHttpAddRequestHeaders</b>, the application can pass in multiple headers in a single buffer. 

An application can also use 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a> to add additional headers to the HTTP request handle before sending a request.

<div class="alert"><b>Note</b>  For more information, see <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a>.</div>
<div> </div>

#### Examples

The following code example includes an If-Modified-Since header in a request.  The response header is interpreted to determine whether the target document has been updated.


```cpp

  DWORD dwSize = sizeof(DWORD);
  DWORD dwStatusCode = 0;
  BOOL  bResults = FALSE;
  HINTERNET hSession = NULL,
        hConnect = NULL,
        hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"A WinHTTP Example Program/1.0", 
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS,
                          0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession,
                               L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTP_PORT,
                               0 );

  // Create an HTTP Request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect,
                                   L"GET",
                                   NULL, 
                                   NULL,
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   0 );

  // Add a request header.
  if( hRequest )
    bResults = WinHttpAddRequestHeaders( hRequest, 
                 L"If-Modified-Since: Mon, 20 Nov 2000 20:00:00 GMT",
                                         (ULONG)-1L,
                                         WINHTTP_ADDREQ_FLAG_ADD );

  // Send a Request.
  if( bResults ) 
    bResults = WinHttpSendRequest( hRequest, 
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0,
                                   0 );

  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL);

  // Use WinHttpQueryHeaders to obtain the header buffer.
  if( bResults )
    bResults = WinHttpQueryHeaders( hRequest, 
                WINHTTP_QUERY_STATUS_CODE | WINHTTP_QUERY_FLAG_NUMBER,
                                    NULL, 
                                    &dwStatusCode,
                                    &dwSize,
                                    WINHTTP_NO_HEADER_INDEX );

  // Based on the status code, determine whether 
  // the document was recently updated.
  if( bResults )
  {
    if( dwStatusCode == 304 ) 
      printf( "Document has not been updated.\n" );
    else if( dwStatusCode == 200 ) 
      printf( "Document has been updated.\n" );
    else 
      printf( "Status code = %u.\n",dwStatusCode );
  }

  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>
