---
UID: NF:tspi.TSPI_lineSetupTransfer
title: TSPI_lineSetupTransfer function
author: windows-sdk-content
description: The TSPI_lineSetupTransfer function initiates a transfer of the call specified by hdCall. It establishes a consultation call, lphdConsultCall, on which the party can be dialed that can become the destination of the transfer.
old-location: tspi\tspi_linesetuptransfer.htm
tech.root: Tapi
ms.assetid: 0cd95e53-62d5-4318-961a-1136646fd222
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TSPI_lineSetupTransfer, TSPI_lineSetupTransfer function [TAPI 2.2], _tspi_tspi_linesetuptransfer, tspi.tspi_linesetuptransfer, tspi/TSPI_lineSetupTransfer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSetupTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- TSPI_lineSetupTransfer
: 
---

# TSPI_lineSetupTransfer function


## -description


The 
<b>TSPI_lineSetupTransfer</b> function initiates a transfer of the call specified by <i>hdCall</i>. It establishes a consultation call, <i>lphdConsultCall</i>, on which the party can be dialed that can become the destination of the transfer.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The handle to the call to be transferred. The call state of <i>hdCall</i> can be <i>connected</i>.


### -param htConsultCall

The TAPI handle to the new, temporary consultation call. The service provider must save this and use it in all subsequent calls to the 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a> procedure reporting events on the new consultation call.


### -param lphdConsultCall

A pointer to an 
<a href="https://msdn.microsoft.com/8bb1c3fe-a3de-4299-bc15-58321c5da549">HDRVCALL</a> representing the service provider's identifier for the new consultation call. The service provider must fill this location with its handle for the new consultation call before this procedure returns. This handle is ignored by TAPI if the function results in an error. The call state of <i>hdConsultCall</i> is not applicable. 




When setting a call up for transfer, another call (a consultation call) is automatically allocated to enable the application (through TAPI) to dial the address (using 
<a href="https://msdn.microsoft.com/8b24b9a3-af97-45dc-aaaf-d95ce9007ba8">TSPI_lineDial</a>) of the party to where the call is to be transferred. The originating party can carry on a conversation over this consultation call prior to completing the transfer.

This transfer procedure may not be valid for some line devices. Instead of calling this procedure, TAPI may need to unhold an existing held call (using 
<a href="https://msdn.microsoft.com/4719c399-0dce-4aa2-9b6e-a84ad13f9228">TSPI_lineUnhold</a>) to identify the destination of the transfer. On switches that support cross-address call transfer, the consultation call can exist on a different address than the call to be transferred. It may also be necessary to set up the consultation call as an entirely new call using 
<a href="https://msdn.microsoft.com/9c3d6a7d-b0bf-4068-9d64-e0c715a8c011">TSPI_lineMakeCall</a>, to the destination of the transfer.

The <b>transferHeld</b> and <b>transferMake</b> flags in the 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a> data structure report what model the service provider uses.


### -param lpCallParams

A pointer to a 
<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a> structure containing call parameters to use when establishing the consultation call. This parameter can be set to <b>NULL</b> if no special call setup parameters are desired (the service provider uses defaults).


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_INVALBEARERMODE, LINEERR_INVALCALLSTATE, LINEERR_INVALRATE, LINEERR_CALLUNAVAIL, LINEERR_INVALCALLPARAMS, LINEERR_NOMEM, LINEERR_INVALLINESTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALMEDIAMODE, LINEERR_OPERATIONFAILED, LINEERR_INUSE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_BEARERMODEUNAVAIL, LINEERR_RATEUNAVAIL, LINEERR_INVALADDRESSMODE, LINEERR_USERUSERINFOTOOBIG.




## -remarks



The service provider returns LINEERR_INVALCALLSTATE if the call to be transferred is not in a valid state.

This operation sets up the transfer of the call specified by <i>hdCall</i>. The setup phase of a transfer establishes a consultation call to send the address of the destination (the party to be transferred to) to the switch, while the call to be transferred is kept on hold. This new call is referred to as a <i>consultation call</i> (<i>hdConsultCall</i>) and can be manipulated (for example, dropped) independently of the original call.

When the consultation call has reached the <i>dialtone</i> call state, TAPI can continue transferring the call either by dialing the destination address and tracking its progress, or by unholding an existing call. The transfer of the original call to the selected destination is completed using 
<a href="https://msdn.microsoft.com/486a62df-dcdb-46f5-af02-1cf091215401">TSPI_lineCompleteTransfer</a>.

While the consultation call exists, the original call typically transitions to the <i>onholdPendingTransfer</i> state.

The 
<a href="https://msdn.microsoft.com/4719c399-0dce-4aa2-9b6e-a84ad13f9228">TSPI_lineUnhold</a> function can recover calls that have the call state <i>onHoldPendingTransfer</i>. If this is done, any consultation call typically goes to the <i>idle</i> state.

In telephony environments that follow the <b>transferHeld</b> or <b>transferMake</b> transfer models, this procedure returns LINEERR_OPERATIONFAILED and does not allocate a consultation call handle.

A consultation call can be canceled by invoking 
<a href="https://msdn.microsoft.com/ac7ec102-d7ad-4e63-833e-3c798487d7b4">TSPI_lineDrop</a> on it. After dropping a consultation call, the original call typically transitions back to the <i>connected</i> state.

This function differs from the corresponding TAPI function in that it follows the TSPI model for beginning the lifetime of a call. TAPI and the service provider exchange opaque handles representing the call with one another. In addition, the service provider is permitted to do callbacks for the new call before it returns from this procedure. In any case, the service provider must also treat the handle it returned as "not yet valid" until after the matching 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> message reports success. In other words, it must not issue any 
<a href="https://msdn.microsoft.com/11ae7e78-8a10-4757-886b-c0aa47c4d55b">LINEEVENT</a> messages for the new call or include it in call counts in messages or status data structures for the line.




## -see-also




<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>



<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/825f132c-fb0e-4e3d-bd2c-4e5226a30ba3">TSPI_lineBlindTransfer</a>



<a href="https://msdn.microsoft.com/486a62df-dcdb-46f5-af02-1cf091215401">TSPI_lineCompleteTransfer</a>



<a href="https://msdn.microsoft.com/8b24b9a3-af97-45dc-aaaf-d95ce9007ba8">TSPI_lineDial</a>



<a href="https://msdn.microsoft.com/ac7ec102-d7ad-4e63-833e-3c798487d7b4">TSPI_lineDrop</a>



<a href="https://msdn.microsoft.com/9ecd6a63-e906-483b-b404-28797d259149">TSPI_lineSwapHold</a>



<a href="https://msdn.microsoft.com/4719c399-0dce-4aa2-9b6e-a84ad13f9228">TSPI_lineUnhold</a>
 

 

