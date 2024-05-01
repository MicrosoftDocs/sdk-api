---
UID: NC:winhttp.WINHTTP_STATUS_CALLBACK
title: WINHTTP_STATUS_CALLBACK (winhttp.h)
description: Represents an application-defined status callback function.
helpviewer_keywords: ["WINHTTP_CALLBACK_STATUS_CLOSE_COMPLETE","WINHTTP_CALLBACK_STATUS_CLOSING_CONNECTION","WINHTTP_CALLBACK_STATUS_CONNECTED_TO_SERVER","WINHTTP_CALLBACK_STATUS_CONNECTING_TO_SERVER","WINHTTP_CALLBACK_STATUS_CONNECTION_CLOSED","WINHTTP_CALLBACK_STATUS_DATA_AVAILABLE","WINHTTP_CALLBACK_STATUS_FLAG_CERT_CN_INVALID","WINHTTP_CALLBACK_STATUS_FLAG_CERT_DATE_INVALID","WINHTTP_CALLBACK_STATUS_FLAG_CERT_REVOKED","WINHTTP_CALLBACK_STATUS_FLAG_CERT_REV_FAILED","WINHTTP_CALLBACK_STATUS_FLAG_INVALID_CA","WINHTTP_CALLBACK_STATUS_FLAG_INVALID_CERT","WINHTTP_CALLBACK_STATUS_FLAG_SECURITY_CHANNEL_ERROR","WINHTTP_CALLBACK_STATUS_GETPROXYFORURL_COMPLETE","WINHTTP_CALLBACK_STATUS_HANDLE_CLOSING","WINHTTP_CALLBACK_STATUS_HANDLE_CREATED","WINHTTP_CALLBACK_STATUS_HEADERS_AVAILABLE","WINHTTP_CALLBACK_STATUS_INTERMEDIATE_RESPONSE","WINHTTP_CALLBACK_STATUS_NAME_RESOLVED","WINHTTP_CALLBACK_STATUS_READ_COMPLETE","WINHTTP_CALLBACK_STATUS_RECEIVING_RESPONSE","WINHTTP_CALLBACK_STATUS_REDIRECT","WINHTTP_CALLBACK_STATUS_REQUEST_ERROR","WINHTTP_CALLBACK_STATUS_REQUEST_SENT","WINHTTP_CALLBACK_STATUS_RESOLVING_NAME","WINHTTP_CALLBACK_STATUS_RESPONSE_RECEIVED","WINHTTP_CALLBACK_STATUS_SECURE_FAILURE","WINHTTP_CALLBACK_STATUS_SENDING_REQUEST","WINHTTP_CALLBACK_STATUS_SENDREQUEST_COMPLETE","WINHTTP_CALLBACK_STATUS_SHUTDOWN_COMPLETE","WINHTTP_CALLBACK_STATUS_WRITE_COMPLETE","WINHTTP_STATUS_CALLBACK","WINHTTP_STATUS_CALLBACK callback","WINHTTP_STATUS_CALLBACK callback function [HTTP]","http.internet_status_callback_prototype","winhttp/WINHTTP_STATUS_CALLBACK","winhttp_internet_status_callback_prototype"]
old-location: http\internet_status_callback_prototype.htm
tech.root: http
ms.assetid: 4d828e41-9073-407a-aab5-531f1d6d6d02
ms.date: 12/05/2018
ms.keywords: WINHTTP_CALLBACK_STATUS_CLOSE_COMPLETE, WINHTTP_CALLBACK_STATUS_CLOSING_CONNECTION, WINHTTP_CALLBACK_STATUS_CONNECTED_TO_SERVER, WINHTTP_CALLBACK_STATUS_CONNECTING_TO_SERVER, WINHTTP_CALLBACK_STATUS_CONNECTION_CLOSED, WINHTTP_CALLBACK_STATUS_DATA_AVAILABLE, WINHTTP_CALLBACK_STATUS_FLAG_CERT_CN_INVALID, WINHTTP_CALLBACK_STATUS_FLAG_CERT_DATE_INVALID, WINHTTP_CALLBACK_STATUS_FLAG_CERT_REVOKED, WINHTTP_CALLBACK_STATUS_FLAG_CERT_REV_FAILED, WINHTTP_CALLBACK_STATUS_FLAG_INVALID_CA, WINHTTP_CALLBACK_STATUS_FLAG_INVALID_CERT, WINHTTP_CALLBACK_STATUS_FLAG_SECURITY_CHANNEL_ERROR, WINHTTP_CALLBACK_STATUS_GETPROXYFORURL_COMPLETE, WINHTTP_CALLBACK_STATUS_HANDLE_CLOSING, WINHTTP_CALLBACK_STATUS_HANDLE_CREATED, WINHTTP_CALLBACK_STATUS_HEADERS_AVAILABLE, WINHTTP_CALLBACK_STATUS_INTERMEDIATE_RESPONSE, WINHTTP_CALLBACK_STATUS_NAME_RESOLVED, WINHTTP_CALLBACK_STATUS_READ_COMPLETE, WINHTTP_CALLBACK_STATUS_RECEIVING_RESPONSE, WINHTTP_CALLBACK_STATUS_REDIRECT, WINHTTP_CALLBACK_STATUS_REQUEST_ERROR, WINHTTP_CALLBACK_STATUS_REQUEST_SENT, WINHTTP_CALLBACK_STATUS_RESOLVING_NAME, WINHTTP_CALLBACK_STATUS_RESPONSE_RECEIVED, WINHTTP_CALLBACK_STATUS_SECURE_FAILURE, WINHTTP_CALLBACK_STATUS_SENDING_REQUEST, WINHTTP_CALLBACK_STATUS_SENDREQUEST_COMPLETE, WINHTTP_CALLBACK_STATUS_SHUTDOWN_COMPLETE, WINHTTP_CALLBACK_STATUS_WRITE_COMPLETE, WINHTTP_STATUS_CALLBACK, WINHTTP_STATUS_CALLBACK callback, WINHTTP_STATUS_CALLBACK callback function [HTTP], http.internet_status_callback_prototype, winhttp/WINHTTP_STATUS_CALLBACK, winhttp_internet_status_callback_prototype
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - WINHTTP_STATUS_CALLBACK
 - winhttp/WINHTTP_STATUS_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_STATUS_CALLBACK
