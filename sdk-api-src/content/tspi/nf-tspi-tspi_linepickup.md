---
UID: NF:tspi.TSPI_linePickup
title: TSPI_linePickup function (tspi.h)
description: The TSPI_linePickup function picks up a call alerting at the specified destination address and returns a call handle for the picked-up call.
helpviewer_keywords: ["TSPI_linePickup","TSPI_linePickup function [TAPI 2.2]","_tspi_tspi_linepickup","tspi.tspi_linepickup","tspi/TSPI_linePickup"]
old-location: tspi\tspi_linepickup.htm
tech.root: tapi3
ms.assetid: 97ab8896-3794-4de2-a1af-41025d2b6b17
ms.date: 12/05/2018
ms.keywords: TSPI_linePickup, TSPI_linePickup function [TAPI 2.2], _tspi_tspi_linepickup, tspi.tspi_linepickup, tspi/TSPI_linePickup
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
 - TSPI_linePickup
 - tspi/TSPI_linePickup
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
 - TSPI_linePickup
---

# TSPI_linePickup function


## -description

The 
<b>TSPI_linePickup</b> function picks up a call alerting at the specified destination address and returns a call handle for the picked-up call. If invoked with <b>NULL</b> for the <i>lpszDestAddress</i> parameter, a group pickup is performed. If required by the device capabilities, <i>lpszGroupID</i> specifies the group identifier to which the alerting station belongs.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdLine

The handle to the line on which a call is to be picked up.

### -param dwAddressID

The address on <i>hdLine</i> at which the pickup is to be originated. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param htCall

The TAPI handle to the new call. The service provider must save this and use it in all subsequent calls to the 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> procedure reporting events on the call.

### -param lphdCall

A pointer to an 
<a href="/windows/desktop/Tapi/hdrvline">HDRVCALL</a> representing the service provider's identifier for the call. The service provider must fill this location with its handle for the call before this procedure returns. This handle is ignored by TAPI if the function results in an error.

### -param lpszDestAddress

A pointer to a <b>null</b>-terminated Unicode string that contains the address whose call is to be picked up. The address is standard link format.

### -param lpszGroupID

A pointer to a <b>null</b>-terminated Unicode string containing the group identifier to which the alerting station belongs. This parameter is required on some switches to pick up calls outside of the current pickup group. 




<div class="alert"><b>Note</b>  <i>lpszGroupID</i> can be specified by itself with a <b>NULL</b> pointer for <i>lpszDestAddress</i>. Alternatively, <i>lpszGroupID</i> can be specified in addition to <i>lpszDestAddress</i>, if required by the device. It can also be <b>NULL</b> itself.</div>
<div> </div>

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_NOMEM, LINEERR_INVALADDRESSID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESS, LINEERR_OPERATIONFAILED, LINEERR_INVALGROUPID, LINEERR_RESOURCEUNAVAIL.

## -remarks

When a call has been picked up successfully, the service provider notifies TAPI with the 
<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a> message about call state changes. The 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure supplies information about the call that was picked up. It lists the reason for the call as <i>pickup</i>. This structure is available by calling 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>.

The service provider sets LINEADDRCAPFLAGS_PICKUPCALLWAIT to <b>TRUE</b> in the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> structure if 
<b>TSPI_linePickup</b> can be used to pick up a call for which the user has audibly detected the call-waiting signal, but for which the provider is unable to perform the detection. This gives the user a mechanism to answer a waiting call even though the service provider was unable to detect the call-waiting signal. When 
<b>TSPI_linePickup</b> is being used to pick up a call-waiting call, both <i>lpszDestAddress</i> and <i>lpszGroupID</i> pointer parameters are <b>NULL</b>. The service provider creates a new call handle for the waiting call and passes that handle to the user in <i>lphdCall</i>. The <i>dwAddressID</i> parameter is most often zero (particularly in single-line residential cases).

Once 
<b>TSPI_linePickup</b> is used to pick up the second call, 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineswaphold">TSPI_lineSwapHold</a> can be used to toggle between them. 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedrop">TSPI_lineDrop</a> can be used to drop one (and toggle to the other), and so forth. If the user wants to drop the current call and pick up the second call, they call 
<b>TSPI_lineDrop</b> when they get the call-waiting beep, wait for the second call to ring, and then call 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineanswer">TSPI_lineAnswer</a> on the new call handle. The service provider sets the LINEADDRFEATURE_PICKUP flag in the <b>dwAddressFeatures</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a> to indicate when pickup is actually possible.

This function differs from the corresponding TAPI function in that it follows the TSPI model for beginning the lifetime of a call. TAPI and the service provider exchange opaque handles representing the call with one another. In addition, the service provider is permitted to do callbacks for the new call before it returns from this procedure. In any case, the service provider must also treat the handle it returned as "not yet valid" until after the matching 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> message reports success. In other words, it must not issue any 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> messages for the new call or include it in call counts in messages or status data structures for the line.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a>



<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineanswer">TSPI_lineAnswer</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linedrop">TSPI_lineDrop</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallstatus">TSPI_lineGetCallStatus</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineswaphold">TSPI_lineSwapHold</a>