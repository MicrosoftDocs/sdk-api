---
UID: NF:tspi.TSPI_lineHold
title: TSPI_lineHold function (tspi.h)
description: The TSPI_lineHold function places the specified call on hold.
helpviewer_keywords: ["TSPI_lineHold","TSPI_lineHold function [TAPI 2.2]","_tspi_tspi_linehold","tspi.tspi_linehold","tspi/TSPI_lineHold"]
old-location: tspi\tspi_linehold.htm
tech.root: tapi3
ms.assetid: 395aa8cc-fdbf-4772-940b-ea5944b26812
ms.date: 12/05/2018
ms.keywords: TSPI_lineHold, TSPI_lineHold function [TAPI 2.2], _tspi_tspi_linehold, tspi.tspi_linehold, tspi/TSPI_lineHold
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
 - TSPI_lineHold
 - tspi/TSPI_lineHold
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
 - TSPI_lineHold
---

# TSPI_lineHold function


## -description

The 
<b>TSPI_lineHold</b> function places the specified call on hold.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The service provider's handle to the call to be placed on hold. The call state of <i>hdCall</i> can be <i>connected</i>.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

The call on hold is temporarily disconnected, allowing TAPI to use the line device for making or answering other calls. 
<b>TSPI_lineHold</b> performs a <i>hard hold</i> of the specified call, as opposed to a <i>consultation call</i>. A call on hard hold typically cannot be transferred or included in a conference call, whereas a consultation call can. Consultation calls are initiated using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetuptransfer">TSPI_lineSetupTransfer</a>, 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a>, or 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineprepareaddtoconference">TSPI_linePrepareAddToConference</a>.

After a call is successfully placed on hold, the call state typically transitions to <i>onHold</i>. A held call is retrieved through 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineunhold">TSPI_lineUnhold</a>. While a call is on hold, the service provider can send 
<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a> messages about state changes of the held call. For example, if the held party hangs up, the call state can transition to <i>disconnected</i>, and the service provider can send a LINE_CALLSTATE message indicating the new state.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetuptransfer">TSPI_lineSetupTransfer</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineunhold">TSPI_lineUnhold</a>