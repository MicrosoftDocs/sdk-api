---
UID: NF:winsock2.WSACreateEvent
title: WSACreateEvent function
author: windows-sdk-content
description: The WSACreateEvent function creates a new event object.
old-location: winsock\wsacreateevent_2.htm
old-project: winsock
ms.assetid: cff3bc31-f34c-4bb2-9004-5ec31d0a704a
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WSACreateEvent, WSACreateEvent function [Winsock], _win32_wsacreateevent_2, winsock.wsacreateevent_2, winsock2/WSACreateEvent
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
 - WSACreateEvent
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSACreateEvent function


## -description



			The 
<b>WSACreateEvent</b> function creates a new event object.


## -parameters






## -returns



If no error occurs, 
<b>WSACreateEvent</b> returns the handle of the event object. Otherwise, the return value is WSA_INVALID_EVENT. To get extended error information, call 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
Not enough free memory available to create the event object.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSACreateEvent</b> function creates a manual-reset event object with an initial state of nonsignaled. The handle of the event object returned cannot be inherited by child processes. 
The event object is unnamed.

The <a href="https://msdn.microsoft.com/8a3f41fe-77da-4e4e-975d-00eec7c11446">WSASetEvent</a> function can be called to set the state of the event object to signaled. The <a href="https://msdn.microsoft.com/99a8b0f3-977f-44cd-a224-0819d7513c90">WSAResetEvent</a> function can be called to set the state of the event object to nonsignaled. When an event object is no longer needed, the <a href="https://msdn.microsoft.com/40cefe46-10a3-4b6a-8c89-3e16237fc685">WSACloseEvent</a> function should be called to free the resources associated with the event object.

Windows Sockets 2 event objects are system objects in Windows environments. Therefore, if a Windows application wants to use an auto-reset event rather than a manual-reset event, the application can call the <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function directly. The scope of an event object is limited to the process in which it is created.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/40cefe46-10a3-4b6a-8c89-3e16237fc685">WSACloseEvent</a>



<a href="https://msdn.microsoft.com/2e6abccd-c82c-4a6b-8720-259986ac9984">WSAEnumNetworkEvents</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>



<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>



<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>



<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a>



<a href="https://msdn.microsoft.com/99a8b0f3-977f-44cd-a224-0819d7513c90">WSAResetEvent</a>



<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>



<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a>



<a href="https://msdn.microsoft.com/8a3f41fe-77da-4e4e-975d-00eec7c11446">WSASetEvent</a>



<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

