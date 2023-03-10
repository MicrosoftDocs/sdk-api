---
UID: NF:tspi.TSPI_linePrepareAddToConference
title: TSPI_linePrepareAddToConference function (tspi.h)
description: The TSPI_linePrepareAddToConference function prepares an existing conference call for the addition of another party. It creates a new, temporary consultation call. The new consultation call can be subsequently added to the conference call.
helpviewer_keywords: ["TSPI_linePrepareAddToConference","TSPI_linePrepareAddToConference function [TAPI 2.2]","_tspi_tspi_lineprepareaddtoconference","tspi.tspi_lineprepareaddtoconference","tspi/TSPI_linePrepareAddToConference"]
old-location: tspi\tspi_lineprepareaddtoconference.htm
tech.root: tapi3
ms.assetid: 84642d7d-7673-45f1-91fb-aede75e51029
ms.date: 12/05/2018
ms.keywords: TSPI_linePrepareAddToConference, TSPI_linePrepareAddToConference function [TAPI 2.2], _tspi_tspi_lineprepareaddtoconference, tspi.tspi_lineprepareaddtoconference, tspi/TSPI_linePrepareAddToConference
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
 - TSPI_linePrepareAddToConference
 - tspi/TSPI_linePrepareAddToConference
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
 - TSPI_linePrepareAddToConference
---

# TSPI_linePrepareAddToConference function


## -description

The 
<b>TSPI_linePrepareAddToConference</b> function prepares an existing conference call for the addition of another party. It creates a new, temporary consultation call. The new consultation call can be subsequently added to the conference call.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdConfCall

The handle to a conference call. The call state of <i>hdConfCall</i> can be <i>connected</i>.

### -param htConsultCall

The TAPI handle to the new, temporary consultation call. The service provider must save this and use it in all subsequent calls to the 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> procedure reporting events on the new call. The call state of <i>hdAddCall</i> is not applicable.

### -param lphdConsultCall

A pointer to an 
<a href="/windows/desktop/Tapi/hdrvline">HDRVCALL</a> representing the service provider's identifier for the new, temporary consultation call. The service provider must fill this location with its handle for the new call before this procedure returns. This handle is invalid if the function results in an error.

### -param lpCallParams

A pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> containing call parameters to use when establishing the consultation call. This parameter is set to <b>NULL</b> if no special call setup parameters are desired.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_BEARERMODEUNAVAIL, LINEERR_INVALLINESTATE, LINEERR_CALLUNAVAIL, LINEERR_INVALMEDIAMODE, LINEERR_CONFERENCEFULL, LINEERR_INVALRATE, LINEERR_INUSE, LINEERR_NOMEM, LINEERR_INVALADDRESSMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALBEARERMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLPARAMS, LINEERR_RATEUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCONFCALLHANDLE, LINEERR_USERUSERINFOTOOBIG.

## -remarks

The service provider returns LINEERR_INVALLINESTATE if the line is currently not in a state in which this operation can be performed. The service provider must indicate a list of currently valid operations in the <b>dwLineFeatures</b> member (of the type <b>LINEFEATURE</b>) in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a> structure.

The service provider returns LINEERR_INVALCALLSTATE if the conference call is not in a valid state for the requested operation.

This function places an existing conference call in the <i>onHoldPendingConference</i> state and creates a consultation call that can be added later to the existing conference call with 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineaddtoconference">TSPI_lineAddToConference</a>.

The consultation call can be canceled using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedrop">TSPI_lineDrop</a>. It may also be possible for TAPI to swap between the consultation call and the held conference call with 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineswaphold">TSPI_lineSwapHold</a>. The service provider initially does media monitoring on the new call for at least the set of media types that were monitored for on the line.

This function differs from the corresponding TAPI function in that it follows the TSPI model for beginning the lifetime of a call. TAPI and the service provider exchange opaque handles representing the call with one another. In addition, the service provider is permitted to do callbacks for the new call before it returns from this procedure. In any case, the service provider must also treat the handle it returned as "not yet valid" until after the matching 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> message reports success. In other words, it must not issue any 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> messages for the new call or include it in call counts in messages or status data structures for the line.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevstatus">LINEDEVSTATUS</a>



<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineaddtoconference">TSPI_lineAddToConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedial">TSPI_lineDial</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedrop">TSPI_lineDrop</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineremovefromconference">TSPI_lineRemoveFromConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetupconference">TSPI_lineSetupConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineswaphold">TSPI_lineSwapHold</a>