---
UID: NF:tapi.phoneGetHookSwitch
title: phoneGetHookSwitch function
author: windows-sdk-content
description: The phoneGetHookSwitch function returns the current hookswitch mode of the specified open phone device.
old-location: tapi2\phonegethookswitch.htm
old-project: Tapi
ms.assetid: 246f8b2b-8748-453d-b2b6-16771c0aad36
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "_tapi2_phonegethookswitch, phoneGetHookSwitch, phoneGetHookSwitch function [TAPI 2.2], tapi/phoneGetHookSwitch, tapi2.phonegethookswitch"
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
 - phoneGetHookSwitch
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneGetHookSwitch function


## -description


The 
<b>phoneGetHookSwitch</b> function returns the current hookswitch mode of the specified open phone device.


## -parameters




### -param hPhone

Handle to the open phone device.


### -param lpdwHookSwitchDevs

Pointer to a <b>DWORD</b> to be filled with the mode of the phone's hookswitch devices. If a bit position is <b>FALSE</b>, the corresponding hookswitch device is onhook; if <b>TRUE</b>, the microphone and/or speaker part of the corresponding hookswitch device is offhook. To find out whether the microphone and/or speaker are enabled, the application can use 
<a href="https://msdn.microsoft.com/d2e9e209-54f5-4895-b57a-a5f4c24e063e">phoneGetStatus</a>. This parameter uses one or more of the 
<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED.




## -remarks



After the hookswitch state of a device changes, and if hookswitch monitoring is enabled, the application is sent a 
<a href="https://msdn.microsoft.com/74e74b62-8387-4056-83e6-2350b3da4077">PHONE_STATE</a> message.




## -see-also




<a href="https://msdn.microsoft.com/74e74b62-8387-4056-83e6-2350b3da4077">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/d2e9e209-54f5-4895-b57a-a5f4c24e063e">phoneGetStatus</a>
 

 

