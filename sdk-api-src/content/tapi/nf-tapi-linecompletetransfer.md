---
UID: NF:tapi.lineCompleteTransfer
title: lineCompleteTransfer function (tapi.h)
description: The lineCompleteTransfer function completes the transfer of the specified call to the party connected in the consultation call.
helpviewer_keywords: ["_tapi2_linecompletetransfer","lineCompleteTransfer","lineCompleteTransfer function [TAPI 2.2]","tapi/lineCompleteTransfer","tapi2.linecompletetransfer"]
old-location: tapi2\linecompletetransfer.htm
tech.root: tapi3
ms.assetid: ebedf664-4c45-49c3-9d86-c3d782077a00
ms.date: 12/05/2018
ms.keywords: _tapi2_linecompletetransfer, lineCompleteTransfer, lineCompleteTransfer function [TAPI 2.2], tapi/lineCompleteTransfer, tapi2.linecompletetransfer
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
 - lineCompleteTransfer
 - tapi/lineCompleteTransfer
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
 - lineCompleteTransfer
---

# lineCompleteTransfer function


## -description

The 
<b>lineCompleteTransfer</b> function completes the transfer of the specified call to the party connected in the consultation call.

## -parameters

### -param hCall

Handle to the call to be transferred. The application must be an owner of this call. The call state of <i>hCall</i> must be <i>onHold</i> or <i>onHoldPendingTransfer</i>.

### -param hConsultCall

Handle to the call that represents a connection with the destination of the transfer. The application must be an owner of this call. The call state of <i>hConsultCall</i> must be <i>connected</i>, <i>ringback</i>, <i>busy</i>, or <i>proceeding</i>.

### -param lphConfCall

Pointer to a memory location where an <i>hCall</i> handle can be returned. If <i>dwTransferMode</i> is LINETRANSFERMODE_CONFERENCE, the newly created conference call is returned in <i>lphConfCall</i> and the application becomes the sole owner of the conference call. Otherwise, this parameter is ignored by TAPI.

### -param dwTransferMode

How the initiated transfer request is to be resolved. This parameter uses one of the 
<a href="/windows/desktop/Tapi/linetransfermode--constants">LINETRANSFERMODE_ Constants</a>.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_NOTOWNER, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCONSULTCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALTRANSFERMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.

## -remarks

The LINE_REPLY message sent in response to a call to the 
<b>lineCompleteTransfer</b> function is based on the status of the call specified by the <i>hCall</i> parameter.

This operation completes the transfer of the original call, <i>hCall</i>, to the party currently connected by <i>hConsultCall</i>. The consultation call is typically dialed on the consultation call allocated as part of 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetuptransfer">lineSetupTransfer</a>, but it can be any call to which the switch is capable of transferring <i>hCall</i>.

The transfer request can be resolved either as a transfer or as a three-way conference call. When resolved as a transfer, the parties connected by <i>hCall</i> and <i>hConsultCall</i> are connected to each other, and both <i>hCall</i> and <i>hConsultCall</i> are typically cleared from the application's line and transition to the <i>idle</i> state. The application's call handle remains valid after the transfer has completed. The application must deallocate its handle with 
<a href="/windows/desktop/api/tapi/nf-tapi-linedeallocatecall">lineDeallocateCall</a> when it is no longer interested in the transferred call.

When resolved as a conference, all three parties enter into a conference call. Both existing call handles remain valid but transition to the <i>conferenced</i> state. A conference call handle is created and returned, and it transitions to the <i>connected</i> state.

If 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetconfrelatedcalls">lineGetConfRelatedCalls</a> is called immediately after 
<b>lineCompleteTransfer</b> with the result that the calls are conferenced, 
<b>lineGetConfRelatedCalls</b> may not return a complete list of related calls. This is because TAPI waits to receive a 
<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a> message indicating that the call has entered LINECALLSTATE_CONFERENCED before it considers the call to actually be part of the conference. That is, it waits for the service provider to confirm the conferenced state. After the application has received the LINE_CALLSTATE message, 
<b>lineGetConfRelatedCalls</b> returns complete information.

It can also be possible to perform a blind transfer of a call using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineblindtransfer">lineBlindTransfer</a>.

## -see-also

<a href="/windows/desktop/Tapi/line-callstate">LINE_CALLSTATE</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/Tapi/transfer-ovr">Transfer overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineblindtransfer">lineBlindTransfer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedeallocatecall">lineDeallocateCall</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetconfrelatedcalls">lineGetConfRelatedCalls</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetuptransfer">lineSetupTransfer</a>