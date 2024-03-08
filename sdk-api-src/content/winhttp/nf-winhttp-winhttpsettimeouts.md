---
UID: NF:winhttp.WinHttpSetTimeouts
title: WinHttpSetTimeouts function (winhttp.h)
description: Sets time-outs involved with HTTP transactions.
helpviewer_keywords: ["WinHttpSetTimeouts","WinHttpSetTimeouts function [WinHTTP]","http.winhttpsettimeouts","winhttp.winhttpsettimeouts_function","winhttp/WinHttpSetTimeouts"]
old-location: http\winhttpsettimeouts.htm
tech.root: http
ms.assetid: e31fee78-44bd-41cd-a181-bb3c0418b469
ms.date: 01/11/2024
ms.keywords: WinHttpSetTimeouts, WinHttpSetTimeouts function [WinHTTP], http.winhttpsettimeouts, winhttp.winhttpsettimeouts_function, winhttp/WinHttpSetTimeouts
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
 - WinHttpSetTimeouts
 - winhttp/WinHttpSetTimeouts
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
 - WinHttpSetTimeouts
---

## -description

The <b>WinHttpSetTimeouts</b> function sets time-outs involved with HTTP transactions.

## -parameters

### -param hInternet [in]

The <a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a> or <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>.

### -param nResolveTimeout [in]

A value of type integer that specifies the time-out value, in milliseconds, to use for name resolution. If resolution takes longer than this time-out value, then the request is canceled. The initial value is zero, meaning no time-out (infinite). 

<b>Windows Vista and Windows XP:  </b>If DNS timeout is specified using NAME_RESOLUTION_TIMEOUT, there is an overhead of one thread per request.

### -param nConnectTimeout [in]

A value of type integer that specifies the time-out value, in milliseconds, to use for server connection requests. If a connection request takes longer than this time-out value, the request is canceled. The initial value is 60,000 (60 seconds).

TCP/IP can time out while setting up the socket during the three leg SYN/ACK exchange, regardless of the value of this parameter.

### -param nSendTimeout [in]

A value of type integer that specifies the time-out value, in milliseconds, to use for sending requests. If sending a request takes longer than this time-out value, the send is canceled. The initial value is 30,000 (30 seconds).

### -param nReceiveTimeout [in]

A value of type integer that specifies the time-out value, in milliseconds, to receive a response to a request. If a response takes longer than this time-out value, the request is canceled. The initial value is 30,000 (30 seconds).

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the timeout parameters has a negative value other than -1.

</td>
</tr>
</table>

## -remarks

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

A value of 0 or -1 sets a time-out to wait infinitely.  A value greater than 0 sets the time-out value in milliseconds.  For example, 30,000 would set the time-out to 30 seconds.  All negative values other than -1 cause the function to fail with ERROR_INVALID_PARAMETER.

<div class="alert"><b>Important</b>  If a small timeout is set using <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption">WinHttpSetOption</a> and <a href="/windows/desktop/WinHttp/option-flags">WINHTTP_OPTION_RECEIVE_TIMEOUT</a>, it can override the value set with the <i>dwReceiveTimeout</i> parameter, causing a response to terminate earlier than expected. To avoid this, do not set a timeout with the <b>WINHTTP_OPTION_RECEIVE_TIMEOUT</b> option that is smaller than the value set using <i>dwReceiveTimeout</i>.</div>
<div> </div>
<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHTTP start page.</div>
<div> </div>

#### Examples

This example shows how to set new time-out values using 
<b>WinHttpSetTimeouts</b>.


```cpp
    // Use WinHttpOpen to obtain an HINTERNET handle.
    HINTERNET hSession = WinHttpOpen(L"A WinHTTP Example Program/1.0", 
                                    WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                                    WINHTTP_NO_PROXY_NAME, 
                                    WINHTTP_NO_PROXY_BYPASS, 0);
    if (hSession)
    {
        // Use WinHttpSetTimeouts to set a new time-out values.
        if (!WinHttpSetTimeouts( hSession, 10000, 10000, 10000, 10000))
            printf( "Error %u in WinHttpSetTimeouts.\n", GetLastError());
              
        // PLACE ADDITIONAL CODE HERE.
    
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



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpclosehandle">WinHttpCloseHandle</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpconnect">WinHttpConnect</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>