---

# WINHTTP_STATUS_CALLBACK callback function


## -description

The <b>WINHTTP_STATUS_CALLBACK</b> type represents an application-defined status callback function.

## -parameters

### -param hInternet [in]

The handle for which the callback function is called.

### -param dwContext [in]

A pointer to a <b>DWORD</b> that specifies the application-defined context value associated with the handle in the 
<i>hInternet</i> parameter.

A context value can be assigned to a Session, Connect, or Request handle by calling <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption">WinHttpSetOption</a>  with the  <a href="/windows/desktop/WinHttp/option-flags">WINHTTP_OPTION_CONTEXT_VALUE</a> option. Alternatively, <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a> can be used to associate a context value with a Request handle.

### -param dwInternetStatus [in]

Points to a <b>DWORD</b> that specifies the status code that indicates why the callback function is called. This can be one of the following values:



#### WINHTTP_CALLBACK_STATUS_CLOSING_CONNECTION

Closing the connection to the server. The 
<i>lpvStatusInformation</i> parameter is <b>NULL</b>. 



#### WINHTTP_CALLBACK_STATUS_CONNECTED_TO_SERVER

Successfully connected to the server. The 
<i>lpvStatusInformation</i> parameter contains a pointer to an <b>LPWSTR</b> that indicates the IP address of the server in dotted notation.



#### WINHTTP_CALLBACK_STATUS_CONNECTING_TO_SERVER

Connecting to the server. The 
<i>lpvStatusInformation</i> parameter contains a pointer to an <b>LPWSTR</b> that indicates the IP address of the server in dotted notation. 



