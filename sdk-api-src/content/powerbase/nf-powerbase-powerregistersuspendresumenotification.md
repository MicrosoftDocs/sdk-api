---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PowerRegisterSuspendResumeNotification function


## -description


Registers to receive notification when the system is suspended or resumed. 


## -parameters




### -param Flags [in]

 This parameter must be <b>DEVICE_NOTIFY_CALLBACK</b>.


### -param Recipient [in]

This parameter is a pointer to a <a href="https://msdn.microsoft.com/749F7C6F-1A42-43DE-921E-C3654034570D">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a> structure. In this case, the callback function is <a href="https://msdn.microsoft.com/5734FDEE-E330-4115-AFA5-725114023A5A">DeviceNotifyCallbackRoutine</a>. When the <b>Callback</b> function executes, the  <i>Type</i> parameter is set indicating the type of event that occurred. Possible values include <b>PBT_APMSUSPEND</b>, <b>PBT_APMRESUMESUSPEND</b>, and <b>PBT_APMRESUMEAUTOMATIC</b> - see  <a href="https://msdn.microsoft.com/2315e17f-f0c1-409c-b1c0-b3735c25c4c1">Power Management Events</a> for more info. The <i>Setting</i> parameter is not used with suspend/resume notifications.


### -param RegistrationHandle [out]

A handle to the registration. Use this handle to unregister for notifications.


## -returns



Returns ERROR_SUCCESS (zero) if the call was successful, and a nonzero value if the call failed. 




## -see-also




<a href="https://msdn.microsoft.com/5734FDEE-E330-4115-AFA5-725114023A5A">DEVICE_NOTIFY_CALLBACK_ROUTINE</a>



<a href="https://msdn.microsoft.com/749F7C6F-1A42-43DE-921E-C3654034570D">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/5680e6bd-1694-4d5f-94ea-41b24149c741">PowerUnregisterSuspendResumeNotification</a>
 

 

