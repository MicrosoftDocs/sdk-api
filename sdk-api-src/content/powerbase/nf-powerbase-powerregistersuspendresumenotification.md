---
UID: NF:powerbase.PowerRegisterSuspendResumeNotification
title: PowerRegisterSuspendResumeNotification function (powerbase.h)
description: Registers to receive notification when the system is suspended or resumed.
helpviewer_keywords: ["PowerRegisterSuspendResumeNotification","PowerRegisterSuspendResumeNotification function","base.powerregistersuspendresumenotification","powerbase/PowerRegisterSuspendResumeNotification"]
old-location: base\powerregistersuspendresumenotification.htm
tech.root: base
ms.assetid: 3b39ec3a-417c-4ce4-a581-ed967f1baec9
ms.date: 12/05/2018
ms.keywords: PowerRegisterSuspendResumeNotification, PowerRegisterSuspendResumeNotification function, base.powerregistersuspendresumenotification, powerbase/PowerRegisterSuspendResumeNotification
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerRegisterSuspendResumeNotification
 - powerbase/PowerRegisterSuspendResumeNotification
dev_langs:
 - c++
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
---

# PowerRegisterSuspendResumeNotification function


## -description

Registers to receive notification when the system is suspended or resumed.

## -parameters

### -param Flags [in]

 This parameter must be <b>DEVICE_NOTIFY_CALLBACK</b>.

### -param Recipient [in]

This parameter is a pointer to a <a href="/windows/win32/api/powrprof/ns-powrprof-device_notify_subscribe_parameters">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a> structure. In this case, the callback function is <a href="/windows/desktop/api/powrprof/nc-powrprof-device_notify_callback_routine">DeviceNotifyCallbackRoutine</a>. When the <b>Callback</b> function executes, the  <i>Type</i> parameter is set indicating the type of event that occurred. Possible values include <b>PBT_APMSUSPEND</b>, <b>PBT_APMRESUMESUSPEND</b>, and <b>PBT_APMRESUMEAUTOMATIC</b> - see  <a href="/windows/desktop/Power/power-management-events">Power Management Events</a> for more info. The <i>Setting</i> parameter is not used with suspend/resume notifications.

### -param RegistrationHandle [out]

A handle to the registration. Use this handle to unregister for notifications.

## -returns

Returns ERROR_SUCCESS (zero) if the call was successful, and a nonzero value if the call failed.

## -see-also

<a href="/windows/desktop/api/powrprof/nc-powrprof-device_notify_callback_routine">DEVICE_NOTIFY_CALLBACK_ROUTINE</a>



<a href="/windows/win32/api/powrprof/ns-powrprof-device_notify_subscribe_parameters">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a>



<a href="/windows/desktop/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification">PowerUnregisterSuspendResumeNotification</a>