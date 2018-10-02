---
UID: NF:tapi.lineUnhold
title: lineUnhold function
author: windows-sdk-content
description: The lineUnhold function retrieves the specified held call.
old-location: tapi2\lineunhold.htm
tech.root: TAPI
ms.assetid: c32d8d3a-f54c-411a-ae86-4aecd6dce456
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: "_tapi2_lineunhold, lineUnhold, lineUnhold function [TAPI 2.2], tapi/lineUnhold, tapi2.lineunhold"
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
 - lineUnhold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineUnhold function


## -description


The 
<b>lineUnhold</b> function retrieves the specified held call.


## -parameters




### -param hCall

Handle to the call to be retrieved. The application must be an owner of this call. The call state of <i>hCall</i> must be <i>onHold</i>, <i>onHoldPendingTransfer</i>, or <i>onHoldPendingConference</i>.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding <a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

