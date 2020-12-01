---
UID: NF:tspi.TSPI_lineSwapHold
title: TSPI_lineSwapHold function (tspi.h)
description: The TSPI_lineSwapHold function swaps the specified active call with the specified call on consultation hold.
helpviewer_keywords: ["TSPI_lineSwapHold","TSPI_lineSwapHold function [TAPI 2.2]","_tspi_tspi_lineswaphold","tspi.tspi_lineswaphold","tspi/TSPI_lineSwapHold"]
old-location: tspi\tspi_lineswaphold.htm
tech.root: tapi3
ms.assetid: 9ecd6a63-e906-483b-b404-28797d259149
ms.date: 12/05/2018
ms.keywords: TSPI_lineSwapHold, TSPI_lineSwapHold function [TAPI 2.2], _tspi_tspi_lineswaphold, tspi.tspi_lineswaphold, tspi/TSPI_lineSwapHold
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
 - TSPI_lineSwapHold
 - tspi/TSPI_lineSwapHold
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
 - TSPI_lineSwapHold
---

# TSPI_lineSwapHold function


## -description

The 
<b>TSPI_lineSwapHold</b> function swaps the specified active call with the specified call on consultation hold.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdActiveCall

The handle to the call to be swapped with the call on consultation hold. The call state of <i>hdActiveCall</i> can be <i>connected</i>.

### -param hdHeldCall

The handle to the consultation call. The call state of <i>hdHeldCall</i> can be <i>onHoldPendingTransfer</i>, <i>onHoldPendingConference</i>, or <i>onHold</i>.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

The service provider must send 
<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a> messages for the call transitions.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetuptransfer">TSPI_lineSetupTransfer</a>