---
UID: NF:winsock2.WSAProviderConfigChange
title: WSAProviderConfigChange function
author: windows-sdk-content
description: The WSAProviderConfigChange function notifies the application when the provider configuration is changed.
old-location: winsock\wsaproviderconfigchange_2.htm
tech.root: WinSock
ms.assetid: abaf367a-8f99-478c-a58c-d57e9f9cd8a1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: WSAProviderConfigChange, WSAProviderConfigChange function [Winsock], _win32_wsaproviderconfigchange_2, winsock.wsaproviderconfigchange_2, winsock2/WSAProviderConfigChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WSAProviderConfigChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSAProviderConfigChange function


## -description


The 
<b>WSAProviderConfigChange</b> function notifies the application when the provider configuration is changed.


## -parameters




### -param lpNotificationHandle [in, out]

Pointer to notification handle. If the notification handle is set to <b>NULL</b> (the handle value not the pointer itself), this function returns a notification handle in the location pointed to by <i>lpNotificationHandle</i>.


### -param lpOverlapped [in]

Pointer to a 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure.


### -param lpCompletionRoutine [in]

Pointer to the completion routine called when the provider change notification is received.


## -returns



If no error occurs the 
<b>WSAProviderConfigChange</b> returns 0. Otherwise, a value of SOCKET_ERROR is returned and a specific error code may be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>. The error code 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_IO_PENDING</a> indicates that the overlapped operation has been successfully initiated and that completion (and thus change event) will be indicated at a later time.

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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
Not enough free memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
Value pointed by <i>lpNotificationHandle</i> parameter is not a valid notification handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
Current operating system environment does not support provider installation or removal without restart.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAProviderConfigChange</b> function notifies the application of provider (both transport and namespace) installation or removal in Windows operating environments that support such configuration change without requiring a restart. When called for the first time (<i>lpNotificationHandle</i> parameter points to <b>NULL</b> handle), this function completes immediately and returns notification handle in the location pointed by <i>lpNotificationHandle</i> that can be used in subsequent calls to receive notifications of provider installation and removal. The second and any subsequent calls only complete when provider information changes since the time the call was made It is expected (but not required) that the application uses overlapped I/O on second and subsequent calls to 
<b>WSAProviderConfigChange</b>, in which case the call will return immediately and application will be notified of provider configuration changes using the completion mechanism chosen through specified overlapped completion parameters.

Notification handle returned by 
<b>WSAProviderConfigChange</b> is like any regular operating system handle that should be closed (when no longer needed) using Windows 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> call.

The following sequence of actions can be used to guarantee that application always has current protocol configuration information:

<ul>
<li>Call <b>WSAProviderConfigChange</b></li>
<li>Call 
<a href="https://msdn.microsoft.com/928b6937-41a3-4268-a3bc-14c9e04870e4">WSAEnumProtocols</a> and/or 
<a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>
</li>
<li>Whenever 
<b>WSAProviderConfigChange</b> notifies application of provider configuration change (through blocking or overlapped I/O), the whole sequence of actions should be repeated.</li>
</ul>
<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This   function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>



<a href="https://msdn.microsoft.com/928b6937-41a3-4268-a3bc-14c9e04870e4">WSAEnumProtocols</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

