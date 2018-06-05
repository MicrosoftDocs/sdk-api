---
UID: NF:tapi.lineCompleteTransfer
title: lineCompleteTransfer function
author: windows-sdk-content
description: The lineCompleteTransfer function completes the transfer of the specified call to the party connected in the consultation call.
old-location: tapi2\linecompletetransfer.htm
old-project: Tapi
ms.assetid: ebedf664-4c45-49c3-9d86-c3d782077a00
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_linecompletetransfer, lineCompleteTransfer, lineCompleteTransfer function [TAPI 2.2], tapi/lineCompleteTransfer, tapi2.linecompletetransfer"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineCompleteTransfer
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="https://msdn.microsoft.com/0a01131f-b63c-45ef-a0a9-17d69a0dacf9">LINETRANSFERMODE_ Constants</a>.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_NOTOWNER, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCONSULTCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALTRANSFERMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.




## -remarks



The LINE_REPLY message sent in response to a call to the 
<b>lineCompleteTransfer</b> function is based on the status of the call specified by the <i>hCall</i> parameter.

This operation completes the transfer of the original call, <i>hCall</i>, to the party currently connected by <i>hConsultCall</i>. The consultation call is typically dialed on the consultation call allocated as part of 
<a href="https://msdn.microsoft.com/40f0ce8f-9809-43ec-af48-d8e410553048">lineSetupTransfer</a>, but it can be any call to which the switch is capable of transferring <i>hCall</i>.

The transfer request can be resolved either as a transfer or as a three-way conference call. When resolved as a transfer, the parties connected by <i>hCall</i> and <i>hConsultCall</i> are connected to each other, and both <i>hCall</i> and <i>hConsultCall</i> are typically cleared from the application's line and transition to the <i>idle</i> state. The application's call handle remains valid after the transfer has completed. The application must deallocate its handle with 
<a href="https://msdn.microsoft.com/a695ee19-e371-4126-b438-62bf52179cba">lineDeallocateCall</a> when it is no longer interested in the transferred call.

When resolved as a conference, all three parties enter into a conference call. Both existing call handles remain valid but transition to the <i>conferenced</i> state. A conference call handle is created and returned, and it transitions to the <i>connected</i> state.

If 
<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a> is called immediately after 
<b>lineCompleteTransfer</b> with the result that the calls are conferenced, 
<b>lineGetConfRelatedCalls</b> may not return a complete list of related calls. This is because TAPI waits to receive a 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> message indicating that the call has entered LINECALLSTATE_CONFERENCED before it considers the call to actually be part of the conference. That is, it waits for the service provider to confirm the conferenced state. After the application has received the LINE_CALLSTATE message, 
<b>lineGetConfRelatedCalls</b> returns complete information.

It can also be possible to perform a blind transfer of a call using 
<a href="https://msdn.microsoft.com/c1997933-475e-4bcd-be44-ad92a2a678eb">lineBlindTransfer</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/b1027f09-74e1-4da8-b718-bb55a56dda1d">Transfer overview</a>



<a href="https://msdn.microsoft.com/c1997933-475e-4bcd-be44-ad92a2a678eb">lineBlindTransfer</a>



<a href="https://msdn.microsoft.com/a695ee19-e371-4126-b438-62bf52179cba">lineDeallocateCall</a>



<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a>



<a href="https://msdn.microsoft.com/40f0ce8f-9809-43ec-af48-d8e410553048">lineSetupTransfer</a>
 

 

