---
UID: NC:wininet.INTERNET_STATUS_CALLBACK
title: INTERNET_STATUS_CALLBACK (wininet.h)
description: Defines a pointer to this callback function.
helpviewer_keywords: ["INTERNET_STATE_BUSY","INTERNET_STATE_CONNECTED","INTERNET_STATE_DISCONNECTED","INTERNET_STATE_DISCONNECTED_BY_USER","INTERNET_STATE_IDLE","INTERNET_STATUS_CALLBACK","INTERNET_STATUS_CALLBACK callback function [WinINet]","INTERNET_STATUS_CLOSING_CONNECTION","INTERNET_STATUS_CONNECTED_TO_SERVER","INTERNET_STATUS_CONNECTING_TO_SERVER","INTERNET_STATUS_CONNECTION_CLOSED","INTERNET_STATUS_COOKIE_HISTORY","INTERNET_STATUS_COOKIE_RECEIVED","INTERNET_STATUS_COOKIE_SENT","INTERNET_STATUS_CTL_RESPONSE_RECEIVED","INTERNET_STATUS_DETECTING_PROXY","INTERNET_STATUS_HANDLE_CLOSING","INTERNET_STATUS_HANDLE_CREATED","INTERNET_STATUS_INTERMEDIATE_RESPONSE","INTERNET_STATUS_NAME_RESOLVED","INTERNET_STATUS_P3P_HEADER","INTERNET_STATUS_P3P_POLICYREF","INTERNET_STATUS_PREFETCH","INTERNET_STATUS_PRIVACY_IMPACTED","INTERNET_STATUS_RECEIVING_RESPONSE","INTERNET_STATUS_REDIRECT","INTERNET_STATUS_REQUEST_COMPLETE","INTERNET_STATUS_REQUEST_SENT","INTERNET_STATUS_RESOLVING_NAME","INTERNET_STATUS_RESPONSE_RECEIVED","INTERNET_STATUS_SENDING_REQUEST","INTERNET_STATUS_STATE_CHANGE","INTERNET_STATUS_USER_INPUT_REQUIRED","InternetStatusCallback","InternetStatusCallback callback","InternetStatusCallback callback function [WinINet]","_inet_internet_status_callback_prototype","wininet.internetstatuscallback","wininet/InternetStatusCallback"]
old-location: wininet\internetstatuscallback.htm
tech.root: wininet
ms.assetid: a054fb71-66ab-46fd-be19-2237f05662bc
ms.date: 12/05/2018
ms.keywords: INTERNET_STATE_BUSY, INTERNET_STATE_CONNECTED, INTERNET_STATE_DISCONNECTED, INTERNET_STATE_DISCONNECTED_BY_USER, INTERNET_STATE_IDLE, INTERNET_STATUS_CALLBACK, INTERNET_STATUS_CALLBACK callback function [WinINet], INTERNET_STATUS_CLOSING_CONNECTION, INTERNET_STATUS_CONNECTED_TO_SERVER, INTERNET_STATUS_CONNECTING_TO_SERVER, INTERNET_STATUS_CONNECTION_CLOSED, INTERNET_STATUS_COOKIE_HISTORY, INTERNET_STATUS_COOKIE_RECEIVED, INTERNET_STATUS_COOKIE_SENT, INTERNET_STATUS_CTL_RESPONSE_RECEIVED, INTERNET_STATUS_DETECTING_PROXY, INTERNET_STATUS_HANDLE_CLOSING, INTERNET_STATUS_HANDLE_CREATED, INTERNET_STATUS_INTERMEDIATE_RESPONSE, INTERNET_STATUS_NAME_RESOLVED, INTERNET_STATUS_P3P_HEADER, INTERNET_STATUS_P3P_POLICYREF, INTERNET_STATUS_PREFETCH, INTERNET_STATUS_PRIVACY_IMPACTED, INTERNET_STATUS_RECEIVING_RESPONSE, INTERNET_STATUS_REDIRECT, INTERNET_STATUS_REQUEST_COMPLETE, INTERNET_STATUS_REQUEST_SENT, INTERNET_STATUS_RESOLVING_NAME, INTERNET_STATUS_RESPONSE_RECEIVED, INTERNET_STATUS_SENDING_REQUEST, INTERNET_STATUS_STATE_CHANGE, INTERNET_STATUS_USER_INPUT_REQUIRED, InternetStatusCallback, InternetStatusCallback callback, InternetStatusCallback callback function [WinINet], _inet_internet_status_callback_prototype, wininet.internetstatuscallback, wininet/InternetStatusCallback
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INTERNET_STATUS_CALLBACK
 - wininet/INTERNET_STATUS_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wininet.h
