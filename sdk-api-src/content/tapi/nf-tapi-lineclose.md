---
UID: NF:tapi.lineClose
title: lineClose function
author: windows-sdk-content
description: The lineClose function closes the specified open line device.
old-location: tapi2\lineclose.htm
old-project: tapi
ms.assetid: ec47a351-c693-4e71-bf23-c31110ca90a1
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_lineclose, lineClose, lineClose function [TAPI 2.2], tapi/lineClose, tapi2.lineclose"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineClose
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineClose function


## -description


The 
<b>lineClose</b> function closes the specified open line device.


## -parameters




### -param hLine

Handle to the open line device to be closed. After the line has been successfully closed, this handle is no longer valid.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL.




## -remarks



If an application calls 
<b>lineClose</b> while it still has active calls on the opened line, the application's ownership of these calls is revoked. If the application was the sole owner of these calls, the calls are dropped as well. It is good programming practice for an application to dispose of the calls it owns on an opened line by explicitly relinquishing ownership and/or by dropping these calls prior to closing the line.

If the line was closed successfully, a 
<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a> message is sent to all applications that are monitoring the line status of open/close changes. Outstanding asynchronous replies are suppressed.

Service providers may find it useful or necessary to forcibly reclaim line devices from an application that has the line open. This can be useful to prevent an application from monopolizing the line device for too long. If this happens, a LINE_CLOSE message is sent to the application, specifying the line handle of the line device that was closed.

The 
<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a> function allocates resources to the invoking application, and applications can be prevented from opening a line if resources are unavailable. Therefore, an application that only occasionally uses a line device (such as for making outgoing calls) should close the line to free resources and allow other applications to open the line.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/f254e331-d574-4fa7-8447-6e4535d3d773">LINE_CLOSE</a>



<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a>
 

 

