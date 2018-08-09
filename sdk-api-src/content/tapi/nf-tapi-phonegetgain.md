---
UID: NF:tapi.phoneGetGain
title: phoneGetGain function
author: windows-sdk-content
description: The phoneGetGain function returns the gain setting of the microphone of the specified phone's hookswitch device.
old-location: tapi2\phonegetgain.htm
old-project: tapi
ms.assetid: ea6ba2f0-ff79-41b8-9165-bb250077b2dc
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_phonegetgain, phoneGetGain, phoneGetGain function [TAPI 2.2], tapi/phoneGetGain, tapi2.phonegetgain"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneGetGain
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneGetGain function


## -description


The 
<b>phoneGetGain</b> function returns the gain setting of the microphone of the specified phone's hookswitch device.


## -parameters




### -param hPhone

Handle to the open phone device.


### -param dwHookSwitchDev

Hookswitch device whose gain level is queried. The <i>dwHookSwitchDev</i> parameter can have only one bit set. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ Constants</a>.


### -param lpdwGain

Pointer to a <b>DWORD</b> containing the current gain setting of the hookswitch microphone component. The <i>dwGain</i> parameter specifies the volume level of the hookswitch device. This is a number in the range 0x00000000 (silence) to 0x0000FFFF (maximum volume). The actual granularity and quantization of gain settings in this range are service provider-specific.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALHOOKSWITCHDEV, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

