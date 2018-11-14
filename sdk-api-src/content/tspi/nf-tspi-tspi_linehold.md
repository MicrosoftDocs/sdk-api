---
UID: NF:tspi.TSPI_lineHold
title: TSPI_lineHold function
author: windows-sdk-content
description: The TSPI_lineHold function places the specified call on hold.
old-location: tspi\tspi_linehold.htm
tech.root: tapi
ms.assetid: 395aa8cc-fdbf-4772-940b-ea5944b26812
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: TSPI_lineHold, TSPI_lineHold function [TAPI 2.2], _tspi_tspi_linehold, tspi.tspi_linehold, tspi/TSPI_lineHold
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
 - TSPI_lineHold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- TSPI_lineHold
: 
---

# TSPI_lineHold function


## -description


The 
<b>TSPI_lineHold</b> function places the specified call on hold.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdCall

The service provider's handle to the call to be placed on hold. The call state of <i>hdCall</i> can be <i>connected</i>.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.




## -remarks



The call on hold is temporarily disconnected, allowing TAPI to use the line device for making or answering other calls. 
<b>TSPI_lineHold</b> performs a <i>hard hold</i> of the specified call, as opposed to a <i>consultation call</i>. A call on hard hold typically cannot be transferred or included in a conference call, whereas a consultation call can. Consultation calls are initiated using 
<a href="https://msdn.microsoft.com/0cd95e53-62d5-4318-961a-1136646fd222">TSPI_lineSetupTransfer</a>, 
<a href="https://msdn.microsoft.com/71b9720b-54dc-44a7-9fad-38dcd9f57ab3">TSPI_lineSetupConference</a>, or 
<a href="https://msdn.microsoft.com/84642d7d-7673-45f1-91fb-aede75e51029">TSPI_linePrepareAddToConference</a>.

After a call is successfully placed on hold, the call state typically transitions to <i>onHold</i>. A held call is retrieved through 
<a href="https://msdn.microsoft.com/4719c399-0dce-4aa2-9b6e-a84ad13f9228">TSPI_lineUnhold</a>. While a call is on hold, the service provider can send 
<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a> messages about state changes of the held call. For example, if the held party hangs up, the call state can transition to <i>disconnected</i>, and the service provider can send a LINE_CALLSTATE message indicating the new state.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/71b9720b-54dc-44a7-9fad-38dcd9f57ab3">TSPI_lineSetupConference</a>



<a href="https://msdn.microsoft.com/0cd95e53-62d5-4318-961a-1136646fd222">TSPI_lineSetupTransfer</a>



<a href="https://msdn.microsoft.com/4719c399-0dce-4aa2-9b6e-a84ad13f9228">TSPI_lineUnhold</a>
 

 

