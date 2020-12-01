---
UID: NF:ws2spi.WPUQuerySocketHandleContext
title: WPUQuerySocketHandleContext function (ws2spi.h)
description: The WPUQuerySocketHandleContext function queries the context value associated with the specified socket handle.
helpviewer_keywords: ["WPUQuerySocketHandleContext","WPUQuerySocketHandleContext function [Winsock]","_win32_wpuquerysockethandlecontext_2","winsock.wpuquerysockethandlecontext_2","ws2spi/WPUQuerySocketHandleContext"]
old-location: winsock\wpuquerysockethandlecontext_2.htm
tech.root: WinSock
ms.assetid: 661ddff0-b80c-4e24-84b3-b444ef1c2ad6
ms.date: 12/05/2018
ms.keywords: WPUQuerySocketHandleContext, WPUQuerySocketHandleContext function [Winsock], _win32_wpuquerysockethandlecontext_2, winsock.wpuquerysockethandlecontext_2, ws2spi/WPUQuerySocketHandleContext
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WPUQuerySocketHandleContext
 - ws2spi/WPUQuerySocketHandleContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WPUQuerySocketHandleContext
---

# WPUQuerySocketHandleContext function


## -description

The 
**WPUQuerySocketHandleContext** function queries the context value associated with the specified socket handle.

## -parameters

### -param s [in]

Description that identifies the socket whose context is to be queried.

### -param lpContext [out]

Pointer that will receive the context value.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
**WPUQuerySocketHandleContext** returns zero and stores the current context value in <i>lpContext</i>. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dl>
</dl>
</td>
<td width="60%">
The descriptor is not a socket created by 
<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
**WPUQuerySocketHandleContext** function queries the current context value associated with the specified socket handle. Service providers typically use this function to retrieve a pointer to provider-specific data associated with the socket. For example, a service provider can use the socket context to store a pointer to a structure containing the socket's state, local and remote transport addresses, and event objects for signaling network events.

Only non-IFS providers use this function, because IFS providers are not able to supply a context value.

## -see-also

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>

