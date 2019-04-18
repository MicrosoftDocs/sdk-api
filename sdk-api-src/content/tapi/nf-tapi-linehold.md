---
UID: NF:tapi.lineHold
title: lineHold function (tapi.h)
author: windows-sdk-content
description: The lineHold function places the specified call on hold.
old-location: tapi2\linehold.htm
tech.root: Tapi
ms.assetid: d2fd450c-402c-4122-a785-a6b5216acfe9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_linehold, lineHold, lineHold function [TAPI 2.2], tapi/lineHold, tapi2.linehold"
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
 - lineHold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# lineHold function


## -description


The 
<b>lineHold</b> function places the specified call on hold.


## -parameters




### -param hCall

Handle to the call to be placed on hold. The application must be an owner of the call. The call state of <i>hCall</i> must be <i>connected</i>.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.




## -remarks



The call on hold is temporarily disconnected allowing the application to use the line device for making or answering other calls. The 
<b>lineHold</b> function performs a so-called "hard hold" of the specified call (as opposed to a "consultation call"). A call on hard hold typically cannot be transferred or included in a conference call, but a consultation call can. Consultation calls are initiated using 
<a href="https://msdn.microsoft.com/40f0ce8f-9809-43ec-af48-d8e410553048">lineSetupTransfer</a>, 
<a href="https://msdn.microsoft.com/13bf81c6-f7f6-4fd4-b546-15e58f7bc618">lineSetupConference</a>, or 
<a href="https://msdn.microsoft.com/e1603b36-8bcb-4665-b711-6d2b6794c963">linePrepareAddToConference</a>.

After a call has been successfully placed on hold, the call state typically transitions to <i>onHold</i>. A held call is retrieved by 
<a href="https://msdn.microsoft.com/c32d8d3a-f54c-411a-ae86-4aecd6dce456">lineUnhold</a>. While a call is on hold, the application can receive 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> messages about state changes of the held call. For example, if the held party hangs up, the call state can transition to <i>disconnected</i>.

In a bridged situation, a 
<b>lineHold</b> operation may possibly not actually place the call on hold, because the status of other stations on the call can govern (for example, attempting to "hold" a call when other stations are participating is not be possible); instead, the call can simply be changed to the LINECONNECTEDMODE_INACTIVE mode if it remains <i>connected</i> at other stations.




## -see-also




<a href="https://msdn.microsoft.com/65e22e4e-e346-41c2-929a-ba0d1f7f1732">Hold Overview</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/e1603b36-8bcb-4665-b711-6d2b6794c963">linePrepareAddToConference</a>



<a href="https://msdn.microsoft.com/13bf81c6-f7f6-4fd4-b546-15e58f7bc618">lineSetupConference</a>



<a href="https://msdn.microsoft.com/40f0ce8f-9809-43ec-af48-d8e410553048">lineSetupTransfer</a>



<a href="https://msdn.microsoft.com/c32d8d3a-f54c-411a-ae86-4aecd6dce456">lineUnhold</a>
 

 

