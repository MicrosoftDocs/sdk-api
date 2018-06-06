---
UID: NF:tapi.phoneSetStatusMessages
title: phoneSetStatusMessages function
author: windows-sdk-content
description: The phoneSetStatusMessages function enables an application to monitor the specified phone device for selected status events.
old-location: tapi2\phonesetstatusmessages.htm
old-project: Tapi
ms.assetid: eb3b6ea8-447f-44df-a0fb-9ab50d6471f8
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_phonesetstatusmessages, phoneSetStatusMessages, phoneSetStatusMessages function [TAPI 2.2], tapi/phoneSetStatusMessages, tapi2.phonesetstatusmessages"
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
 - phoneSetStatusMessages
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneSetStatusMessages function


## -description


The 
<b>phoneSetStatusMessages</b> function enables an application to monitor the specified phone device for selected status events.


## -parameters




### -param hPhone

Handle to the open phone device to be monitored.


### -param dwPhoneStates

Set of phone status changes and events for which the application can receive notification messages. This parameter can have zero, one, or more of the 
<a href="https://msdn.microsoft.com/5db53dd4-606a-40b9-9159-b67a0ea1e400">PHONESTATE_ Constants</a>.


### -param dwButtonModes

Set of phone-button modes for which the application can receive notification messages. This parameter can have zero, one, or more of the 
<a href="https://msdn.microsoft.com/7bf337ee-acda-42fe-b50b-370aad50dc03">PHONEBUTTONMODE_ Constants</a>.


### -param dwButtonStates

Set of phone-button state changes for which the application can receive notification messages. If the <i>dwButtonModes</i> parameter is zero, <i>dwButtonStates</i> is ignored. If <i>dwButtonModes</i> has one or more bits set, this parameter must also have at least one bit set. This parameter uses the 
<a href="https://msdn.microsoft.com/f1196e31-65c6-4ade-a0b7-c7758ce97be1">PHONEBUTTONSTATE_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPHONESTATE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALBUTTONMODE, PHONEERR_OPERATIONFAILED, PHONEERR_INVALBUTTONSTATE, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONUNAVAIL.




## -remarks



An application can use the 
<b>phoneSetStatusMessages</b> function to enable or disable the generation of the corresponding messages. All phone status messages are disabled by default.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/84650abf-235e-4792-a67d-2f0f08b85a32">PHONE_CLOSE</a>



<a href="https://msdn.microsoft.com/74e74b62-8387-4056-83e6-2350b3da4077">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/7bfef6d7-d5fd-4887-afb8-b1d850df050d">phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/e06153c1-707e-45a9-8d26-747d53e16cf2">phoneInitialize</a>



<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>



<a href="https://msdn.microsoft.com/8fba6d5e-0d8c-488f-a17c-4852b487e300">phoneOpen</a>
 

 

