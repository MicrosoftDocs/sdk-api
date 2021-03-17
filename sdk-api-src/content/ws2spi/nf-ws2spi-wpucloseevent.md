---
UID: NF:ws2spi.WPUCloseEvent
title: WPUCloseEvent function (ws2spi.h)
description: The WPUCloseEvent function closes an open event object handle.
helpviewer_keywords: ["WPUCloseEvent","WPUCloseEvent function [Winsock]","_win32_wpucloseevent_2","winsock.wpucloseevent_2","ws2spi/WPUCloseEvent"]
old-location: winsock\wpucloseevent_2.htm
tech.root: WinSock
ms.assetid: d8c6133b-e5a7-4936-a796-0930bb95fd0c
ms.date: 12/05/2018
ms.keywords: WPUCloseEvent, WPUCloseEvent function [Winsock], _win32_wpucloseevent_2, winsock.wpucloseevent_2, ws2spi/WPUCloseEvent
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
 - WPUCloseEvent
 - ws2spi/WPUCloseEvent
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
 - WPUCloseEvent
---

# WPUCloseEvent function


## -description

The 
**WPUCloseEvent** function closes an open event object handle.

## -parameters

### -param hEvent [in]

Handle to an open event object.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If the function succeeds, the return value is **TRUE**. Otherwise, the return value is **FALSE** and a specific error code is available in <i>lpErrno</i>.



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

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpucreateevent">WPUCreateEvent</a>

