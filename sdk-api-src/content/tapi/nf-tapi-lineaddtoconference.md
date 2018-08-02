---
UID: NF:tapi.lineAddToConference
title: lineAddToConference function
author: windows-sdk-content
description: The lineAddToConference function adds the call specified by hConsultCall to the conference call specified by hConfCall.
old-location: tapi2\lineaddtoconference.htm
old-project: Tapi
ms.assetid: fbbaea96-727c-46b9-91d1-31d3f89d8ad8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "_tapi2_lineaddtoconference, lineAddToConference, lineAddToConference function [TAPI 2.2], tapi/lineAddToConference, tapi2.lineaddtoconference"
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineAddToConference
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineAddToConference function


## -description


The 
<b>lineAddToConference</b> function adds the call specified by <i>hConsultCall</i> to the conference call specified by <i>hConfCall</i>.


## -parameters




### -param hConfCall

Handle to the conference call. The application must be an owner of this call. Any monitoring (media, tones, digits) on a conference call applies only to the <i>hConfCall</i>, not to the individual participating calls. Call state of <i>hConfCall</i> must be <i>onHoldPendingConference</i> or <i>onHold</i>.


### -param hConsultCall

Handle to the call to be added to the conference call. The application must be an owner of this call. This call cannot be a parent of another conference or a participant in any conference. Depending on the device capabilities indicated in 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>, the <i>hConsultCall</i> may not necessarily have been established using 
<a href="https://msdn.microsoft.com/13bf81c6-f7f6-4fd4-b546-15e58f7bc618">lineSetupConference</a> or 
<a href="https://msdn.microsoft.com/e1603b36-8bcb-4665-b711-6d2b6794c963">linePrepareAddToConference</a>. The call state of <i>hConsultCall</i> must be <i>connected</i>, <i>onHold</i>, <i>proceeding</i>, or <i>ringback</i>. Many PBXs allow calls to be added to conferences before they are actually answered.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds, or it is a negative error number if an error occurs. Possible return values are:

LINEERR_CONFERENCEFULL, LINEERR_NOTOWNER, LINEERR_INVALCONFCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.




## -remarks



If LINEERR_INVALCALLHANDLE is returned, the specified call handle for the added call is invalid; <i>hConsultCall</i> is a parent of another conference or already a participant in a conference; <i>hConsultCall</i> cannot be added for other reasons (such as, it must have been established using 
<a href="https://msdn.microsoft.com/13bf81c6-f7f6-4fd4-b546-15e58f7bc618">lineSetupConference</a> or 
<a href="https://msdn.microsoft.com/e1603b36-8bcb-4665-b711-6d2b6794c963">linePrepareAddToConference</a>); or <i>hConsultCall</i> and <i>hConfCall</i> are calls on different open lines.

The call handle of the added party remains valid after adding the call to a conference. Its state typically changes to <i>conferenced</i> while the state of the conference call typically becomes <i>connected</i>. Using 
<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a>, you can obtain a list of call handles that are part of the same conference call as the specified call. The specified call is either a conference call or a participant call in a conference call. New handles are generated for those calls for which the application does not already have handles, and the application is granted monitor privilege to those calls. The handle to an individual participating call can be used later to remove that party from the conference call using 
<a href="https://msdn.microsoft.com/03363579-66c2-4bb5-b110-01084c20bf09">lineRemoveFromConference</a>.

If 
<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a> is called immediately after 
<b>lineAddToConference</b>, it may not return a complete list of related calls because TAPI waits to receive a 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> message indicating that the call has entered LINECALLSTATE_CONFERENCED before it considers the call to actually be part of the conference (that is, the conferenced state is confirmed by the service provider). After the application has received the LINE_CALLSTATE message, 
<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a> returns complete information.

<div class="alert"><b>Note</b>  All calls that are part of a conference must exist on the same open line.</div>
<div> </div>
The call states of the calls participating in a conference are not independent. For example, when dropping a conference call, all participating calls can automatically become idle. An application should consult the line's device capabilities to determine what form of conference removal is available. The application should track the LINE_CALLSTATE messages to determine what happened to the calls involved.

The conference call is established either by 
<a href="https://msdn.microsoft.com/13bf81c6-f7f6-4fd4-b546-15e58f7bc618">lineSetupConference</a> or 
<a href="https://msdn.microsoft.com/ebedf664-4c45-49c3-9d86-c3d782077a00">lineCompleteTransfer</a>. The call added to a conference is typically established using 
<a href="https://msdn.microsoft.com/13bf81c6-f7f6-4fd4-b546-15e58f7bc618">lineSetupConference</a> or 
<a href="https://msdn.microsoft.com/e1603b36-8bcb-4665-b711-6d2b6794c963">linePrepareAddToConference</a>. Some switches can allow adding arbitrary calls to the conference, and such a call can have been set up using 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> and be on (hard) hold. The application can examine the <b>dwAddrCapFlags</b> member of the 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a> structure to determine the permitted operations.




## -see-also




<a href="https://msdn.microsoft.com/f685097b-1b54-412b-999f-d9bdb3120ab9">Conference overview</a>



<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/ebedf664-4c45-49c3-9d86-c3d782077a00">lineCompleteTransfer</a>



<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a>



<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>



<a href="https://msdn.microsoft.com/e1603b36-8bcb-4665-b711-6d2b6794c963">linePrepareAddToConference</a>



<a href="https://msdn.microsoft.com/03363579-66c2-4bb5-b110-01084c20bf09">lineRemoveFromConference</a>



<a href="https://msdn.microsoft.com/13bf81c6-f7f6-4fd4-b546-15e58f7bc618">lineSetupConference</a>
 

 

