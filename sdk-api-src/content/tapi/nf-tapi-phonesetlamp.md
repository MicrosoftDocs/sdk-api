---
UID: NF:tapi.phoneSetLamp
title: phoneSetLamp function
author: windows-driver-content
description: The phoneSetLamp function causes the specified lamp to be lit on the specified open phone device in the specified lamp mode.
old-location: tapi2\phonesetlamp.htm
old-project: Tapi
ms.assetid: 2e21ef29-9c40-4463-8678-028a8772a494
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "_tapi2_phonesetlamp, phoneSetLamp, phoneSetLamp function [TAPI 2.2], tapi/phoneSetLamp, tapi2.phonesetlamp"
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
-	phoneSetLamp
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneSetLamp function


## -description


The 
<b>phoneSetLamp</b> function causes the specified lamp to be lit on the specified open phone device in the specified lamp mode.


## -parameters




### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.


### -param dwButtonLampID

Button whose lamp is to be lit.


### -param dwLampMode

How the lamp is to be lit. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe">PHONELAMPMODE_ Constants</a>.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding <a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOTOWNER, PHONEERR_NOMEM, PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALLAMPMODE, PHONEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

