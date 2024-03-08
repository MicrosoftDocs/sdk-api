---
UID: NF:winhttp.WinHttpSendRequest
title: WinHttpSendRequest function (winhttp.h)
description: Sends the specified request to the HTTP server. (WinHttpSendRequest)
helpviewer_keywords: ["WinHttpSendRequest","WinHttpSendRequest function [WinHTTP]","http.winhttpsendrequest","winhttp.winhttpsendrequest_function","winhttp/WinHttpSendRequest"]
old-location: http\winhttpsendrequest.htm
tech.root: http
ms.assetid: 991bf531-2e6b-4581-8069-f75789915522
ms.date: 12/05/2018
ms.keywords: WinHttpSendRequest, WinHttpSendRequest function [WinHTTP], http.winhttpsendrequest, winhttp.winhttpsendrequest_function, winhttp/WinHttpSendRequest
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
 - WinHttpSendRequest
 - winhttp/WinHttpSendRequest
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
 - WinHttpSendRequest
---

# WinHttpSendRequest function


## -description

The <b>WinHttpSendRequest</b> function sends the specified request to the HTTP server.

## -parameters

### -param hRequest [in]

An <a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>.

### -param lpszHeaders [in, optional]

A pointer to a string  that contains the additional headers to append to the request. This parameter can be <b>WINHTTP_NO_ADDITIONAL_HEADERS</b> if there are no additional headers to append.

### -param dwHeadersLength [in]

An unsigned long integer value that contains the length, in characters, of the additional headers. If this parameter is <b>-1L</b> and 
<i>pwszHeaders</i> is not <b>NULL</b>, this function assumes that 
<i>pwszHeaders</i> is <b>null</b>-terminated, and the length is calculated.

### -param lpOptional [in, optional]

A pointer to a buffer that contains any optional data to send immediately after the request headers. This parameter is generally used for POST and PUT operations. The optional data can be the resource or data posted to the server. This parameter can be <b>WINHTTP_NO_REQUEST_DATA</b> if there is no optional data to send.

If the <i>dwOptionalLength</i> parameter is 0, this parameter is ignored and set to <b>NULL</b>.

This buffer must remain available until the request handle is closed or the call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> has completed.

### -param dwOptionalLength [in]

An unsigned long integer value that contains the length, in bytes, of the optional data. This parameter can be zero if there is no optional data to send.

This parameter must contain a valid length when the <i>lpOptional</i> parameter is not <b>NULL</b>. Otherwise, <i>lpOptional</i> is ignored and set to <b>NULL</b>.

### -param dwTotalLength [in]

An unsigned long integer value that contains the length, in bytes, of the total data sent.  This parameter specifies the Content-Length header of the request.  If the value of this parameter is greater than the length specified by 
<i>dwOptionalLength</i>, then 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwritedata">WinHttpWriteData</a> can be used to send additional data.

<i>dwTotalLength</i> must not change between calls to <b>WinHttpSendRequest</b> for the same request.  If <i>dwTotalLength</i> needs to be changed, the caller should create a new request.

### -param dwContext [in]

A pointer to a pointer-sized variable that contains an application-defined value that is passed, with the request handle, to any callback functions.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Error codes are listed in the following table.

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
<dt><b>ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
The secure HTTP server requires a client certificate. The application retrieves the list of certificate issuers by calling <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption">WinHttpQueryOption</a> with the <b>WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST</b> option.

If the server requests the client certificate, but does not require it, the application can alternately call <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption">WinHttpSetOption</a> with the <b>WINHTTP_OPTION_CLIENT_CERT_CONTEXT</b> option. In this case, the application specifies the WINHTTP_NO_CLIENT_CERT_CONTEXT macro in the <i>lpBuffer</i> parameter of <b>WinHttpSetOption</b>. For more information, see the <b>WINHTTP_OPTION_CLIENT_CERT_CONTEXT</b> option.<b>Windows Server 2003 with SP1, Windows XP with SP2 and Windows 2000:  </b>This error is not supported.



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
The server name cannot be resolved.

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
One or more errors were found in the Secure Sockets Layer (SSL) certificate sent by the server.  To determine what type of error was encountered, verify through a 
<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_CALLBACK_STATUS_SECURE_FAILURE</a> notification in a status callback function.  For more information, see 
<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The WinHTTP function support is shut down or unloaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The request timed out.

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

