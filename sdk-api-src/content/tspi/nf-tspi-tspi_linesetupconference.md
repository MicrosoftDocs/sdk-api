---
UID: NF:tspi.TSPI_lineSetupConference
title: TSPI_lineSetupConference function (tspi.h)
description: The TSPI_lineSetupConference function sets up a conference call for the addition of the third party.
helpviewer_keywords: ["TSPI_lineSetupConference","TSPI_lineSetupConference function [TAPI 2.2]","_tspi_tspi_linesetupconference","tspi.tspi_linesetupconference","tspi/TSPI_lineSetupConference"]
old-location: tspi\tspi_linesetupconference.htm
tech.root: tapi3
ms.assetid: 71b9720b-54dc-44a7-9fad-38dcd9f57ab3
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetupConference, TSPI_lineSetupConference function [TAPI 2.2], _tspi_tspi_linesetupconference, tspi.tspi_linesetupconference, tspi/TSPI_lineSetupConference
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
 - TSPI_lineSetupConference
 - tspi/TSPI_lineSetupConference
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
 - TSPI_lineSetupConference
---

# TSPI_lineSetupConference function


## -description

The 
<b>TSPI_lineSetupConference</b> function sets up a conference call for the addition of the third party.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The handle to the initial call that identifies the first party of a conference call. In some environments, a call must exist in order to start a conference call. In other telephony environments, no call initially exists and <i>hdCall</i> is left <b>NULL</b>. The call state of <i>hdCall</i> can be <i>connected</i>.

### -param hdLine

The handle to the line device on which to originate the conference call if <i>hdCall</i> is <b>NULL</b>. The <i>hdLine</i> parameter is ignored if <i>hdCall</i> is non-<b>NULL</b>. The service provider reports which model it supports through the <b>setupConfNull</b> flag of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> data structure.

### -param htConfCall

The TAPI handle to the new conference call. The service provider must save this and use it in all subsequent calls to the 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> procedure reporting events on the new call.

### -param lphdConfCall

A pointer to an 
<a href="/windows/desktop/Tapi/hdrvline">HDRVCALL</a> representing the service provider's identifier for the newly created conference call. The service provider must fill this location with its handle for the new call before this procedure returns. This handle is ignored by TAPI if the function results in an error. The call state of <i>hdConfCall</i> is not applicable.

### -param htConsultCall

The TAPI handle to the consultation call. When setting up a call for the addition of a new party, a new temporary call (consultation call) is automatically allocated. The service provider must save the <i>htConsultCall</i> and use it in all subsequent calls to the 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> procedure reporting events on the new consultation call.

### -param lphdConsultCall

A pointer to an 
<a href="/windows/desktop/Tapi/hdrvline">HDRVCALL</a> representing the service provider's identifier for a call. When setting up a call for the addition of a new party, a new temporary call (consultation call) is automatically allocated. The service provider must fill this location with its handle for the new consultation call before this procedure returns. This handle is ignored by TAPI if the function results in an error. The call state of <i>hdConsultCall</i> is not applicable.

### -param dwNumParties

The expected number of parties in the conference call. The service provider is free to do with this number as it pleases. For example, the service provider can ignore it, or use it as a hint to allocate the right size conference bridge inside the switch. TAPI does not validate this parameter when this function is called.

### -param lpCallParams

A pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> structure containing call parameters to use when establishing the consultation call. This parameter is set to <b>NULL</b> if no special call setup parameters are desired and the service provider uses default parameters.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_INVALADDRESSMODE, LINEERR_INVALLINEHANDLE, LINEERR_INVALBEARERMODE, LINEERR_INVALCALLSTATE, LINEERR_INVALCALLPARAMS, LINEERR_CALLUNAVAIL, LINEERR_INVALLINESTATE, LINEERR_CONFERENCEFULL, LINEERR_INVALMEDIAMODE, LINEERR_NOMEM, LINEERR_INVALRATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INUSE, LINEERR_OPERATIONFAILED, LINEERR_RATEUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_USERUSERINFOTOOBIG, LINEERR_BEARERMODEUNAVAIL.

## -remarks

The service provider returns LINEERR_INVALLINEHANDLE if the specified line handle for the line containing the conference call is invalid. This error can also indicate that the telephony environment requires an initial line to set up a conference but a non-<b>NULL</b> call handle was supplied instead.

The service provider returns LINEERR_INVALCALLHANDLE if the telephony environment requires an initial call to set up a conference but a <b>NULL</b> call handle was supplied instead.

<b>TSPI_lineSetupConference</b> provides two ways to establish a new conference call, depending on whether a normal two-party call is required to pre-exist or not. When setting up a conference call from an existing two-party call, the <i>hdCall</i> parameter is a valid call handle that is initially added to the conference call by the 
<b>TSPI_lineSetupConference</b> request and <i>hdLine</i> is ignored. On switches where conference call setup does not start with an existing call, <i>hdCall</i> must be <b>NULL</b> and <i>hdLine</i> must be specified to identify the line device on which to initiate the conference call. In either case, a consultation call is allocated for connecting to the party that is to be added to the call. TAPI can use 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedial">TSPI_lineDial</a> to dial the address of the other party.

The conference call typically transitions into the <i>onHoldPendingConference</i> state, the consultation call <i>dialtone</i> state and the initial call (if one) into the <i>conferenced</i> state.

A conference call can also be set up using a 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linecompletetransfer">TSPI_lineCompleteTransfer</a> function that is resolved into a three-way conference.

TAPI may be able to toggle between the consultation call and the conference call using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineswaphold">TSPI_lineSwapHold</a>.

The 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineunhold">TSPI_lineUnhold</a> function can recover calls that have the call state <i>onHoldPendingConference</i>. If this is done, any consultation call typically goes to the <i>idle</i> state.

A consultation call can be canceled by invoking 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedrop">TSPI_lineDrop</a> on it. When dropping a consultation call, the existing conference call typically transitions back to the <i>connected</i> state. TAPI and its client applications should observe the 
<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a> messages to determine exactly what happens to the calls. For example, if the conference call reverts back to a regular two-party call, the conference call becomes <i>idle</i> and the original participant call may revert to <i>connected</i>.

This function differs from the corresponding TAPI function in that it follows the TSPI model for beginning the lifetime of a call. TAPI and the service provider exchange opaque handles representing the call with one another. In addition, the service provider is permitted to do callbacks for the new call before it returns from this procedure. In any case, the service provider must also treat the handle it returned as "not yet valid" until after the matching 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> message reports success. In other words, it must not issue any 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> messages for the new call or include it in call counts in messages or status data structures for the line.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/Tapi/lineaddrcapflags--constants">LINEADDRCAPFLAGS_ Constants</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineaddtoconference">TSPI_lineAddToConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedial">TSPI_lineDial</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineprepareaddtoconference">TSPI_linePrepareAddToConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineremovefromconference">TSPI_lineRemoveFromConference</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineswaphold">TSPI_lineSwapHold</a>