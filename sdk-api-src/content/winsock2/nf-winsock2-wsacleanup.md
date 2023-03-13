---
UID: NF:winsock2.WSACleanup
title: WSACleanup function (winsock2.h)
description: The WSACleanup function (winsock2.h) terminates use of the WS2_32.dll. 
helpviewer_keywords: ["WSACleanup","WSACleanup function [Winsock]","_win32_wsacleanup_2","winsock.wsacleanup_2","winsock/WSACleanup"]
old-location: winsock\wsacleanup_2.htm
tech.root: WinSock
ms.assetid: 72b7cc3e-be34-41e7-acbf-61742149ec8b
ms.date: 08/03/2022
ms.keywords: WSACleanup, WSACleanup function [Winsock], _win32_wsacleanup_2, winsock.wsacleanup_2, winsock/WSACleanup
req.header: winsock2.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - WSACleanup
 - winsock2/WSACleanup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
 - bcrypt.dll
 - wsock32.dll
api_name:
 - WSACleanup
---

# WSACleanup function


## -description

The 
<b>WSACleanup</b> function terminates use of the Winsock 2 DLL (<i>Ws2_32.dll</i>).



## -returns

The return value is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

In a multithreaded environment, 
<b>WSACleanup</b> terminates Windows Sockets operations for all threads.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
</table>

## -remarks

An application or DLL is required to perform a successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call before it can use Windows Sockets services. When it has completed the use of Windows Sockets, the application or DLL must call 
<b>WSACleanup</b> to deregister itself from a Windows Sockets implementation and allow the implementation to free any resources allocated on behalf of the application or DLL. 

When <b>WSACleanup</b> is called, any pending blocking or asynchronous Windows Sockets calls issued by any thread in this process are canceled without posting any notification messages or without signaling any event objects. Any pending overlapped send or receive operations (<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a> with an overlapped socket, for example) issued by any thread in this process are also canceled without setting the event object or invoking the completion routine, if one was specified. In this case, the pending overlapped operations fail with the error status <b>WSA_OPERATION_ABORTED</b>.

Sockets that were open when 
<b>WSACleanup</b> was called are reset and automatically deallocated as if 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> were called. Sockets that have been closed with 
<b>closesocket</b> but that still have pending data to be sent can be affected when 
<b>WSACleanup</b> is called. In this case, the pending data can be lost if the WS2_32.DLL is unloaded from memory as the application exits. To ensure that all pending data is sent, an application should use 
<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> to close the connection, then wait until the close completes before calling 
<b>closesocket</b> and 
<b>WSACleanup</b>. All resources and internal state, such as queued unposted or posted messages, must be deallocated so as to be available to the next user.

There must be a call to 
<b>WSACleanup</b> for each successful call to 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>. Only the final 
<b>WSACleanup</b> function call performs the actual cleanup. The preceding calls simply decrement an internal reference count in the WS2_32.DLL.

<div class="alert"><b>Note</b>  <b>WSACleanup</b> does not unregister names (peer names, for example) that may have been registered with a Windows Sockets namespace provider such as Peer Name Resolution Protocol (PNRP) namespace provider.</div>
<div> </div>
In  Windows Sockets 1.1, attempting to call 
<b>WSACleanup</b> from within a blocking hook and then failing to check the return code was a common programming error. If a Winsock 1.1 application needs to quit while a blocking call is outstanding, the application has to first cancel the blocking call with 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a> then issue the 
<b>WSACleanup</b> call once control has been returned to the application. In Windows Sockets 2, this issue does not exist and the <b>WSACancelBlockingCall</b> function has been removed.

The 
<b>WSACleanup</b> function typically leads to protocol-specific helper DLLs being unloaded. As a result, the 
<b>WSACleanup</b> function should not be called from the DllMain function in a application DLL. This can potentially cause deadlocks. For more information, please see the <a href="/windows/win32/dlls/dllmain">DLL Main Function</a>.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/P2PSdk/pnrp-namespace-provider-api">PNRP Namespace Provider API</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>



<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a>