#### WINHTTP_CALLBACK_STATUS_CONNECTION_CLOSED

Successfully closed the connection to the server. The 
<i>lpvStatusInformation</i> parameter is <b>NULL</b>. 



#### WINHTTP_CALLBACK_STATUS_DATA_AVAILABLE

Data is available to be retrieved with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a>.   The <i>lpvStatusInformation</i> parameter points to a <b>DWORD</b> that contains the number of bytes of data  available. The <i>dwStatusInformationLength</i> 
 parameter itself is  4 (the size of a <b>DWORD</b>).



#### WINHTTP_CALLBACK_STATUS_HANDLE_CREATED

An 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle has been created.   The 
<i>lpvStatusInformation</i> parameter contains a pointer to the 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle.



#### WINHTTP_CALLBACK_STATUS_HANDLE_CLOSING

This handle value has been terminated. The 
<i>lpvStatusInformation</i> parameter contains a pointer to the 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle.  There will be no more callbacks for this handle.



#### WINHTTP_CALLBACK_STATUS_HEADERS_AVAILABLE

The response header has been received and is available with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryheaders">WinHttpQueryHeaders</a>. The 
<i>lpvStatusInformation</i> parameter is <b>NULL</b>.



#### WINHTTP_CALLBACK_STATUS_INTERMEDIATE_RESPONSE

Received an intermediate (100 level) status code message from the server.  The 
<i>lpvStatusInformation</i> parameter contains a pointer to a <b>DWORD</b> that indicates the status code.



#### WINHTTP_CALLBACK_STATUS_NAME_RESOLVED

Successfully found the IP address of the server.   The 
<i>lpvStatusInformation</i> parameter contains a pointer to a <b>LPWSTR</b> that indicates the name that was resolved.



#### WINHTTP_CALLBACK_STATUS_READ_COMPLETE

Data was successfully read from the server.  The 
<i>lpvStatusInformation</i> parameter contains a pointer to the buffer specified in the call to 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a>. The 
<i>dwStatusInformationLength</i> parameter contains the number of bytes read.

When used by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive">WinHttpWebSocketReceive</a>, the 
<i>lpvStatusInformation</i> parameter contains a pointer to a <a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status">WINHTTP_WEB_SOCKET_STATUS</a> structure, and the 
<i>dwStatusInformationLength</i> parameter  indicates the size of <i>lpvStatusInformation</i>.



#### WINHTTP_CALLBACK_STATUS_RECEIVING_RESPONSE

Waiting for the server to respond to a request. The 
<i>lpvStatusInformation</i> parameter is <b>NULL</b>. 



#### WINHTTP_CALLBACK_STATUS_REDIRECT

An HTTP request is about to automatically redirect the request. The 
<i>lpvStatusInformation</i> parameter contains a pointer to an <b>LPWSTR</b> indicating the new URL. At this point, the application can read any data returned by the server with the redirect response and can query the response headers. It can also cancel the operation by closing the handle.



#### WINHTTP_CALLBACK_STATUS_REQUEST_ERROR

An error occurred while sending an HTTP request.  The 
<i>lpvStatusInformation</i> parameter contains a pointer to a 
<a href="/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result">WINHTTP_ASYNC_RESULT</a> structure. Its <b>dwResult</b> member indicates the ID of the called function and <b>dwError</b> indicates the return value.



#### WINHTTP_CALLBACK_STATUS_REQUEST_SENT

Successfully sent the information request to the server. The 
<i>lpvStatusInformation</i> parameter contains a pointer to a <b>DWORD</b> indicating the number of bytes sent. 



#### WINHTTP_CALLBACK_STATUS_RESOLVING_NAME

Looking up the IP address of a server name. The 
<i>lpvStatusInformation</i> parameter contains a pointer to the server name being resolved.



#### WINHTTP_CALLBACK_STATUS_RESPONSE_RECEIVED

Successfully received a response from the server. The 
<i>lpvStatusInformation</i> parameter contains a pointer to a <b>DWORD</b> indicating the number of bytes received.



