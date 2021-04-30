---
UID: NF:winhttp.WinHttpReceiveResponse
title: WinHttpReceiveResponse function (winhttp.h)
description: The WinHttpReceiveResponse function waits to receive the response to an HTTP request initiated by WinHttpSendRequest.
helpviewer_keywords: ["WinHttpReceiveResponse","WinHttpReceiveResponse function [WinHTTP]","http.winhttpreceiveresponse","winhttp.winhttpreceiveresponse_function","winhttp/WinHttpReceiveResponse"]
old-location: http\winhttpreceiveresponse.htm
tech.root: http
ms.assetid: 0b79e73b-9f6a-42eb-9108-1ba142ad7c48
ms.date: 12/05/2018
ms.keywords: WinHttpReceiveResponse, WinHttpReceiveResponse function [WinHTTP], http.winhttpreceiveresponse, winhttp.winhttpreceiveresponse_function, winhttp/WinHttpReceiveResponse
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
 - WinHttpReceiveResponse
 - winhttp/WinHttpReceiveResponse
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
 - WinHttpReceiveResponse
---

# WinHttpReceiveResponse function


## -description

The <b>WinHttpReceiveResponse</b> function waits to receive the response to an HTTP request initiated by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>. When <b>WinHttpReceiveResponse</b> completes successfully, the status code and response headers have been received and are available for the application to inspect using <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryheaders">WinHttpQueryHeaders</a>. An application must call <b>WinHttpReceiveResponse</b> before it can use <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpquerydataavailable">WinHttpQueryDataAvailable</a> and <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a> to access the response entity body (if any).

## -parameters

### -param hRequest [in]

<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a> and sent by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>.  Wait until <b>WinHttpSendRequest</b> has completed for this handle before calling  <b>WinHttpReceiveResponse</b>.

### -param lpReserved [in]

This parameter is reserved and must be <b>NULL</b>.

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
<dt><b>ERROR_WINHTTP_CANNOT_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
Returned if  connection to the server failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
Returned when an overflow condition is encountered in the course of parsing chunked encoding.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
Returned when the server requests client authentication.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_CONNECTION_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered. For example, WinHTTP version 5.1 does not support SSL2 unless the client specifically enables it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_HEADER_COUNT_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
Returned when a larger number of headers were present in a response than WinHTTP could receive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_HEADER_SIZE_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
Returned by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> when the size of headers received  exceeds the limit for the request handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The requested operation cannot be carried out because the handle supplied is not in the correct state.

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
<dt><b>ERROR_WINHTTP_INVALID_SERVER_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
The server response could not be parsed.

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
<dt><b>ERROR_WINHTTP_LOGIN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The login attempt failed.  When this error is encountered, the request handle should be closed with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>.  A new request handle must be created before retrying the function that originally produced this error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_NAME_NOT_RESOLVED</b></dt>
</dl>
</td>
<td width="60%">
The server name could not be resolved.

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
<dt><b>ERROR_WINHTTP_REDIRECT_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The redirection failed because either the scheme changed or all attempts made to redirect failed (default is five attempts).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_RESEND_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The WinHTTP function failed.  The desired function can be retried on the same request handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
Returned when an incoming response exceeds an internal WinHTTP size limit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_SECURE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
One or more errors were found in the Secure Sockets Layer (SSL) certificate sent by the server.  To determine what type of error was encountered, check for a 
<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_CALLBACK_STATUS_SECURE_FAILURE</a> notification in a status callback function.  For more information, see 
<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The request has timed out.

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

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function can operate either synchronously or asynchronously.  If this function returns <b>FALSE</b>, this function failed and you can call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information. If this function returns <b>TRUE</b>, the application should expect either the <b>WINHTTP_CALLBACK_STATUS_HEADERS_AVAILABLE</b> completion callback, indicating success, or the <b>WINHTTP_CALLBACK_STATUS_REQUEST_ERROR</b> completion callback, indicating that the operation completed asynchronously, but failed.

If a status callback function has been installed with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>, then those of the following notifications  that  have been set in the <i>dwNotificationFlags</i> parameter of <b>WinHttpSetStatusCallback</b> indicate progress in receiving the response:

<ul>
<li>WINHTTP_CALLBACK_STATUS_RECEIVING_RESPONSE </li>
<li>WINHTTP_CALLBACK_STATUS_RESPONSE_RECEIVED</li>
<li>WINHTTP_CALLBACK_STATUS_HEADERS_AVAILABLE</li>
<li>WINHTTP_CALLBACK_STATUS_INTERMEDIATE_RESPONSE </li>
<li>WINHTTP_CALLBACK_STATUS_REDIRECT</li>
</ul>
If the server closes the connection, the following notifications will also be reported, provided that they have been set in the <i>dwNotificationFlags</i> parameter of <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>:

<ul>
<li>WINHTTP_CALLBACK_STATUS_CLOSING_CONNECTION</li>
<li>WINHTTP_CALLBACK_STATUS_CONNECTION_CLOSED</li>
</ul>
<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

This example shows code that  writes data to an HTTP server.  The server name supplied in the example, www.wingtiptoys.com, is fictitious and must be replaced with the name of a server for which you have write access.


```cpp
    LPSTR pszData = "WinHttpWriteData Example";
    DWORD dwBytesWritten = 0;
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
                                       (DWORD)strlen(pszData), 0);

    // Write data to the server.
    if (bResults)
        bResults = WinHttpWriteData( hRequest, pszData, 
                                     (DWORD)strlen(pszData), 
                                     &dwBytesWritten);

    // End the request.
    if (bResults)
        bResults = WinHttpReceiveResponse( hRequest, NULL);

    // Report any errors.
    if (!bResults)
        printf("Error %d has occurred.\n",GetLastError());


    // Close any open handles.
    if (hRequest) WinHttpCloseHandle(hRequest);
    if (hConnect) WinHttpCloseHandle(hConnect);
    if (hSession) WinHttpCloseHandle(hSession);

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>