api_name:
 - INTERNET_STATUS_CALLBACK
---

# INTERNET_STATUS_CALLBACK callback function


## -description

Prototype for an application-defined status callback function.

The <b>INTERNET_STATUS_CALLBACK</b> type defines a pointer to this callback function.<i>InternetStatusCallback</i> is a placeholder for the application-defined function name.

## -parameters

### -param hInternet [in]

The handle for which the callback function is called.

### -param dwContext [in]

A pointer to a variable that specifies the application-defined context value associated with 
<i>hInternet</i>.

### -param dwInternetStatus [in]

A status code that indicates why the callback function is called. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_CLOSING_CONNECTION"></a><a id="internet_status_closing_connection"></a><dl>
<dt><b>INTERNET_STATUS_CLOSING_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
Closing the connection to the server. The 
<i>lpvStatusInformation</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_CONNECTED_TO_SERVER"></a><a id="internet_status_connected_to_server"></a><dl>
<dt><b>INTERNET_STATUS_CONNECTED_TO_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Successfully connected to the socket address (SOCKADDR) pointed to by 
<i>lpvStatusInformation</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_CONNECTING_TO_SERVER"></a><a id="internet_status_connecting_to_server"></a><dl>
<dt><b>INTERNET_STATUS_CONNECTING_TO_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Connecting to the socket address (SOCKADDR) pointed to by 
<i>lpvStatusInformation</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_CONNECTION_CLOSED"></a><a id="internet_status_connection_closed"></a><dl>
<dt><b>INTERNET_STATUS_CONNECTION_CLOSED</b></dt>
</dl>
</td>
<td width="60%">
Successfully closed the connection to the server. The 
<i>lpvStatusInformation</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_COOKIE_HISTORY"></a><a id="internet_status_cookie_history"></a><dl>
<dt><b>INTERNET_STATUS_COOKIE_HISTORY</b></dt>
</dl>
</td>
<td width="60%">
Retrieving content from the cache. Contains data about past cookie events for the URL such as if cookies were accepted, rejected, downgraded, or leashed.  

