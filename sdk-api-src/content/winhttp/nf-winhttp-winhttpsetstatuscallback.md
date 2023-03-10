---
UID: NF:winhttp.WinHttpSetStatusCallback
title: WinHttpSetStatusCallback function (winhttp.h)
description: The WinHttpSetStatusCallback function sets up a callback function that WinHTTP can call as progress is made during an operation.
helpviewer_keywords: ["WINHTTP_CALLBACK_FLAG_ALL_COMPLETIONS","WINHTTP_CALLBACK_FLAG_ALL_NOTIFICATIONS","WINHTTP_CALLBACK_FLAG_CLOSE_CONNECTION","WINHTTP_CALLBACK_FLAG_CONNECT_TO_SERVER","WINHTTP_CALLBACK_FLAG_DATA_AVAILABLE","WINHTTP_CALLBACK_FLAG_DETECTING_PROXY","WINHTTP_CALLBACK_FLAG_HANDLES","WINHTTP_CALLBACK_FLAG_HEADERS_AVAILABLE","WINHTTP_CALLBACK_FLAG_INTERMEDIATE_RESPONSE","WINHTTP_CALLBACK_FLAG_READ_COMPLETE","WINHTTP_CALLBACK_FLAG_RECEIVE_RESPONSE","WINHTTP_CALLBACK_FLAG_REDIRECT","WINHTTP_CALLBACK_FLAG_REQUEST_ERROR","WINHTTP_CALLBACK_FLAG_RESOLVE_NAME","WINHTTP_CALLBACK_FLAG_SECURE_FAILURE","WINHTTP_CALLBACK_FLAG_SENDREQUEST_COMPLETE","WINHTTP_CALLBACK_FLAG_SEND_REQUEST","WINHTTP_CALLBACK_FLAG_WRITE_COMPLETE","WinHttpSetStatusCallback","WinHttpSetStatusCallback function [WinHTTP]","http.winhttpsetstatuscallback","winhttp.winhttpsetstatuscallback_function","winhttp/WinHttpSetStatusCallback"]
old-location: http\winhttpsetstatuscallback.htm
tech.root: http
ms.assetid: b093daf0-7abe-49cb-8c09-9519e3c130b6
ms.date: 12/05/2018
ms.keywords: WINHTTP_CALLBACK_FLAG_ALL_COMPLETIONS, WINHTTP_CALLBACK_FLAG_ALL_NOTIFICATIONS, WINHTTP_CALLBACK_FLAG_CLOSE_CONNECTION, WINHTTP_CALLBACK_FLAG_CONNECT_TO_SERVER, WINHTTP_CALLBACK_FLAG_DATA_AVAILABLE, WINHTTP_CALLBACK_FLAG_DETECTING_PROXY, WINHTTP_CALLBACK_FLAG_HANDLES, WINHTTP_CALLBACK_FLAG_HEADERS_AVAILABLE, WINHTTP_CALLBACK_FLAG_INTERMEDIATE_RESPONSE, WINHTTP_CALLBACK_FLAG_READ_COMPLETE, WINHTTP_CALLBACK_FLAG_RECEIVE_RESPONSE, WINHTTP_CALLBACK_FLAG_REDIRECT, WINHTTP_CALLBACK_FLAG_REQUEST_ERROR, WINHTTP_CALLBACK_FLAG_RESOLVE_NAME, WINHTTP_CALLBACK_FLAG_SECURE_FAILURE, WINHTTP_CALLBACK_FLAG_SENDREQUEST_COMPLETE, WINHTTP_CALLBACK_FLAG_SEND_REQUEST, WINHTTP_CALLBACK_FLAG_WRITE_COMPLETE, WinHttpSetStatusCallback, WinHttpSetStatusCallback function [WinHTTP], http.winhttpsetstatuscallback, winhttp.winhttpsetstatuscallback_function, winhttp/WinHttpSetStatusCallback
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
 - WinHttpSetStatusCallback
 - winhttp/WinHttpSetStatusCallback
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
 - WinHttpSetStatusCallback
---

# WinHttpSetStatusCallback function


## -description

The <b>WinHttpSetStatusCallback</b> function sets up a callback function that WinHTTP can call as progress is made during an operation.

## -parameters

### -param hInternet [in]

<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle for which the callback is to be set.

### -param lpfnInternetCallback [in]

Pointer to the callback function to call when progress is made.  Set this to <b>NULL</b> to remove the existing callback function. For more information about the callback function, see 
<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a>.

### -param dwNotificationFlags [in]

Unsigned long integer value that specifies flags to indicate which
                events  activate the callback function.

