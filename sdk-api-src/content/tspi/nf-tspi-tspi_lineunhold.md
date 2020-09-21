---
UID: NF:tspi.TSPI_lineUnhold
title: TSPI_lineUnhold function (tspi.h)
description: The TSPI_lineUnhold function retrieves the specified held call.
helpviewer_keywords: ["TSPI_lineUnhold","TSPI_lineUnhold function [TAPI 2.2]","_tspi_tspi_lineunhold","tspi.tspi_lineunhold","tspi/TSPI_lineUnhold"]
old-location: tspi\tspi_lineunhold.htm
tech.root: tapi3
ms.assetid: 4719c399-0dce-4aa2-9b6e-a84ad13f9228
ms.date: 12/05/2018
ms.keywords: TSPI_lineUnhold, TSPI_lineUnhold function [TAPI 2.2], _tspi_tspi_lineunhold, tspi.tspi_lineunhold, tspi/TSPI_lineUnhold
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
 - TSPI_lineUnhold
 - tspi/TSPI_lineUnhold
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
 - TSPI_lineUnhold
---

# TSPI_lineUnhold function


## -description

The 
<b>TSPI_lineUnhold</b> function retrieves the specified held call.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The handle to the call to be retrieved. The call state of <i>hdCall</i> can be <i>onHold</i>.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

The service provider returns LINEERR_INVALCALLSTATE if the call is not currently on hold.

This operation works for calls on hard hold (calls placed on hold using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linehold">TSPI_lineHold</a>) and on soft hold. The service provider should check that the call is currently in the <i>onHold</i>, <i>onHoldPendingTransfer</i>, or <i>onHoldPendingConference</i> state, change the state to <i>connected</i>, and send a LINECALLSTATE message for the new call state.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linehold">TSPI_lineHold</a>