The 
<i>lpvStatusInformation</i> parameter is a pointer to an <a href="/windows/win32/api/wininet/ns-wininet-internet_proxy_info">InternetCookieHistory</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_COOKIE_RECEIVED"></a><a id="internet_status_cookie_received"></a><dl>
<dt><b>INTERNET_STATUS_COOKIE_RECEIVED</b></dt>
</dl>
</td>
<td width="60%">
Indicates the number of cookies that were accepted, rejected, downgraded (changed from persistent to session cookies), or leashed (will be sent out only in 1st party context). The 
<i>lpvStatusInformation</i> parameter is a <b>DWORD</b> with the number of cookies received.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_COOKIE_SENT"></a><a id="internet_status_cookie_sent"></a><dl>
<dt><b>INTERNET_STATUS_COOKIE_SENT</b></dt>
</dl>
</td>
<td width="60%">
Indicates the number of cookies that were either sent or suppressed, when a request is sent. The 
<i>lpvStatusInformation</i> parameter is a <b>DWORD</b> with the number of cookies sent or suppressed.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_CTL_RESPONSE_RECEIVED"></a><a id="internet_status_ctl_response_received"></a><dl>
<dt><b>INTERNET_STATUS_CTL_RESPONSE_RECEIVED</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_DETECTING_PROXY"></a><a id="internet_status_detecting_proxy"></a><dl>
<dt><b>INTERNET_STATUS_DETECTING_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Notifies the client application that a proxy has been detected.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_HANDLE_CLOSING"></a><a id="internet_status_handle_closing"></a><dl>
<dt><b>INTERNET_STATUS_HANDLE_CLOSING</b></dt>
</dl>
</td>
<td width="60%">
This handle value has been terminated. pvStatusInformation contains the address of the handle being closed. The <i>lpvStatusInformation</i> parameter contains the address of the handle being closed.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_HANDLE_CREATED"></a><a id="internet_status_handle_created"></a><dl>
<dt><b>INTERNET_STATUS_HANDLE_CREATED</b></dt>
</dl>
</td>
<td width="60%">
Used by 
<a href="/windows/desktop/api/wininet/nf-wininet-internetconnecta">InternetConnect</a> to indicate it has created the new handle. This lets the application call 
<a href="/windows/desktop/api/wininet/nf-wininet-internetclosehandle">InternetCloseHandle</a> from another thread, if the connect is taking too long. The 
<i>lpvStatusInformation</i> parameter contains the address of an 
<a href="/windows/desktop/WinInet/appendix-a-hinternet-handles">HINTERNET</a> handle.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_INTERMEDIATE_RESPONSE"></a><a id="internet_status_intermediate_response"></a><dl>
<dt><b>INTERNET_STATUS_INTERMEDIATE_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
Received an intermediate (100 level) status code message from the server.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_NAME_RESOLVED"></a><a id="internet_status_name_resolved"></a><dl>
<dt><b>INTERNET_STATUS_NAME_RESOLVED</b></dt>
</dl>
</td>
<td width="60%">
Successfully found the IP address of the name contained in 
<i>lpvStatusInformation</i>. The <i>lpvStatusInformation</i> parameter points to a <b>PCTSTR</b> containing the host name.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_P3P_HEADER"></a><a id="internet_status_p3p_header"></a><dl>
<dt><b>INTERNET_STATUS_P3P_HEADER</b></dt>
</dl>
</td>
<td width="60%">
 The response has a P3P header in it.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_P3P_POLICYREF"></a><a id="internet_status_p3p_policyref"></a><dl>
<dt><b>INTERNET_STATUS_P3P_POLICYREF</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_PREFETCH"></a><a id="internet_status_prefetch"></a><dl>
<dt><b>INTERNET_STATUS_PREFETCH</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_PRIVACY_IMPACTED_"></a><a id="internet_status_privacy_impacted_"></a><dl>
<dt><b>INTERNET_STATUS_PRIVACY_IMPACTED </b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_RECEIVING_RESPONSE"></a><a id="internet_status_receiving_response"></a><dl>
<dt><b>INTERNET_STATUS_RECEIVING_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
Waiting for the server to respond to a request. The 
<i>lpvStatusInformation</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_REDIRECT"></a><a id="internet_status_redirect"></a><dl>
<dt><b>INTERNET_STATUS_REDIRECT</b></dt>
</dl>
</td>
<td width="60%">
An HTTP request is about to automatically redirect the request. The 
<i>lpvStatusInformation</i> parameter points to the new URL. At this point, the application can read any data returned by the server with the redirect response and can query the response headers. It can also cancel the operation by closing the handle. This callback is not made if the original request specified 
<a href="/windows/desktop/WinInet/api-flags">INTERNET_FLAG_NO_AUTO_REDIRECT</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_REQUEST_COMPLETE"></a><a id="internet_status_request_complete"></a><dl>
<dt><b>INTERNET_STATUS_REQUEST_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
An asynchronous operation has been completed. The 
<i>lpvStatusInformation</i> parameter contains the address of an 
<a href="/windows/desktop/api/wininet/ns-wininet-internet_async_result">INTERNET_ASYNC_RESULT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_REQUEST_SENT"></a><a id="internet_status_request_sent"></a><dl>
<dt><b>INTERNET_STATUS_REQUEST_SENT</b></dt>
</dl>
</td>
<td width="60%">
Successfully sent the information request to the server. The 
<i>lpvStatusInformation</i> parameter points to a <b>DWORD</b> value that contains the number of bytes sent.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_RESOLVING_NAME"></a><a id="internet_status_resolving_name"></a><dl>
<dt><b>INTERNET_STATUS_RESOLVING_NAME</b></dt>
</dl>
</td>
<td width="60%">
Looking up the IP address of the name contained in 
<i>lpvStatusInformation</i>. The <i>lpvStatusInformation</i> parameter points to a <b>PCTSTR</b> containing the host name.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_RESPONSE_RECEIVED"></a><a id="internet_status_response_received"></a><dl>
<dt><b>INTERNET_STATUS_RESPONSE_RECEIVED</b></dt>
</dl>
</td>
<td width="60%">
Successfully received a response from the server. 

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_SENDING_REQUEST"></a><a id="internet_status_sending_request"></a><dl>
<dt><b>INTERNET_STATUS_SENDING_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Sending the information request to the server. The 
<i>lpvStatusInformation</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_STATE_CHANGE"></a><a id="internet_status_state_change"></a><dl>
<dt><b>INTERNET_STATUS_STATE_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
Moved between a secure (HTTPS) and a nonsecure (HTTP) site. The user must be informed of this change; otherwise, the user is at risk of disclosing sensitive information involuntarily.  When this flag is set, the <i>lpvStatusInformation</i> parameter points to a status  DWORD that contains additional flags.