The possible values are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_ALL_COMPLETIONS"></a><a id="winhttp_callback_flag_all_completions"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_ALL_COMPLETIONS</b></dt>
</dl>
</td>
<td width="60%">
Activates upon any completion notification.  This flag specifies that all notifications required for read or write operations are used. See 
<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a> for a list of completions.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_ALL_NOTIFICATIONS"></a><a id="winhttp_callback_flag_all_notifications"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_ALL_NOTIFICATIONS</b></dt>
</dl>
</td>
<td width="60%">
Activates upon any status change notification including completions.  See 
<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a> for a list of notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_RESOLVE_NAME"></a><a id="winhttp_callback_flag_resolve_name"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_RESOLVE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Activates upon beginning and completing name resolution.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_CONNECT_TO_SERVER"></a><a id="winhttp_callback_flag_connect_to_server"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_CONNECT_TO_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Activates upon beginning and completing connection to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_DETECTING_PROXY"></a><a id="winhttp_callback_flag_detecting_proxy"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_DETECTING_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Activates when detecting the proxy server.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_DATA_AVAILABLE"></a><a id="winhttp_callback_flag_data_available"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_DATA_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
Activates when completing a query for data.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_HEADERS_AVAILABLE"></a><a id="winhttp_callback_flag_headers_available"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_HEADERS_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
Activates when the response headers are available for retrieval.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_READ_COMPLETE"></a><a id="winhttp_callback_flag_read_complete"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_READ_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Activates upon completion of a data-read operation.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_REQUEST_ERROR"></a><a id="winhttp_callback_flag_request_error"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_REQUEST_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Activates when an asynchronous error occurs.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_SEND_REQUEST"></a><a id="winhttp_callback_flag_send_request"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_SEND_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Activates upon beginning and completing the sending of a request
                    header with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_SENDREQUEST_COMPLETE"></a><a id="winhttp_callback_flag_sendrequest_complete"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_SENDREQUEST_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Activates when a request header has been sent with 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_WRITE_COMPLETE"></a><a id="winhttp_callback_flag_write_complete"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_WRITE_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Activates upon completion of a data-post operation.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_RECEIVE_RESPONSE"></a><a id="winhttp_callback_flag_receive_response"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_RECEIVE_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
Activates upon beginning and completing the receipt of a
                    resource from the HTTP server.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_CLOSE_CONNECTION"></a><a id="winhttp_callback_flag_close_connection"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_CLOSE_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
Activates when beginning and completing the closing of an
                    HTTP connection.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_HANDLES"></a><a id="winhttp_callback_flag_handles"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_HANDLES</b></dt>
</dl>
</td>
<td width="60%">
Activates when an 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle is 
                    created or closed.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_REDIRECT"></a><a id="winhttp_callback_flag_redirect"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_REDIRECT</b></dt>
</dl>
</td>
<td width="60%">
Activates when the request is redirected.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_INTERMEDIATE_RESPONSE"></a><a id="winhttp_callback_flag_intermediate_response"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_INTERMEDIATE_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
Activates when receiving an intermediate (100 level) status 
                    code message from the server.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_CALLBACK_FLAG_SECURE_FAILURE"></a><a id="winhttp_callback_flag_secure_failure"></a><dl>
<dt><b>WINHTTP_CALLBACK_FLAG_SECURE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Activates upon a secure connection failure.

</td>
</tr>
</table>

### -param dwReserved [in]

This parameter is reserved and must be <b>NULL</b>.

## -returns

If successful, returns a pointer to the previously defined status callback function or  <b>NULL</b> if there was no previously defined status callback function. Returns <b>WINHTTP_INVALID_STATUS_CALLBACK</b> if the callback function could not be installed. For extended error information, call 
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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

If you set the callback on the session handle before creating the request handle, the request handle inherits the callback function pointer from its parent session.

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Both synchronous and asynchronous functions use the callback function to indicate the progress of the request, such as resolving a name, connecting to a server, and so on. The callback function is required for an asynchronous operation.

A callback function can be set on any handle and is inherited by derived handles. A callback function can be changed using 
<b>WinHttpSetStatusCallback</b>, provided there are no pending requests that need to use the previous callback value. However, changing the callback function on a handle does not change the callbacks on derived handles, such as that returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>. You must change the callback function at each level.

Many WinHTTP functions perform several operations on the network. Each operation can take time to complete and each can fail.

After initiating the 
<b>WinHttpSetStatusCallback</b> function, the callback function can be accessed from within WinHTTP for monitoring time-intensive network operations.

At the end of asynchronous processing, the application may set the callback function to <b>NULL</b>. This prevents the client application from receiving additional notifications.

The following code snippet shows the recommended method for setting the callback function to <b>NULL</b>.


``` syntax
WinHttpSetStatusCallback( hOpen,
                          NULL,
                          WINHTTP_CALLBACK_FLAG_ALL_NOTIFICATIONS,
                          NULL );

```

Note, however, that WinHTTP does not synchronize <b>WinHttpSetStatusCallback</b> with worker threads. If  a callback originating in another thread is in progress when an application calls <b>WinHttpSetStatusCallback</b>, the application still receives a callback notification even after <b>WinHttpSetStatusCallback</b> successfully sets the callback function to <b>NULL</b> and returns.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

## Examples

The following example shows how to install a callback function for asynchronous WinHTTP functions.  The example assumes that a 
<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a> function named "AsyncCallback( )" has been previously implemented:


```cpp
    // Use WinHttpOpen to obtain an HINTERNET handle.
    HINTERNET hSession = WinHttpOpen(L"A WinHTTP Example Program/1.0", 
                                    WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                                    WINHTTP_NO_PROXY_NAME, 
                                    WINHTTP_NO_PROXY_BYPASS, 0);
    if (hSession)
    {
        // Install the status callback function.
        WINHTTP_STATUS_CALLBACK isCallback = WinHttpSetStatusCallback( hSession,
                                               (WINHTTP_STATUS_CALLBACK)AsyncCallback,
                                               WINHTTP_CALLBACK_FLAG_ALL_NOTIFICATIONS, 
                                               NULL);
                                               
        // Place additional code here.
    
        // When finished, release the HINTERNET handle.
        WinHttpCloseHandle(hSession);
    }
    else
    {
        printf("Error %u in WinHttpOpen.\n", GetLastError());
    }

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>
