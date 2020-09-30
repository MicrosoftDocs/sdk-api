---
UID: NF:ws2spi.WPUResetEvent
title: WPUResetEvent function (ws2spi.h)
description: The WPUResetEvent function resets the state of the specified event object to nonsignaled. This call is safe for use within interrupt context.
helpviewer_keywords: ["WPUResetEvent","WPUResetEvent function [Winsock]","_win32_wpuresetevent_2","winsock.wpuresetevent_2","ws2spi/WPUResetEvent"]
old-location: winsock\wpuresetevent_2.htm
tech.root: WinSock
ms.assetid: a3385c77-899c-4772-88b9-fb3e0fab54e0
ms.date: 12/05/2018
ms.keywords: WPUResetEvent, WPUResetEvent function [Winsock], _win32_wpuresetevent_2, winsock.wpuresetevent_2, ws2spi/WPUResetEvent
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
 - WPUResetEvent
 - ws2spi/WPUResetEvent
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
 - WPUResetEvent
---

# WPUResetEvent function


## -description

The 
**WPUResetEvent** function resets the state of the specified event object to nonsignaled. This call is safe for use within interrupt context.

## -parameters

### -param hEvent [in]

Handle that identifies an open event object.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, the 
**WPUResetEvent** function returns the value **TRUE**. Otherwise, **FALSE** is returned, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> parameter is not a valid event object handle.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpucloseevent">WPUCloseEvent</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpucreateevent">WPUCreateEvent</a>



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpusetevent">WPUSetEvent</a>