<b>Windows Server 2003, Windows XP and Windows 2000:  </b>The TCP reservation range set with the <b>WINHTTP_OPTION_PORT_RESERVATION</b> option is not large enough to send this request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The content length specified in the <i>dwTotalLength</i> parameter does not match the length specified in the Content-Length header.

The <i>lpOptional</i> parameter must be <b>NULL</b> and the <i>dwOptionalLength</i> parameter must be zero when the Transfer-Encoding header is present.

The Content-Length header cannot be present when the Transfer-Encoding header is present. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> ERROR_WINHTTP_RESEND_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
 The application must call <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a> again due to a redirect or authentication challenge.

<b>Windows Server 2003 with SP1, Windows XP with SP2 and Windows 2000:  </b>This error is not supported.

</td>
</tr>
</table>

## -remarks

Even when WinHTTP is used in asynchronous mode, that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>, this function can operate either synchronously or asynchronously.  In either case, if the request is sent successfully, the application is called back with the completion status set to <b>WINHTTP_CALLBACK_STATUS_SENDREQUEST_COMPLETE</b>. The <b>WINHTTP_CALLBACK_STATUS_REQUEST_ERROR</b> completion indicates that the operation completed asynchronously, but failed.  Upon receiving the <b>WINHTTP_CALLBACK_STATUS_SENDREQUEST_COMPLETE</b> status callback, the application can start to receive a response from the server with <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a>. Before then, no other asynchronous functions can be called, otherwise, <b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b> is returned. 

An application must not delete or alter the buffer pointed to by <i>lpOptional</i> until the request handle is closed or the call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> has completed, because an authentication challenge or redirect that required the optional data could be encountered in the course of receiving the response. If the operation must be aborted with <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>, the application must keep the buffer valid until it receives the callback  <b>WINHTTP_CALLBACK_STATUS_REQUEST_ERROR</b> with an <b>ERROR_WINHTTP_OPERATION_CANCELLED</b> error code.

If  WinHTTP  is used synchronously, that is, when <b>WINHTP_FLAG_ASYNC</b> was not set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>, an application is not called with a completion status even if a callback function is registered. While in this mode, the application can call <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a> when <b>WinHttpSendRequest</b> returns.

The 
<b>WinHttpSendRequest</b> function sends the specified request to the HTTP server and allows the client to specify additional headers to send along with the request.

This function also lets the client specify optional data to send to the HTTP server immediately following the request headers. This feature is generally used for write operations such as PUT and POST.

An application can use the same HTTP request handle in multiple calls to 
<b>WinHttpSendRequest</b> to re-send the same request, but the application must read all data returned from the previous call before calling this function again.

The name and value of request headers added with this function are validated.  Headers must be well formed.  For more information about valid HTTP headers, see 
<a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.  If an invalid header is used, this function fails and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
<a href="/windows/desktop/WinHttp/error-messages">ERROR_INVALID_PARAMETER</a>.  The invalid header is not added.

<b>Windows 2000:  </b>When sending requests from multiple threads, there may be a significant decrease in network and CPU performance.  

<b>Windows XP and Windows 2000:  </b>See <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a>.

<h3><a id="WinHttpSetStatusCallback"></a><a id="winhttpsetstatuscallback"></a><a id="WINHTTPSETSTATUSCALLBACK"></a>WinHttpSetStatusCallback</h3>
If a status callback function has been installed with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>, then those of the following notifications  that  have been set in the <i>dwNotificationFlags</i> parameter of <b>WinHttpSetStatusCallback</b>  indicate the progress in sending the request:

