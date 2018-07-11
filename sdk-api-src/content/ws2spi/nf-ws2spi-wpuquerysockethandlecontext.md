---
UID: NF:ws2spi.WPUQuerySocketHandleContext
title: WPUQuerySocketHandleContext function
author: windows-sdk-content
description: The WPUQuerySocketHandleContext function queries the context value associated with the specified socket handle.
old-location: winsock\wpuquerysockethandlecontext_2.htm
old-project: WinSock
ms.assetid: 661ddff0-b80c-4e24-84b3-b444ef1c2ad6
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: WPUQuerySocketHandleContext, WPUQuerySocketHandleContext function [Winsock], _win32_wpuquerysockethandlecontext_2, winsock.wpuquerysockethandlecontext_2, ws2spi/WPUQuerySocketHandleContext
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
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WPUQuerySocketHandleContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WPUQuerySocketHandleContext function


## -description



			The 
<b>WPUQuerySocketHandleContext</b> function queries the context value associated with the specified socket handle.


## -parameters




### -param s [in]

Description that identifies the socket whose context is to be queried.


### -param lpContext [out]

Pointer that will receive the context value.


### -param lpErrno [out]

Pointer to the error code.


## -returns




						If no error occurs, 
<b>WPUQuerySocketHandleContext</b> returns zero and stores the current context value in <i>lpContext</i>. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket created by 
<a href="https://msdn.microsoft.com/ecbf9d8b-b705-4160-ac77-afa5b1501534">WPUCreateSocketHandle</a>.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The 
<b>WPUQuerySocketHandleContext</b> function queries the current context value associated with the specified socket handle. Service providers typically use this function to retrieve a pointer to provider-specific data associated with the socket. For example, a service provider can use the socket context to store a pointer to a structure containing the socket's state, local and remote transport addresses, and event objects for signaling network events.

Only non-IFS providers use this function, because IFS providers are not able to supply a context value.




## -see-also




<a href="https://msdn.microsoft.com/ecbf9d8b-b705-4160-ac77-afa5b1501534">WPUCreateSocketHandle</a>
 

 

