---
UID: NF:tapi.phoneGetStatusMessages
title: phoneGetStatusMessages function
author: windows-sdk-content
description: The phoneGetStatusMessages function returns which phone-state changes on the specified phone device generate a callback to the application.
old-location: tapi2\phonegetstatusmessages.htm
tech.root: Tapi
ms.assetid: 3ee182cf-20e2-4745-9aee-d5de8b44c1b4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "_tapi2_phonegetstatusmessages, phoneGetStatusMessages, phoneGetStatusMessages function [TAPI 2.2], tapi/phoneGetStatusMessages, tapi2.phonegetstatusmessages"
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
 - phoneGetStatusMessages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# phoneGetStatusMessages function


## -description


The 
<b>phoneGetStatusMessages</b> function returns which phone-state changes on the specified phone device generate a callback to the application.


## -parameters




### -param hPhone

Handle to the open phone device to be monitored.


### -param lpdwPhoneStates

Pointer to a <b>DWORD</b> holding zero, one or more of the 
<a href="https://msdn.microsoft.com/5db53dd4-606a-40b9-9159-b67a0ea1e400">PHONESTATE_ Constants</a>. These flags specify the set of phone status changes and events for which the application can receive notification messages. Monitoring can be individually enabled and disabled.


### -param lpdwButtonModes

Pointer to a <b>DWORD</b> containing flags that specify the set of phone-button modes for which the application can receive notification messages. This parameter uses zero, one or more of the 
<a href="https://msdn.microsoft.com/7bf337ee-acda-42fe-b50b-370aad50dc03">PHONEBUTTONMODE_ Constants</a>.


### -param lpdwButtonStates

Pointer to a <b>DWORD</b> that contains flags specifying the set of phone button state changes for which the application can receive notification messages. This parameter uses zero, one or more of the 
<a href="https://msdn.microsoft.com/f1196e31-65c6-4ade-a0b7-c7758ce97be1">PHONEBUTTONSTATE_ Constants</a>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_OPERATIONFAILED, PHONEERR_UNINITIALIZED.




## -remarks



An application can use 
<b>phoneGetStatusMessages</b> to query the generation of the corresponding messages. Message generation can be controlled by 
<b>phoneGetStatusMessages</b>. All phone status messages are disabled by default.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/84650abf-235e-4792-a67d-2f0f08b85a32">PHONE_CLOSE</a>



<a href="https://msdn.microsoft.com/74e74b62-8387-4056-83e6-2350b3da4077">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/7bfef6d7-d5fd-4887-afb8-b1d850df050d">phoneGetDevCaps</a>



<a href="https://msdn.microsoft.com/eb3b6ea8-447f-44df-a0fb-9ab50d6471f8">phoneSetStatusMessages</a>
 

 