</td>
</tr>
</table>

### -param lpvStatusInformation [in]

A pointer to additional status information. When the <b>INTERNET_STATUS_STATE_CHANGE</b> flag is set, <i>lpvStatusInformation</i> points to a <b>DWORD</b> that contains one or more of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_CONNECTED"></a><a id="internet_state_connected"></a><dl>
<dt><b>INTERNET_STATE_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Connected state. Mutually exclusive with disconnected state.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_DISCONNECTED"></a><a id="internet_state_disconnected"></a><dl>
<dt><b>INTERNET_STATE_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Disconnected state. No network connection could be established.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_DISCONNECTED_BY_USER"></a><a id="internet_state_disconnected_by_user"></a><dl>
<dt><b>INTERNET_STATE_DISCONNECTED_BY_USER</b></dt>
</dl>
</td>
<td width="60%">
Disconnected by user request.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_IDLE"></a><a id="internet_state_idle"></a><dl>
<dt><b>INTERNET_STATE_IDLE</b></dt>
</dl>
</td>
<td width="60%">
No network requests are being made by Windows Internet.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATE_BUSY"></a><a id="internet_state_busy"></a><dl>
<dt><b>INTERNET_STATE_BUSY</b></dt>
</dl>
</td>
<td width="60%">
Network requests are being made by Windows Internet.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_STATUS_USER_INPUT_REQUIRED"></a><a id="internet_status_user_input_required"></a><dl>
<dt><b>INTERNET_STATUS_USER_INPUT_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The request requires user input to be completed.

</td>
</tr>
</table>

### -param dwStatusInformationLength [in]

The size, in bytes, of the data pointed to by 
<i>lpvStatusInformation</i>.

## -remarks

Because callbacks are made during processing of the request, the application should spend little time in the callback function to avoid degrading data throughput on the network. For example, displaying a dialog box in a callback function can be such a lengthy operation that the server terminates the request.

The callback function can be called in a thread context different from the thread that initiated the request.

<div class="alert"><b>Caution</b>  Always notify the user when a state change from a secure (HTTPS) site to a nonsecure (HTTP) site occurs, to guard against involuntary information disclosure.</div>
<div> </div>
Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/asynchronous-operation">Asynchronous Operation</a>



<a href="/windows/desktop/WinInet/creating-status-callback-functions">Creating Status Callback Functions</a>



<a href="/windows/desktop/api/wininet/ns-wininet-internet_async_result">INTERNET_ASYNC_RESULT</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>