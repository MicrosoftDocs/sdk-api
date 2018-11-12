---
UID: NF:tapi.lineSwapHold
title: lineSwapHold function
author: windows-sdk-content
description: The lineSwapHold function swaps the specified active call with the specified call on consultation hold.
old-location: tapi2\lineswaphold.htm
tech.root: tapi
ms.assetid: 9e575c82-301c-4505-b400-faf4dc291ff8
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_tapi2_lineswaphold, lineSwapHold, lineSwapHold function [TAPI 2.2], tapi/lineSwapHold, tapi2.lineswaphold"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - lineSwapHold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSwapHold function


## -description


The 
<b>lineSwapHold</b> function swaps the specified active call with the specified call on consultation hold.


## -parameters




### -param hActiveCall

Handle to the active call. The application must be an owner of the call. The call state of <i>hActiveCall</i> must be <i>connected</i>.


### -param hHeldCall

Handle to the consultation call. The application must be an owner of the call. The call state of <i>hHeldCall</i> can be <i>onHoldPendingTransfer</i>, <i>onHoldPendingConference</i>, or <i>onHold</i>.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.




## -remarks



Swapping the active call with the call on consultation hold allows the application to alternate or toggle between these two calls. This is typical in call waiting.




## -see-also




<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

