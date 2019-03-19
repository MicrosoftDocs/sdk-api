---
UID: NF:winsock2.WSACancelAsyncRequest
title: WSACancelAsyncRequest function (winsock2.h)
author: windows-sdk-content
description: The WSACancelAsyncRequest function cancels an incomplete asynchronous operation.
old-location: winsock\wsacancelasyncrequest_2.htm
tech.root: WinSock
ms.assetid: 0e53eccf-ef85-43ec-a02c-12896471a7a9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSACancelAsyncRequest, WSACancelAsyncRequest function [Winsock], _win32_wsacancelasyncrequest_2, winsock.wsacancelasyncrequest_2, winsock/WSACancelAsyncRequest
ms.topic: function
req.header: winsock2.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSACancelAsyncRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
Indicates that the specified asynchronous task handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
The asynchronous routine being canceled has already completed.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  It is unclear whether the application can usefully distinguish between 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a> and 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEALREADY</a>, since in both cases the error indicates that there is no asynchronous operation in progress with the indicated handle. (Trivial exception: zero is always an invalid asynchronous task handle.) The Windows Sockets specification does not prescribe how a conformant Windows Sockets provider should distinguish between the two cases. For maximum portability, a Windows Sockets application should treat the two errors as equivalent.</div>
<div> </div>



## -remarks



The 
<b>WSACancelAsyncRequest</b> function is used to cancel an asynchronous operation that was initiated by one of the <b>WSAAsyncGetXByY</b> functions such as 
<a href="https://msdn.microsoft.com/1a2b9c76-6e84-4ac2-b5c1-a2268edd0c49">WSAAsyncGetHostByName</a>. The operation to be canceled is identified by the <i>hAsyncTaskHandle</i> parameter, which should be set to the asynchronous task handle as returned by the initiating <b>WSAAsyncGetXByY</b> function.

An attempt to cancel an existing asynchronous <b>WSAAsyncGetXByY</b> operation can fail with an error code of 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEALREADY</a> for two reasons. First, the original operation has already completed and the application has dealt with the resultant message. Second, the original operation has already completed but the resultant message is still waiting in the application window queue.




## -see-also




<a href="https://msdn.microsoft.com/814cbb2e-8dd2-44b0-b8be-cfc5491bdc49">WSAAsyncGetHostByAddr</a>



<a href="https://msdn.microsoft.com/1a2b9c76-6e84-4ac2-b5c1-a2268edd0c49">WSAAsyncGetHostByName</a>



<a href="https://msdn.microsoft.com/747c40fd-5dc1-4533-896e-bc1c4368d7bd">WSAAsyncGetProtoByName</a>



<a href="https://msdn.microsoft.com/10f28345-c178-47c0-9d0f-87f6743131d9">WSAAsyncGetProtoByNumber</a>



<a href="https://msdn.microsoft.com/d3524197-cd7a-4863-8fbb-a05e6f5d38e0">WSAAsyncGetServByName</a>



<a href="https://msdn.microsoft.com/0d0bd09c-ea97-46fb-b7b0-6e3e0a41dbc1">WSAAsyncGetServByPort</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

