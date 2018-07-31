---
UID: NF:winsock2.WSAResetEvent
title: WSAResetEvent function
author: windows-sdk-content
description: The WSAResetEvent function resets the state of the specified event object to nonsignaled.
old-location: winsock\wsaresetevent_2.htm
old-project: WinSock
ms.assetid: 99a8b0f3-977f-44cd-a224-0819d7513c90
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WSAResetEvent, WSAResetEvent function [Winsock], _win32_wsaresetevent_2, winsock.wsaresetevent_2, winsock2/WSAResetEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: 
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
tech.root: 
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAResetEvent
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAResetEvent function


## -description


The 
<b>WSAResetEvent</b> function resets the state of the specified event object to nonsignaled.


## -parameters




### -param hEvent [in]

A handle that identifies an open event object handle.


## -returns



If the 
<b>WSAResetEvent</b> function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call 
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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> parameter is not a valid event object handle.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAResetEvent</b> function is used to set the state of the event object to nonsignaled.

The proper way to reset the state of an event object used with the <a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a> function is to pass the handle of the event object to the <a href="https://msdn.microsoft.com/2e6abccd-c82c-4a6b-8720-259986ac9984">WSAEnumNetworkEvents</a> function in the <i>hEventObject</i> parameter. This will reset the event object and adjust the status of active FD events on the socket in an atomic fashion.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/40cefe46-10a3-4b6a-8c89-3e16237fc685">WSACloseEvent</a>



<a href="https://msdn.microsoft.com/cff3bc31-f34c-4bb2-9004-5ec31d0a704a">WSACreateEvent</a>



<a href="https://msdn.microsoft.com/2e6abccd-c82c-4a6b-8720-259986ac9984">WSAEnumNetworkEvents</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>



<a href="https://msdn.microsoft.com/8a3f41fe-77da-4e4e-975d-00eec7c11446">WSASetEvent</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

