---
UID: NF:tapi.phoneSetVolume
title: phoneSetVolume function
author: windows-sdk-content
description: The phoneSetVolume function sets the volume of the speaker component of the specified hookswitch device to the specified level.
old-location: tapi2\phonesetvolume.htm
tech.root: tapi
ms.assetid: 114aba48-f058-47c9-9ee7-493bd758b8a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_phonesetvolume, phoneSetVolume, phoneSetVolume function [TAPI 2.2], tapi/phoneSetVolume, tapi2.phonesetvolume"
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
 - phoneSetVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# phoneSetVolume function


## -description


The 
<b>phoneSetVolume</b> function sets the volume of the speaker component of the specified hookswitch device to the specified level.


## -parameters




### -param hPhone

Handle to the open phone device. The application must be the owner of the phone.


### -param dwHookSwitchDev

Hookswitch device whose speaker's volume is to be set, one of the 
<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ Constants</a>.


### -param dwVolume

New volume setting of the device. The <i>dwVolume</i> parameter specifies the volume level of the hookswitch device. This is a number in the range 0x00000000 (silence) to 0x0000FFFF (maximum volume). The actual granularity and quantization of volume settings in this range are service provider-specific. A value for <i>dwVolume</i> that is out of range is set to the nearest value in the range.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_NOTOWNER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

