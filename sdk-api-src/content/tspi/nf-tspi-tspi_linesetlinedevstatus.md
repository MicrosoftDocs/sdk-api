---
UID: NF:tspi.TSPI_lineSetLineDevStatus
title: TSPI_lineSetLineDevStatus function (tspi.h)
description: The TSPI_lineSetLineDevStatus service provider sets the device status as indicated, sending appropriate LINE_LINEDEVSTATE messages to indicate the new status.
helpviewer_keywords: ["TSPI_lineSetLineDevStatus","TSPI_lineSetLineDevStatus function [TAPI 2.2]","_tspi_tspi_linesetlinedevstatus","tspi.tspi_linesetlinedevstatus","tspi/TSPI_lineSetLineDevStatus"]
old-location: tspi\tspi_linesetlinedevstatus.htm
tech.root: tapi3
ms.assetid: 82afe6fd-a9fd-4e53-a460-370cab404366
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetLineDevStatus, TSPI_lineSetLineDevStatus function [TAPI 2.2], _tspi_tspi_linesetlinedevstatus, tspi.tspi_linesetlinedevstatus, tspi/TSPI_lineSetLineDevStatus
req.header: tspi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineSetLineDevStatus
 - tspi/TSPI_lineSetLineDevStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSetLineDevStatus
---

# TSPI_lineSetLineDevStatus function


## -description

The 
<b>TSPI_lineSetLineDevStatus</b> service provider sets the device status as indicated, sending appropriate 
<a href="/previous-versions/windows/desktop/legacy/ms725231(v=vs.85)">LINE_LINEDEVSTATE</a> messages to indicate the new status.

## -parameters

### -param dwRequestID

Identifier for reporting asynchronous function results.

### -param hdLine

The service provider's handle to the line device.

### -param dwStatusToChange

One or more of the 
<a href="/windows/desktop/Tapi/linedevstatusflags--constants">LINEDEVSTATUSFLAGS_ constants</a>.

### -param fStatus

<b>TRUE</b> to turn on the indicated status bit(s), <b>FALSE</b> to turn off.

## -returns

Returns <b>dwRequestID</b> if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALLINESTATE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_RESOURCEUNAVAIL.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms725231(v=vs.85)">LINE_LINEDEVSTATE</a>