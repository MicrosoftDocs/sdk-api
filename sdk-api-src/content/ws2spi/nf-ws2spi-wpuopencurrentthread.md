---
UID: NF:ws2spi.WPUOpenCurrentThread
title: WPUOpenCurrentThread function (ws2spi.h)
description: The WPUOpenCurrentThread function opens a handle to the current thread that can be used with overlapped functions in a layered service provider.
helpviewer_keywords: ["WPUOpenCurrentThread","WPUOpenCurrentThread function [Winsock]","_win32_wpuopencurrentthread_2","winsock.wpuopencurrentthread_2","ws2spi/WPUOpenCurrentThread"]
old-location: winsock\wpuopencurrentthread_2.htm
tech.root: WinSock
ms.assetid: 92d21f29-240f-407e-89a7-bbbb8f9bf0eb
ms.date: 12/05/2018
ms.keywords: WPUOpenCurrentThread, WPUOpenCurrentThread function [Winsock], _win32_wpuopencurrentthread_2, winsock.wpuopencurrentthread_2, ws2spi/WPUOpenCurrentThread
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
 - WPUOpenCurrentThread
 - ws2spi/WPUOpenCurrentThread
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
 - WPUOpenCurrentThread
---

# WPUOpenCurrentThread function


## -description

The 
**WPUOpenCurrentThread** function opens a handle to the current thread that can be used with overlapped functions in a layered service provider. This is intended to be used by layered service providers that wish to initiate overlapped I/O from nonapplication threads.

## -parameters

### -param lpThreadId [out]

Pointer to a 
<a href="/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a> structure that can then be passed to an overlapped function.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
**WPUOpenCurrentThread** returns the zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dl>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a> call must occur before using this function.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
**WPUOpenCurrentThread** function provides a pointer to a 
<a href="/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a> structure that can then be passed to an overlapped function such as 
[LPWSPSend](nc-ws2spi-lpwspsend.md) or 
[LPWSPRecv](nc-ws2spi-lpwsprecv.md). Layered service providers using a private thread in one of the upper layers will use 
**WPUOpenCurrentThread** to pass a 
**WSATHREADID** pointer to the lower layer that is administering overlapped functions.

Overlapped functions such as 
[LPWSPSend](nc-ws2spi-lpwspsend.md) and 
[LPWSPRecv](nc-ws2spi-lpwsprecv.md) can then be used in the same way as a regular service provider.

Every call to 
**WPUOpenCurrentThread** must have a corresponding call to 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosethread">WPUCloseThread</a>.

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuclosethread">WPUCloseThread</a>



[LPWSPRecv](nc-ws2spi-lpwsprecv.md)



[LPWSPSend](nc-ws2spi-lpwspsend.md)

