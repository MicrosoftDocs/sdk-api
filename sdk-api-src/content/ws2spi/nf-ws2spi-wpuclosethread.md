---
UID: NF:ws2spi.WPUCloseThread
title: WPUCloseThread function (ws2spi.h)
description: The WPUCloseThread function closes a thread opened with a call to WPUOpenCurrentThread.
helpviewer_keywords: ["WPUCloseThread","WPUCloseThread function [Winsock]","_win32_wpuclosethread_2","winsock.wpuclosethread_2","ws2spi/WPUCloseThread"]
old-location: winsock\wpuclosethread_2.htm
tech.root: WinSock
ms.assetid: 1a5e7a99-484f-4862-bd28-edf85debc8e5
ms.date: 12/05/2018
ms.keywords: WPUCloseThread, WPUCloseThread function [Winsock], _win32_wpuclosethread_2, winsock.wpuclosethread_2, ws2spi/WPUCloseThread
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
 - WPUCloseThread
 - ws2spi/WPUCloseThread
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
 - WPUCloseThread
---

# WPUCloseThread function


## -description

The 
**WPUCloseThread** function closes a thread opened with a call to 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a>.

## -parameters

### -param lpThreadId [in]

Pointer to a 
<a href="/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a> structure that identifies the thread context. This structure must have been initialized by a previous call to 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a>.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a> returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.



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
**WPUCloseThread** function is used in a layered service provider to deallocate the resources that were initiated in a call by the 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a> function. The 
<a href="/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a> structure in the <i>lpThreadId</i> is the thread to deallocate.

Every call to 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a> must have a call to 
**WPUCloseThread**. These two functions are used when the overlapped functions, such as 
[LPWSPSend](nc-ws2spi-lpwspsend.md), are called in a lower layer of the service provider than the current thread.

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuopencurrentthread">WPUOpenCurrentThread</a>



<a href="/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a>

