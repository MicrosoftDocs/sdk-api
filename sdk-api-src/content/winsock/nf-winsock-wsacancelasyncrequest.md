---
UID: NF:winsock.WSACancelAsyncRequest
title: WSACancelAsyncRequest function (winsock.h)
description: The WSACancelAsyncRequest function (winsock.h) cancels an incomplete asynchronous operation.
helpviewer_keywords: ["WSACancelAsyncRequest","WSACancelAsyncRequest function [Winsock]","_win32_wsacancelasyncrequest_2","winsock.wsacancelasyncrequest_2","winsock/WSACancelAsyncRequest"]
old-location: winsock\wsacancelasyncrequest_2.htm
tech.root: WinSock
ms.assetid: 0e53eccf-ef85-43ec-a02c-12896471a7a9
ms.date: 08/16/2022
ms.keywords: WSACancelAsyncRequest, WSACancelAsyncRequest function [Winsock], _win32_wsacancelasyncrequest_2, winsock.wsacancelasyncrequest_2, winsock/WSACancelAsyncRequest
req.header: winsock.h
req.include-header: Winsock2.h
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSACancelAsyncRequest
 - winsock/WSACancelAsyncRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSACancelAsyncRequest
---

# WSACancelAsyncRequest function


## -description

The 
<b>WSACancelAsyncRequest</b> function cancels an incomplete asynchronous operation.

## -parameters

### -param hAsyncTaskHandle [in]

Handle that specifies the asynchronous operation to be canceled.

## -returns

The value returned by 
<b>WSACancelAsyncRequest</b> is zero if the operation was successfully canceled. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
Indicates that the specified asynchronous task handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
The asynchronous routine being canceled has already completed.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  It is unclear whether the application can usefully distinguish between 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a> and 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a>, since in both cases the error indicates that there is no asynchronous operation in progress with the indicated handle. (Trivial exception: zero is always an invalid asynchronous task handle.) The Windows Sockets specification does not prescribe how a conformant Windows Sockets provider should distinguish between the two cases. For maximum portability, a Windows Sockets application should treat the two errors as equivalent.</div>
<div> </div>

## -remarks

The 
<b>WSACancelAsyncRequest</b> function is used to cancel an asynchronous operation that was initiated by one of the <b>WSAAsyncGetXByY</b> functions such as 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname">WSAAsyncGetHostByName</a>. The operation to be canceled is identified by the <i>hAsyncTaskHandle</i> parameter, which should be set to the asynchronous task handle as returned by the initiating <b>WSAAsyncGetXByY</b> function.

An attempt to cancel an existing asynchronous <b>WSAAsyncGetXByY</b> operation can fail with an error code of 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a> for two reasons. First, the original operation has already completed and the application has dealt with the resultant message. Second, the original operation has already completed but the resultant message is still waiting in the application window queue.

## -see-also

<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyaddr">WSAAsyncGetHostByAddr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname">WSAAsyncGetHostByName</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname">WSAAsyncGetProtoByName</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber">WSAAsyncGetProtoByNumber</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname">WSAAsyncGetServByName</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport">WSAAsyncGetServByPort</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>
