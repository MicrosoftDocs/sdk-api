---
UID: NF:tapi.lineSetupTransferA
title: lineSetupTransferA function (tapi.h)
author: windows-sdk-content
description: The lineSetupTransfer function initiates a transfer of the call specified by the hCall parameter.
old-location: tapi2\linesetuptransfer.htm
tech.root: Tapi
ms.assetid: 40f0ce8f-9809-43ec-af48-d8e410553048
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_linesetuptransfer, lineSetupTransfer, lineSetupTransfer function [TAPI 2.2], lineSetupTransferA, lineSetupTransferW, tapi/lineSetupTransfer, tapi/lineSetupTransferA, tapi/lineSetupTransferW, tapi2.linesetuptransfer"
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/111e6c11-67a7-4aab-81dd-f1b4316887e7">lineDial</a> to dial the address associated with the new transfer destination of the call. The originating party can carry on a conversation over this consultation call prior to completing the transfer. The call state of <i>hConsultCall</i> is not applicable. 




This transfer procedure may not be valid for some line devices. The application may need to ignore the new consultation call and unhold an existing held call (using 
<a href="https://msdn.microsoft.com/c32d8d3a-f54c-411a-ae86-4aecd6dce456">lineUnhold</a>) to identify the destination of the transfer. On switches that support cross-address call transfer, the consultation call can exist on a different address than the call to be transferred. It may also be necessary that the consultation call be set up as an entirely new call, by 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>, to the destination of the transfer. Which forms of transfer are available are specified in the call's address capabilities.


### -param lpCallParams

Pointer to a 
<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a> structure containing the call parameters to use when establishing the consultation call. This parameter can be set to <b>NULL</b> if no special call setup parameters are desired.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_BEARERMODEUNAVAIL, LINEERR_INVALRATE, LINEERR_CALLUNAVAIL, LINEERR_NOMEM, LINEERR_INUSE, LINEERR_NOTOWNER, LINEERR_INVALADDRESSMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALBEARERMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_RATEUNAVAIL, LINEERR_INVALCALLPARAMS, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALLINESTATE, LINEERR_UNINITIALIZED, LINEERR_INVALMEDIAMODE, LINEERR_USERUSERINFOTOOBIG, LINEERR_INVALPOINTER.




## -remarks



The 
<b>lineSetupTransfer</b> function sets up the transfer of the call specified by <i>hCall</i>. The setup phase of a transfer establishes a consultation call that enables the application to send the address of the destination (the party to be transferred to) to the switch, while the call to be transferred is kept on hold. This new call is referred to as a consultation call (<i>hConsultCall</i>) and can be dropped or otherwise manipulated independently of the original call.

When the consultation call has reached the <i>dialtone</i> call state, the application can proceed transferring the call either by dialing the destination address and tracking its progress, or by unholding an existing call. The transfer of the original call to the selected destination is completed using 
<a href="https://msdn.microsoft.com/ebedf664-4c45-49c3-9d86-c3d782077a00">lineCompleteTransfer</a>.

While the consultation call exists, the original call typically transitions to the <i>onholdPendingTransfer</i> state. The application may be able to toggle between the consultation call and the original call by using 
<a href="https://msdn.microsoft.com/9e575c82-301c-4505-b400-faf4dc291ff8">lineSwapHold</a>. A consultation call can be canceled by invoking 
<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a> on it. After dropping a consultation call, the original call typically transitions back to the <i>connected</i> state. If the call state of the original call is <i>onholdPendingTransfer</i>, the 
<a href="https://msdn.microsoft.com/c32d8d3a-f54c-411a-ae86-4aecd6dce456">lineUnhold</a> function can be used to recover the call. In this case, the call state of the consultation call is set to <i>idle</i>.

The application can also transfer calls in a single step, without having to deal with the intervening consultation call, by using 
<a href="https://msdn.microsoft.com/c1997933-475e-4bcd-be44-ad92a2a678eb">lineBlindTransfer</a>.




## -see-also




<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/b1027f09-74e1-4da8-b718-bb55a56dda1d">Transfer Overview</a>



<a href="https://msdn.microsoft.com/c1997933-475e-4bcd-be44-ad92a2a678eb">lineBlindTransfer</a>



<a href="https://msdn.microsoft.com/ebedf664-4c45-49c3-9d86-c3d782077a00">lineCompleteTransfer</a>



<a href="https://msdn.microsoft.com/111e6c11-67a7-4aab-81dd-f1b4316887e7">lineDial</a>



<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>



<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>



<a href="https://msdn.microsoft.com/9e575c82-301c-4505-b400-faf4dc291ff8">lineSwapHold</a>



<a href="https://msdn.microsoft.com/c32d8d3a-f54c-411a-ae86-4aecd6dce456">lineUnhold</a>
 

 

