---
UID: NF:tapi.lineSetLineDevStatus
title: lineSetLineDevStatus function
author: windows-sdk-content
description: The lineSetLineDevStatus function sets the line device status.
old-location: tapi2\linesetlinedevstatus.htm
tech.root: tapi
ms.assetid: c8eb142d-5160-49f3-81c1-61094c180df8
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "_tapi2_linesetlinedevstatus, lineSetLineDevStatus, lineSetLineDevStatus function [TAPI 2.2], tapi/lineSetLineDevStatus, tapi2.linesetlinedevstatus"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetLineDevStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetLineDevStatus function


## -description


The 
<b>lineSetLineDevStatus</b> function sets the line device status. Except for basic parameter validation, it is a straight pass-through to the service provider. The service provider sends a 
<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a> message to inform applications of the new state, when set; TAPI does not synthesize these messages.


## -parameters




### -param hLine

Handle to the line device.


### -param dwStatusToChange

One or more of the 
<a href="https://msdn.microsoft.com/5fa754d3-07b2-4b75-91ef-1bf961d9fef4">LINEDEVSTATUSFLAGS_ Constants</a>.


### -param fStatus

<b>TRUE</b> (–1) to turn on the indicated status bit(s), <b>FALSE</b> (0) to turn off.


## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALLINESTATE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONUNAVAIL, LINEERR_OPERATIONFAILED, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.