<ul>
<li>WINHTTP_CALLBACK_STATUS_DETECTING_PROXY (not implemented)</li>
<li>WINHTTP_CALLBACK_STATUS_SENDREQUEST_COMPLETE (only in asynchronous mode)</li>
<li>WINHTTP_CALLBACK_STATUS_REDIRECT</li>
<li>WINHTTP_CALLBACK_STATUS_SECURE_FAILURE</li>
<li>WINHTTP_CALLBACK_STATUS_INTERMEDIATE_RESPONSE</li>
</ul>
<div class="alert"><b>Note</b>  On Windows 7 and Windows Server 2008 R2, all of the following notifications are deprecated.</div>
<div> </div>
<ul>
<li>WINHTTP_CALLBACK_STATUS_RESOLVING_NAME</li>
<li>WINHTTP_CALLBACK_STATUS_NAME_RESOLVED</li>
<li>WINHTTP_CALLBACK_STATUS_CONNECTING_TO_SERVER</li>
<li>WINHTTP_CALLBACK_STATUS_CONNECTED_TO_SERVER</li>
<li>WINHTTP_CALLBACK_STATUS_SENDING_REQUEST</li>
<li>WINHTTP_CALLBACK_STATUS_REQUEST_SENT</li>
<li>WINHTTP_CALLBACK_STATUS_RECEIVING_RESPONSE</li>
<li>WINHTTP_CALLBACK_STATUS_RESPONSE_RECEIVED</li>
</ul>
If the server closes the connection, the following notifications are also sent, provided that they  have been set in the <i>dwNotificationFlags</i> parameter of <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>:

<ul>
<li>WINHTTP_CALLBACK_STATUS_CLOSING_CONNECTION</li>
<li>WINHTTP_CALLBACK_STATUS_CONNECTION_CLOSED</li>
</ul>
<h3><a id="Support_for_Greater_Than_4-GB_Upload"></a><a id="support_for_greater_than_4-gb_upload"></a><a id="SUPPORT_FOR_GREATER_THAN_4-GB_UPLOAD"></a>Support for Greater Than 4-GB Upload</h3>
Starting in Windows Vista and Windows Server 2008, WinHttp supports uploading files up to the size of a LARGE_INTEGER (2^64 bytes) using the Content-Length header. Payload lengths specified in the call to <b>WinHttpSendRequest</b> are limited to the size of a <b>DWORD</b> (2^32 bytes). To upload data to a URL larger than a <b>DWORD</b>, the application must provide the length in the Content-Length header of the request. In this case, the WinHttp client application calls <b>WinHttpSendRequest</b> with the <i>dwTotalLength</i> parameter set to <b>WINHTTP_IGNORE_REQUEST_TOTAL_LENGTH</b>.

If the Content-Length header specifies a length less than a 2^32, the application must also specify the content length in the call to <b>WinHttpSendRequest</b>. If the <i>dwTotalLength</i> parameter does not match the length specified in the Content-Length header, the call fails and returns <b>ERROR_INVALID_PARAMETER</b>.

The Content-Length header can be added in the call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpaddrequestheaders">WinHttpAddRequestHeaders</a>, or it can be specified in the <i>lpszHeader</i> parameter of <b>WinHttpSendRequest</b> as shown in the following code example.


``` syntax
BOOL fRet = WinHttpSendRequest(
			hReq,
			L"Content-Length: 68719476735\r\n",
			-1L,
			WINHTTP_NO_REQUEST_DATA,
			0,
			WINHTTP_IGNORE_REQUEST_TOTAL_LENGTH,
			pMyContent);
```

<h3><a id="Transfer-Encoding_Header"></a><a id="transfer-encoding_header"></a><a id="TRANSFER-ENCODING_HEADER"></a>Transfer-Encoding Header</h3>
Starting in Windows Vista and Windows Server 2008, WinHttp enables applications to perform chunked transfer encoding on data sent to the server. When the Transfer-Encoding header is present on the WinHttp request, the <i>dwTotalLength</i> parameter in the call to <b>WinHttpSendRequest</b> is set to <b>WINHTTP_IGNORE_REQUEST_TOTAL_LENGTH</b> and the application sends the entity body in one or more calls to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwritedata">WinHttpWriteData</a>. The <i>lpOptional</i> parameter of <b>WinHttpSendRequest</b> must be <b>NULL</b> and the <i>dwOptionLength</i> parameter must be zero, otherwise an <b>ERROR_WINHTTP_INVALID_PARAMETER</b> error is returned. To terminate the chunked data transfer, the application generates a zero length chunk and sends it in the last call to <b>WinHttpWriteData</b>.


#### Examples

The following code example shows how to obtain an 
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

    // Place additional code here.


    // Report errors.
    if (!bResults)
        printf("Error %d has occurred.\n",GetLastError());

    // Close open handles.
    if (hRequest) WinHttpCloseHandle(hRequest);
    if (hConnect) WinHttpCloseHandle(hConnect);
    if (hSession) WinHttpCloseHandle(hSession);

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<i>WINHTTP_STATUS_CALLBACK</i>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a>
