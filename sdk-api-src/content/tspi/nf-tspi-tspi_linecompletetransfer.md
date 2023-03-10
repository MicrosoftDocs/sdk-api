---
UID: NF:tspi.TSPI_lineCompleteTransfer
title: TSPI_lineCompleteTransfer function (tspi.h)
description: The TSPI_lineCompleteTransfer function completes the transfer of the specified call to the party connected in the consultation call.
helpviewer_keywords: ["TSPI_lineCompleteTransfer","TSPI_lineCompleteTransfer function [TAPI 2.2]","_tspi_tspi_linecompletetransfer","tspi.tspi_linecompletetransfer","tspi/TSPI_lineCompleteTransfer"]
old-location: tspi\tspi_linecompletetransfer.htm
tech.root: tapi3
ms.assetid: 486a62df-dcdb-46f5-af02-1cf091215401
ms.date: 12/05/2018
ms.keywords: TSPI_lineCompleteTransfer, TSPI_lineCompleteTransfer function [TAPI 2.2], _tspi_tspi_linecompletetransfer, tspi.tspi_linecompletetransfer, tspi/TSPI_lineCompleteTransfer
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
 - TSPI_lineCompleteTransfer
 - tspi/TSPI_lineCompleteTransfer
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
 - TSPI_lineCompleteTransfer
---

# TSPI_lineCompleteTransfer function


## -description

The 
<b>TSPI_lineCompleteTransfer</b> function completes the transfer of the specified call to the party connected in the consultation call. If <i>dwTransferMode</i> is LINETRANSFERMODE_CONFERENCE, the original call handle is changed to a conference call. Otherwise, the service provider should send call state messages changing the calls to <i>idle</i>.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdCall

The service provider's handle to the call to be transferred. The call state of <i>hdCall</i> can be <i>onHoldPendingTransfer</i>.

### -param hdConsultCall

A handle to the call that represents a connection to the destination of the transfer. The call state of <i>hdConsultCall</i> can be <i>connected</i>, <i>ringback</i>, <i>busy</i>, or <i>proceeding</i>.

### -param htConfCall

This parameter is only valid if <i>dwTransferMode</i> is specified as LINETRANSFERMODE_CONFERENCE. The service provider must save this parameter value and use it in all subsequent calls to the 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> procedure reporting events on the call. Otherwise this parameter is ignored.

### -param lphdConfCall

A pointer to an 
<a href="/windows/desktop/Tapi/hdrvline">HDRVCALL</a> representing the service provider's identifier for the call. This parameter is only valid if <i>dwTransferMode</i> is specified as LINETRANSFERMODE_CONFERENCE. The service provider must fill this location with its handle for the new conference call before returning from this function.

### -param dwTransferMode

Specifies how the initiated transfer request is to be resolved. This parameter uses one of the 
<a href="/windows/desktop/Tapi/linetransfermode--constants">LINETRANSFERMODE_ constants</a>.

## -returns

Returns <i>dwRequestID</i> or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

This function completes the transfer of the original call, <i>hdCall</i>, to the party currently connected through <i>hdConsultCall</i>. The consultation call is typically dialed on the consultation call allocated as part of 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetuptransfer">TSPI_lineSetupTransfer</a>, but it can be any call to which the switch is capable of transferring <i>hdCall</i>.

The transfer request can be resolved either as a transfer or as a three-way conference call. When resolved as a transfer, the parties connected through <i>hdCall</i> and <i>hdConsultCall</i> are connected to each other, and both <i>hdCall</i> and <i>hdConsultCall</i> transition to the idle state.

When resolved as a conference, all three parties enter into a conference call. Both existing call handles remain valid, but transition to the <i>conferenced</i> state. A conference call handle is created and returned, and it transitions to the <i>connected</i> state.

It may also be possible to perform a blind transfer of a call using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineblindtransfer">TSPI_lineBlindTransfer</a>.

This function differs from the corresponding TAPI function in that it follows the TSPI model for beginning the lifetime of a call. TAPI and the service provider exchange opaque handles representing the call with one another. In addition, the service provider is permitted to do callbacks for the new call before it returns from this procedure. In any case, the service provider must also treat the handle it returned as "not yet valid" until after the matching 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> message reports success. In other words, it must not issue any 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> message for the new call or include it in call counts in messages or status data structures for the line.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a>



<a href="/windows/desktop/Tapi/linetransfermode--constants">LINETRANSFERMODE_ Constants</a>



<a href="/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)">LINE_CALLSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineblindtransfer">TSPI_lineBlindTransfer</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclosecall">TSPI_lineCloseCall</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetuptransfer">TSPI_lineSetupTransfer</a>