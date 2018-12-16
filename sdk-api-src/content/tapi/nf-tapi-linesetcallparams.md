---
UID: NF:tapi.lineSetCallParams
title: lineSetCallParams function
author: windows-sdk-content
description: The lineSetCallParams function allows an application to change bearer mode and/or the rate parameters of an existing call.
old-location: tapi2\linesetcallparams.htm
tech.root: tapi
ms.assetid: c8088116-2bfc-420f-a83a-d00c7947b6e7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linesetcallparams, lineSetCallParams, lineSetCallParams function [TAPI 2.2], tapi/lineSetCallParams, tapi2.linesetcallparams"
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
 - lineSetCallParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetCallParams function


## -description


The 
<b>lineSetCallParams</b> function allows an application to change bearer mode and/or the rate parameters of an existing call.


## -parameters




### -param hCall

Handle to the call whose parameters are to be changed. The application must be an owner of the call. The call state of <i>hCall</i> can be any state except <i>idle</i> or <i>disconnected</i>.
					


### -param dwBearerMode

New bearer mode for the call. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/87e46ec9-ed5f-4ff5-a382-34eb164f4e66">LINEBEARERMODE_ Constants</a>.


### -param dwMinRate

Lower bound for the call's new data rate. The application can accept a new rate as low as this one.


### -param dwMaxRate

Upper bound for the call's new data rate. This is the maximum data rate the application can accept. If an exact data rate is required, <i>dwMinRate</i> and <i>dwMaxRate</i> should be equal.


### -param lpDialParams

Pointer to the new dial parameters for the call, of type 
<a href="https://msdn.microsoft.com/efb65462-abe5-46db-9299-97871e0d011e">LINEDIALPARAMS</a>. This parameter can be left <b>NULL</b> if the call's current dialing parameters are to be used.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_BEARERMODEUNAVAIL, LINEERR_NOTOWNER, LINEERR_INVALBEARERMODE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSTATE, LINEERR_RATEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALRATE, LINEERR_UNINITIALIZED, LINEERR_NOMEM.




## -remarks



This operation is used to change the parameters of an existing call. Examples of its usage include changing the bearer mode and/or the data rate of an existing call.




## -see-also




<a href="https://msdn.microsoft.com/efb65462-abe5-46db-9299-97871e0d011e">LINEDIALPARAMS</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

