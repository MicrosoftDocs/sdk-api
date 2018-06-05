---
UID: NF:tapi.linePrepareAddToConferenceA
title: linePrepareAddToConferenceA function
author: windows-sdk-content
description: The linePrepareAddToConference function prepares an existing conference call for the addition of another party.
old-location: tapi2\lineprepareaddtoconference.htm
old-project: Tapi
ms.assetid: e1603b36-8bcb-4665-b711-6d2b6794c963
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_lineprepareaddtoconference, linePrepareAddToConference, linePrepareAddToConference function [TAPI 2.2], linePrepareAddToConferenceA, linePrepareAddToConferenceW, tapi/linePrepareAddToConference, tapi/linePrepareAddToConferenceA, tapi/linePrepareAddToConferenceW, tapi2.lineprepareaddtoconference"
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
req.unicode-ansi: linePrepareAddToConferenceW (Unicode) and linePrepareAddToConferenceA (ANSI)
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
-	linePrepareAddToConference
-	linePrepareAddToConferenceA
-	linePrepareAddToConferenceW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# linePrepareAddToConferenceA function


## -description


The 
<b>linePrepareAddToConference</b> function prepares an existing conference call for the addition of another party.


## -parameters




### -param hConfCall

Handle to a conference call. The application must be an owner of this call. The call state of <i>hConfCall</i> must be <i>connected</i>.


### -param lphConsultCall

Pointer to an HCALL handle. This location is then loaded with a handle identifying the consultation call to be added. Initially, the application is the sole owner of this call.


### -param lpCallParams

Pointer to a 
<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a> structure containing call parameters to use when establishing the consultation call. This parameter can be set to <b>NULL</b> if no special call setup parameters are desired.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_BEARERMODEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_CALLUNAVAIL, LINEERR_INVALRATE, LINEERR_CONFERENCEFULL, LINEERR_NOMEM, LINEERR_INUSE, LINEERR_NOTOWNER, LINEERR_INVALADDRESSMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALBEARERMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLPARAMS, LINEERR_RATEUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCONFCALLHANDLE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALLINESTATE, LINEERR_USERUSERINFOTOOBIG, LINEERR_INVALMEDIAMODE, LINEERR_UNINITIALIZED.




## -remarks



If LINEERR_INVALLINESTATE is returned, the line is currently not in a state in which this operation can be performed. A list of currently valid operations can be found in the <b>dwLineFeatures</b> member (of the type 
<a href="https://msdn.microsoft.com/77fa313c-e720-4607-b691-51b5be76ceed">LINEFEATURE</a>) in the 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a> structure. (Calling 
<a href="https://msdn.microsoft.com/9c0fa2ba-1157-43d2-af56-aa4e0c28bd05">lineGetLineDevStatus</a> updates the information in 
<b>LINEDEVSTATUS</b>.)

A conference call handle can be obtained with 
<a href="https://msdn.microsoft.com/13bf81c6-f7f6-4fd4-b546-15e58f7bc618">lineSetupConference</a> or with 
<a href="https://msdn.microsoft.com/ebedf664-4c45-49c3-9d86-c3d782077a00">lineCompleteTransfer</a> that is resolved as a three-way conference call. The 
<b>linePrepareAddToConference</b> function typically places the existing conference call in the <i>onHoldPendingConference</i> state and creates a consultation call that can be added later to the existing conference call with 
<a href="https://msdn.microsoft.com/fbbaea96-727c-46b9-91d1-31d3f89d8ad8">lineAddToConference</a>.

The consultation call can be canceled using 
<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>. It may also be possible for an application to swap between the consultation call and the held conference call with 
<a href="https://msdn.microsoft.com/9e575c82-301c-4505-b400-faf4dc291ff8">lineSwapHold</a>.




## -see-also




<a href="https://msdn.microsoft.com/f685097b-1b54-412b-999f-d9bdb3120ab9">Conference overview</a>



<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a>



<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/fbbaea96-727c-46b9-91d1-31d3f89d8ad8">lineAddToConference</a>



<a href="https://msdn.microsoft.com/ebedf664-4c45-49c3-9d86-c3d782077a00">lineCompleteTransfer</a>



<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>



<a href="https://msdn.microsoft.com/9c0fa2ba-1157-43d2-af56-aa4e0c28bd05">lineGetLineDevStatus</a>



<a href="https://msdn.microsoft.com/13bf81c6-f7f6-4fd4-b546-15e58f7bc618">lineSetupConference</a>



<a href="https://msdn.microsoft.com/9e575c82-301c-4505-b400-faf4dc291ff8">lineSwapHold</a>
 

 

