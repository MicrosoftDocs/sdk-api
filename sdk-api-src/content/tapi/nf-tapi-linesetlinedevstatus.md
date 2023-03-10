---
UID: NF:tapi.lineSetLineDevStatus
title: lineSetLineDevStatus function (tapi.h)
description: The lineSetLineDevStatus function sets the line device status.
helpviewer_keywords: ["_tapi2_linesetlinedevstatus","lineSetLineDevStatus","lineSetLineDevStatus function [TAPI 2.2]","tapi/lineSetLineDevStatus","tapi2.linesetlinedevstatus"]
old-location: tapi2\linesetlinedevstatus.htm
tech.root: tapi3
ms.assetid: c8eb142d-5160-49f3-81c1-61094c180df8
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetlinedevstatus, lineSetLineDevStatus, lineSetLineDevStatus function [TAPI 2.2], tapi/lineSetLineDevStatus, tapi2.linesetlinedevstatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineSetLineDevStatus
 - tapi/lineSetLineDevStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetLineDevStatus
---

# lineSetLineDevStatus function


## -description

The 
<b>lineSetLineDevStatus</b> function sets the line device status. Except for basic parameter validation, it is a straight pass-through to the service provider. The service provider sends a 
<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a> message to inform applications of the new state, when set; TAPI does not synthesize these messages.

## -parameters

### -param hLine

Handle to the line device.

### -param dwStatusToChange

One or more of the 
<a href="/windows/desktop/Tapi/linedevstatusflags--constants">LINEDEVSTATUSFLAGS_ Constants</a>.

### -param fStatus

<b>TRUE</b> (–1) to turn on the indicated status bit(s), <b>FALSE</b> (0) to turn off.

## -returns

Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALLINEHANDLE, LINEERR_INVALLINESTATE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONUNAVAIL, LINEERR_OPERATIONFAILED, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.