---
UID: NF:ws2spi.WSCEnableNSProvider
title: WSCEnableNSProvider function
author: windows-sdk-content
description: Changes the state of a given namespace provider.
old-location: winsock\wscenablensprovider_2.htm
old-project: WinSock
ms.assetid: 2dff5af6-3011-4e3f-b812-fffaca8fa2d9
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: WSCEnableNSProvider, WSCEnableNSProvider function [Winsock], _win32_wscenablensprovider_2, winsock.wscenablensprovider_2, ws2spi/WSCEnableNSProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ws2spi.h
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
tech.root: 
req.typenames: WSC_PROVIDER_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSCEnableNSProvider
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSCEnableNSProvider function


## -description



			The 
<b>WSCEnableNSProvider</b> function changes the state of a given namespace provider. It is intended to give the end-user the ability to change the state of the namespace providers.


## -parameters




### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the namespace provider.


### -param fEnable [in]

A Boolean value that, if <b>TRUE</b>, the provider is set to the active state. If <b>FALSE</b>, the provider is disabled and will not be available for query operations or service registration.


## -returns




						If no error occurs, the 
<b>WSCEnableNSProvider</b> function returns <b>NO_ERROR</b> (zero). Otherwise, it returns <b>SOCKET_ERROR</b> if the function fails, and you must retrieve the appropriate error code using the 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProviderId</i> parameter points to memory that is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified namespace provider identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSASYSCALLFAILURE</a></b></dt>
</dl>
</td>
<td width="60%">
 A system call that should never fail has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
 Insufficient memory was available. This error is returned when there is insufficient memory to allocate a new catalog entry.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSCEnableNSProvider</b> function is intended to be used to change the state of the namespace providers. An independent software vendor (ISV) should not normally de-activate another ISV namespace provider in order to activate its own. The choice should be left to the user.    

The <b>WSCEnableNSProvider</b> function does not affect applications that are already running. Newly installed namespace providers will not be visible to applications nor will the changes in a namespace provider's activation state be visible. Applications launched after the call to 
<b>WSCEnableNSProvider</b> will see the changes.

The <b>WSCEnableNSProvider</b> function can only be called by a user logged on as a member of the Administrators group. If <b>WSCEnableNSProvider</b> is called by a user that is not a member of the Administrators group, the function call will fail. 
 

For computers running Windows Vista or Windows Server 2008, this function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to <b>requireAdministrator</b>. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.






## -see-also




<a href="https://msdn.microsoft.com/c2e5332f-3327-4624-96b4-8e321795961d">WSCEnumProtocols</a>



<a href="https://msdn.microsoft.com/f17f6174-879e-45e7-a250-975d1ee24fe0">WSCInstallNameSpace</a>



<a href="https://msdn.microsoft.com/5267f986-99fc-4e53-9fbb-3850bb9d24cf">WSCUnInstallNameSpace</a>



<a href="https://msdn.microsoft.com/00a06104-570f-4cd5-9520-bc73516ac7a5">WSCWriteNameSpaceOrder</a>
 

 

