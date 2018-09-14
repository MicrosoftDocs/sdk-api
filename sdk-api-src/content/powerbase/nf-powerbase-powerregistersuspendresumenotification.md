---
UID: NF:powerbase.PowerRegisterSuspendResumeNotification
title: PowerRegisterSuspendResumeNotification function
author: windows-sdk-content
description: Registers to receive notification when the system is suspended or resumed.
old-location: base\powerregistersuspendresumenotification.htm
tech.root: power
ms.assetid: 3b39ec3a-417c-4ce4-a581-ed967f1baec9
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: PowerRegisterSuspendResumeNotification, PowerRegisterSuspendResumeNotification function, base.powerregistersuspendresumenotification, powerbase/PowerRegisterSuspendResumeNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: powerbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Powrprof.dll
 - API-MS-Win-power-base-l1-1-0.dll
api_name:
 - PowerRegisterSuspendResumeNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

