---
UID: NF:tapi.lineSetupTransferA
title: lineSetupTransferA function (tapi.h)
description: The lineSetupTransfer function initiates a transfer of the call specified by the hCall parameter. (lineSetupTransferA)
helpviewer_keywords: ["lineSetupTransferA", "tapi/lineSetupTransferA"]
old-location: tapi2\linesetuptransfer.htm
tech.root: tapi3
ms.assetid: 40f0ce8f-9809-43ec-af48-d8e410553048
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetuptransfer, lineSetupTransfer, lineSetupTransfer function [TAPI 2.2], lineSetupTransferA, lineSetupTransferW, tapi/lineSetupTransfer, tapi/lineSetupTransferA, tapi/lineSetupTransferW, tapi2.linesetuptransfer
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineSetupTransferW (Unicode) and lineSetupTransferA (ANSI)
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
 - lineSetupTransferA
 - tapi/lineSetupTransferA
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
 - lineSetupTransfer
 - lineSetupTransferA
 - lineSetupTransferW
---

# lineSetupTransferA function


## -description

The 
<b>lineSetupTransfer</b> function initiates a transfer of the call specified by the <i>hCall</i> parameter. It establishes a consultation call, <i>lphConsultCall</i>, on which the party can be dialed that can become the destination of the transfer. The application acquires owner privilege to the <i>lphConsultCall</i> parameter.

## -parameters

### -param hCall

Handle to the call to be transferred. The application must be an owner of the call. The call state of <i>hCall</i> must be <i>connected</i>.

### -param lphConsultCall

Pointer to an <i>hCall</i> handle. This location is then loaded with a handle identifying the temporary consultation call. When setting up a call for transfer, a consultation call is automatically allocated that enables 
<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a> to dial the address associated with the new transfer destination of the call. The originating party can carry on a conversation over this consultation call prior to completing the transfer. The call state of <i>hConsultCall</i> is not applicable. 




This transfer procedure may not be valid for some line devices. The application may need to ignore the new consultation call and unhold an existing held call (using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineunhold">lineUnhold</a>) to identify the destination of the transfer. On switches that support cross-address call transfer, the consultation call can exist on a different address than the call to be transferred. It may also be necessary that the consultation call be set up as an entirely new call, by 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>, to the destination of the transfer. Which forms of transfer are available are specified in the call's address capabilities.

### -param lpCallParams

Pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> structure containing the call parameters to use when establishing the consultation call. This parameter can be set to <b>NULL</b> if no special call setup parameters are desired.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_BEARERMODEUNAVAIL, LINEERR_INVALRATE, LINEERR_CALLUNAVAIL, LINEERR_NOMEM, LINEERR_INUSE, LINEERR_NOTOWNER, LINEERR_INVALADDRESSMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALBEARERMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_RATEUNAVAIL, LINEERR_INVALCALLPARAMS, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALLINESTATE, LINEERR_UNINITIALIZED, LINEERR_INVALMEDIAMODE, LINEERR_USERUSERINFOTOOBIG, LINEERR_INVALPOINTER.

## -remarks

The 
<b>lineSetupTransfer</b> function sets up the transfer of the call specified by <i>hCall</i>. The setup phase of a transfer establishes a consultation call that enables the application to send the address of the destination (the party to be transferred to) to the switch, while the call to be transferred is kept on hold. This new call is referred to as a consultation call (<i>hConsultCall</i>) and can be dropped or otherwise manipulated independently of the original call.

When the consultation call has reached the <i>dialtone</i> call state, the application can proceed transferring the call either by dialing the destination address and tracking its progress, or by unholding an existing call. The transfer of the original call to the selected destination is completed using 
<a href="/windows/desktop/api/tapi/nf-tapi-linecompletetransfer">lineCompleteTransfer</a>.

While the consultation call exists, the original call typically transitions to the <i>onholdPendingTransfer</i> state. The application may be able to toggle between the consultation call and the original call by using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineswaphold">lineSwapHold</a>. A consultation call can be canceled by invoking 
<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a> on it. After dropping a consultation call, the original call typically transitions back to the <i>connected</i> state. If the call state of the original call is <i>onholdPendingTransfer</i>, the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineunhold">lineUnhold</a> function can be used to recover the call. In this case, the call state of the consultation call is set to <i>idle</i>.

The application can also transfer calls in a single step, without having to deal with the intervening consultation call, by using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineblindtransfer">lineBlindTransfer</a>.





> [!NOTE]
> The tapi.h header defines lineSetupTransfer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/Tapi/transfer-ovr">Transfer Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineblindtransfer">lineBlindTransfer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linecompletetransfer">lineCompleteTransfer</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedrop">lineDrop</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineswaphold">lineSwapHold</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineunhold">lineUnhold</a>
