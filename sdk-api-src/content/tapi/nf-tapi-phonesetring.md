---
UID: NF:tapi.phoneSetRing
title: phoneSetRing function
author: windows-driver-content
description: The phoneSetRing function rings the specified open phone device using the specified ring mode and volume.
old-location: tapi2\phonesetring.htm
old-project: Tapi
ms.assetid: 14aca99e-e190-4c48-95f2-0b2a3ba3de3f
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: "_tapi2_phonesetring, phoneSetRing, phoneSetRing function [TAPI 2.2], tapi/phoneSetRing, tapi2.phonesetring"
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
-	phoneSetRing
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneSetRing function


## -description


The 
<b>phoneSetRing</b> function rings the specified open phone device using the specified ring mode and volume.


## -parameters




### -param hPhone

Handle to the open phone device. The application must be the owner of the phone device.


### -param dwRingMode

Ringing pattern with which to ring the phone. This parameter must be within the range of zero to the value of the <b>dwNumRingModes</b> member in the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure. If <b>dwNumRingModes</b> is zero, the ring mode of the phone cannot be controlled; if <b>dwNumRingModes</b> is 1, a value of 0 for <i>dwRingMode</i> indicates that the phone should not be rung (silence), and other values from 1 to <b>dwNumRingModes</b> are valid ring modes for the phone device.


### -param dwVolume

Volume level with which the phone is ringing. This is a number in the range 0x00000000 (silence) to 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service provider-specific. A value for <i>dwVolume</i> that is out of range is set to the nearest value in the range.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_NOTOWNER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALRINGMODE, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.




## -remarks



The service provider defines the actual audible ringing patterns corresponding to each of the phone's ring modes.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

