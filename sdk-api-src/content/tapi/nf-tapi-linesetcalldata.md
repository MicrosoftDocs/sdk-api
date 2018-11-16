---
UID: NF:tapi.lineSetCallData
title: lineSetCallData function
author: windows-sdk-content
description: The lineSetCallData function sets the CallData member in LINECALLINFO.
old-location: tapi2\linesetcalldata.htm
tech.root: Tapi
ms.assetid: f428f952-f8ff-4b55-a957-58fdb35a8c0e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_tapi2_linesetcalldata, lineSetCallData, lineSetCallData function [TAPI 2.2], tapi/lineSetCallData, tapi2.linesetcalldata"
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
 - lineSetCallData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- lineSetCallData
: 
---

# lineSetCallData function


## -description


The 
<b>lineSetCallData</b> function sets the <b>CallData</b> member in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>. Depending on the service provider implementation, the <b>CallData</b> member can be propagated to all applications having handles to the call, including those on other machines (through the server), and can travel with the call when it is transferred.


## -parameters




### -param hCall

Handle to the call. The application must have OWNER privilege.


### -param lpCallData

Address of the data to be copied to the <b>CallData</b> member in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>, replacing any existing data. For more information, see the 
<a href="https://msdn.microsoft.com/8b7a674f-ba78-4830-bb20-7fa74e202a1a">call data</a> topic.


### -param dwSize

Number of bytes of data to be copied. A value of 0 causes any existing data to be removed. 




<div class="alert"><b>Note</b>  If <i>lpCallData</i> is a pointer to a string, the size must include the null terminator.</div>
<div> </div>

## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALCALLHANDLE, LINEERR_INVALCALLSTATE, LINEERR_INVALPARAM, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_NOTOWNER, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

