---
UID: NF:tapi.phoneGetLamp
title: phoneGetLamp function
author: windows-driver-content
description: The phoneGetLamp function returns the current lamp mode of the specified lamp.
old-location: tapi2\phonegetlamp.htm
old-project: Tapi
ms.assetid: 97bc1dc1-ac7e-479f-8fea-e2fcca88367b
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "_tapi2_phonegetlamp, phoneGetLamp, phoneGetLamp function [TAPI 2.2], tapi/phoneGetLamp, tapi2.phonegetlamp"
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
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	phoneGetLamp
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneGetLamp function


## -description


The 
<b>phoneGetLamp</b> function returns the current lamp mode of the specified lamp.


## -parameters




### -param hPhone

Handle to the open phone device.


### -param dwButtonLampID

Identifier of the lamp to be queried.


### -param lpdwLampMode

Pointer to a memory location that holds the lamp mode status of the given lamp. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe">PHONELAMPMODE_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.




## -remarks



Phone sets that have multiple lamps per button should be modeled using multiple button/lamp pairs. Each extra button/lamp pair should use a DUMMY button.




## -see-also




<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

