---
UID: NF:tspi.TSPI_lineSwapHold
title: TSPI_lineSwapHold function
author: windows-sdk-content
description: The TSPI_lineSwapHold function swaps the specified active call with the specified call on consultation hold.
old-location: tspi\tspi_lineswaphold.htm
tech.root: tapi
ms.assetid: 9ecd6a63-e906-483b-b404-28797d259149
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: TSPI_lineSwapHold, TSPI_lineSwapHold function [TAPI 2.2], _tspi_tspi_lineswaphold, tspi.tspi_lineswaphold, tspi/TSPI_lineSwapHold
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
 - TSPI_lineSwapHold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineSwapHold function


## -description


The 
<b>TSPI_lineSwapHold</b> function swaps the specified active call with the specified call on consultation hold.


## -parameters




### -param dwRequestID

The identifier of the asynchronous request.


### -param hdActiveCall

The handle to the call to be swapped with the call on consultation hold. The call state of <i>hdActiveCall</i> can be <i>connected</i>.


### -param hdHeldCall

The handle to the consultation call. The call state of <i>hdHeldCall</i> can be <i>onHoldPendingTransfer</i>, <i>onHoldPendingConference</i>, or <i>onHold</i>.


## -returns



Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.




## -remarks



The service provider must send 
<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a> messages for the call transitions.




## -see-also




<a href="https://msdn.microsoft.com/673c9d23-e380-49f7-bd06-23552634d5b9">ASYNC_COMPLETION</a>



<a href="https://msdn.microsoft.com/9070d6d2-f92c-4e07-8281-5b7e82862aaf">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/71b9720b-54dc-44a7-9fad-38dcd9f57ab3">TSPI_lineSetupConference</a>



<a href="https://msdn.microsoft.com/0cd95e53-62d5-4318-961a-1136646fd222">TSPI_lineSetupTransfer</a>
 

 

