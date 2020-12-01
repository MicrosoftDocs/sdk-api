---
UID: NC:powrprof.DEVICE_NOTIFY_CALLBACK_ROUTINE
title: DEVICE_NOTIFY_CALLBACK_ROUTINE (powrprof.h)
description: An application's DeviceNotifyCallbackRoutine callback function is used for receiving power notifications.
helpviewer_keywords: ["DEVICE_NOTIFY_CALLBACK_ROUTINE","DEVICE_NOTIFY_CALLBACK_ROUTINE callback function","DeviceNotifyCallbackRoutine","DeviceNotifyCallbackRoutine callback","DeviceNotifyCallbackRoutine callback function","PDEVICE_NOTIFY_CALLBACK_ROUTINE","PDEVICE_NOTIFY_CALLBACK_ROUTINE callback function pointer","base.device_notify_callback_routine","powrprof/DeviceNotifyCallbackRoutine","powrprof/PDEVICE_NOTIFY_CALLBACK_ROUTINE"]
old-location: base\device_notify_callback_routine.htm
tech.root: base
ms.assetid: 5734FDEE-E330-4115-AFA5-725114023A5A
ms.date: 12/05/2018
ms.keywords: DEVICE_NOTIFY_CALLBACK_ROUTINE, DEVICE_NOTIFY_CALLBACK_ROUTINE callback function, DeviceNotifyCallbackRoutine, DeviceNotifyCallbackRoutine callback, DeviceNotifyCallbackRoutine callback function, PDEVICE_NOTIFY_CALLBACK_ROUTINE, PDEVICE_NOTIFY_CALLBACK_ROUTINE callback function pointer, base.device_notify_callback_routine, powrprof/DeviceNotifyCallbackRoutine, powrprof/PDEVICE_NOTIFY_CALLBACK_ROUTINE
req.header: powrprof.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DEVICE_NOTIFY_CALLBACK_ROUTINE
 - powrprof/DEVICE_NOTIFY_CALLBACK_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Powrprof.h
api_name:
 - DEVICE_NOTIFY_CALLBACK_ROUTINE
---

# DEVICE_NOTIFY_CALLBACK_ROUTINE callback function


## -description

An application's 
    <i>DeviceNotifyCallbackRoutine</i> 
    callback function is used for receiving power notifications.

## -parameters

### -param Context

The context provided when registering for the power notification.

### -param Type

The type of power event that caused this notification.

### -param Setting

The value of this parameter depends on the type of notification subscribed to.

## -returns

This function returns a Windows error code.

## -see-also

<a href="/windows/win32/api/powrprof/ns-powrprof-device_notify_subscribe_parameters">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a>



<a href="/windows/desktop/api/powerbase/nf-powerbase-powerregistersuspendresumenotification">PowerRegisterSuspendResumeNotification</a>