---
UID: NF:tapi.phoneSetGain
title: phoneSetGain function
author: windows-driver-content
description: The phoneSetGain function sets the gain of the microphone of the specified hookswitch device to the specified gain level.
old-location: tapi2\phonesetgain.htm
old-project: Tapi
ms.assetid: 24e6047c-ca70-4e97-acb5-37647c5306c3
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "_tapi2_phonesetgain, phoneSetGain, phoneSetGain function [TAPI 2.2], tapi/phoneSetGain, tapi2.phonesetgain"
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
-	phoneSetGain
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneSetGain function


## -description


The 
<b>phoneSetGain</b> function sets the gain of the microphone of the specified hookswitch device to the specified gain level.


## -parameters




### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.


### -param dwHookSwitchDev

Hookswitch device whose microphone's gain is to be set. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ Constants</a>.


### -param dwGain

Pointer to a <b>DWORD</b> containing the new gain setting of the device. The <i>dwGain</i> parameter specifies the gain level of the hookswitch device. This is a number in the range 0x00000000 (silence) to 0x0000FFFF (maximum volume). The actual granularity and quantization of gain settings in this range are service provider-specific. A value for <i>dwGain</i> that is out of range is set to the nearest value in the range.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding <a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_NOTOWNER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

