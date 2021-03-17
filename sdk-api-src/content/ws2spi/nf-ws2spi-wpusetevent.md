---
UID: NF:ws2spi.WPUSetEvent
title: WPUSetEvent function (ws2spi.h)
description: The WPUSetEvent function sets the state of the specified event object to signaled. This call is safe for use within interrupt context.
helpviewer_keywords: ["WPUSetEvent","WPUSetEvent function [Winsock]","_win32_wpusetevent_2","winsock.wpusetevent_2","ws2spi/WPUSetEvent"]
old-location: winsock\wpusetevent_2.htm
tech.root: WinSock
ms.assetid: d5caa926-1223-4917-85ba-4f79731e955a
ms.date: 12/05/2018
ms.keywords: WPUSetEvent, WPUSetEvent function [Winsock], _win32_wpusetevent_2, winsock.wpusetevent_2, ws2spi/WPUSetEvent
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
 - WPUSetEvent
 - ws2spi/WPUSetEvent
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
 - WPUSetEvent
---

# WPUSetEvent function


## -description

The 
**WPUSetEvent** function sets the state of the specified event object to signaled. This call is safe for use within interrupt context.

## -parameters

### -param hEvent [in]

Handle that identifies an open event object.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, the 
**WPUSetEvent** function returns the value **TRUE**. Otherwise, **FALSE** is returned, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dl>
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



<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpuresetevent">WPUResetEvent</a>