#### WINHTTP_CALLBACK_STATUS_SECURE_FAILURE

One or more errors were encountered while establishing a Secure (HTTPS) connection to the server. The 
<i>lpvStatusInformation</i> parameter contains a pointer to a <b>DWORD</b> that is a bitwise-OR combination of
error values. For more information, see the description for <i>lpvStatusInformation</i>.



#### WINHTTP_CALLBACK_STATUS_SENDING_REQUEST

Sending the information request to the server. The 
<i>lpvStatusInformation</i> parameter is <b>NULL</b>.



#### WINHTTP_CALLBACK_STATUS_SENDREQUEST_COMPLETE

The request completed successfully.  The 
<i>lpvStatusInformation</i> parameter is the lpOptional value passed to
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a> (the initial request body),
and the <i>dwStatusInformationLength</i> parameter indicates the number of such initial body bytes successfully
written (the dwOptionalLength value passed to WinHttpSendRequest).



#### WINHTTP_CALLBACK_STATUS_WRITE_COMPLETE

Data was successfully written to the server.  The 
<i>lpvStatusInformation</i> parameter contains a pointer to a <b>DWORD</b> that indicates the number of bytes written.

When used by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive">WinHttpWebSocketSend</a>, the 
<i>lpvStatusInformation</i> parameter contains a pointer to a <a href="/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status">WINHTTP_WEB_SOCKET_STATUS</a> structure, and the 
<i>dwStatusInformationLength</i> parameter indicates the size of <i>lpvStatusInformation</i>.



#### WINHTTP_CALLBACK_STATUS_GETPROXYFORURL_COMPLETE

The operation initiated by a call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurlex">WinHttpGetProxyForUrlEx</a> is complete. Data is available to be retrieved with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a>.   



#### WINHTTP_CALLBACK_STATUS_CLOSE_COMPLETE

The connection was successfully closed via a call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose">WinHttpWebSocketClose</a>.
The <i>lpvStatusInformation</i> parameter is <b>NULL</b>.



#### WINHTTP_CALLBACK_STATUS_SHUTDOWN_COMPLETE

The connection was successfully shut down via a call to <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown">WinHttpWebSocketShutdown</a>.
The <i>lpvStatusInformation</i> parameter is <b>NULL</b>.

### -param lpvStatusInformation [in]

A pointer to a buffer that specifies information pertinent to this call to the callback function. The format of these data depends on the value of the <i>dwInternetStatus</i> argument. For more information, see <i>dwInternetStatus</i>.


If the <i>dwInternetStatus</i> argument is WINHTTP_CALLBACK_STATUS_SECURE_FAILURE, then <i>lpvStatusInformation</i> points to a DWORD which is a bitwise-OR combination of one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_STATUS_FLAG_CERT_REV_FAILED"></a><a id="winhttp_callback_status_flag_cert_rev_failed"></a><dl>
<dt><b>WINHTTP_CALLBACK_STATUS_FLAG_CERT_REV_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Certification revocation checking has been enabled, but the revocation check failed to verify whether a certificate has been revoked.  The server used to check for revocation might be unreachable.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_STATUS_FLAG_INVALID_CERT"></a><a id="winhttp_callback_status_flag_invalid_cert"></a><dl>
<dt><b>WINHTTP_CALLBACK_STATUS_FLAG_INVALID_CERT</b></dt>
</dl>
</td>
<td width="60%">
SSL certificate is invalid.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_STATUS_FLAG_CERT_REVOKED"></a><a id="winhttp_callback_status_flag_cert_revoked"></a><dl>
<dt><b>WINHTTP_CALLBACK_STATUS_FLAG_CERT_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
SSL certificate was revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_STATUS_FLAG_INVALID_CA"></a><a id="winhttp_callback_status_flag_invalid_ca"></a><dl>
<dt><b>WINHTTP_CALLBACK_STATUS_FLAG_INVALID_CA</b></dt>
</dl>
</td>
<td width="60%">
The function is unfamiliar with the Certificate Authority that generated the server's certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_STATUS_FLAG_CERT_CN_INVALID"></a><a id="winhttp_callback_status_flag_cert_cn_invalid"></a><dl>
<dt><b>WINHTTP_CALLBACK_STATUS_FLAG_CERT_CN_INVALID</b></dt>
</dl>
</td>
<td width="60%">
SSL certificate common name (host name field) is incorrect, for example, if you entered www.microsoft.com and the common name on the certificate says www.msn.com.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_STATUS_FLAG_CERT_DATE_INVALID"></a><a id="winhttp_callback_status_flag_cert_date_invalid"></a><dl>
<dt><b>WINHTTP_CALLBACK_STATUS_FLAG_CERT_DATE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
SSL certificate date that was received from the server is bad. The certificate is expired.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_STATUS_FLAG_SECURITY_CHANNEL_ERROR"></a><a id="winhttp_callback_status_flag_security_channel_error"></a><dl>
<dt><b>WINHTTP_CALLBACK_STATUS_FLAG_SECURITY_CHANNEL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The application experienced an internal error loading the SSL libraries.

</td>
</tr>
</table>

### -param dwStatusInformationLength [in]

<b>WINHTTP_CALLBACK_STATUS_REDIRECT</b> status callbacks provide a <i>dwStatusInformationLength</i> value that corresponds to the character count of the <b>LPWSTR</b> pointed to by <i>lpvStatusInformation</i>.

## -remarks

The callback function must be threadsafe and reentrant because it can be called on another thread for a separate request, and reentered on the same thread for the current request. It must therefore be coded to handle reentrance safely while processing. When the <i>dwInternetStatus</i> parameter is equal to <b>WINHTTP_CALLBACK_STATUS_HANDLE_CLOSING</b>, the callback does not need to be able to handle reentrance for the same request, because this callback is guaranteed to be the last, and does not occur when other messages for this request are handled.

The status callback function receives updates on the status of asynchronous operations through notification flags.  Notifications that indicate a particular operation is complete are called completion notifications, or just completions.  The following table lists the six completion flags and the corresponding function that is complete when this flag is received.

<table class="clsStd">
<tr>
<th>Completion flag</th>
<th>Function</th>
</tr>
<tr>
<td>WINHTTP_CALLBACK_STATUS_DATA_AVAILABLE</td>
<td>
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpquerydataavailable">WinHttpQueryDataAvailable</a>
</td>
</tr>
<tr>
<td>WINHTTP_CALLBACK_STATUS_HEADERS_AVAILABLE</td>
<td>
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreceiveresponse">WinHttpReceiveResponse</a>
</td>
</tr>
<tr>
<td>WINHTTP_CALLBACK_STATUS_READ_COMPLETE</td>
<td>
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpreaddata">WinHttpReadData</a>
</td>
</tr>
<tr>
<td>WINHTTP_CALLBACK_STATUS_SENDREQUEST_COMPLETE</td>
<td>
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>
</td>
</tr>
<tr>
<td>WINHTTP_CALLBACK_STATUS_WRITE_COMPLETE</td>
<td>
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwritedata">WinHttpWriteData</a>
</td>
</tr>
<tr>
<td>WINHTTP_CALLBACK_STATUS_REQUEST_ERROR</td>
<td>Any of the above functions when an error occurs.</td>
</tr>
</table>
 

Because callbacks are made during the processing of the request, the application should spend as little time as possible in the callback function to avoid degrading data throughput on the network. For example, displaying a dialog box in a callback function can be such a lengthy operation that the server terminates the request.

The callback function can be called in a thread context different from the thread that initiated the request.

Similarly, there is no callback thread affinity when you call WinHttp asynchronously: a call might start from one thread, but any other thread can receive the callback.


<div class="alert"><b>Note</b>  For more information about implementation in Windows XP and Windows 2000, see <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetstatuscallback">WinHttpSetStatusCallback</a>
