---
UID: NS:powrprof._DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
title: DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS (powrprof.h)
description: Contains parameters used when registering for a power notification.
helpviewer_keywords: ["*PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS","DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS","DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS structure","PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS","PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS structure pointer","base.device_notify_subscribe_parameters","powrprof/DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS","powrprof/PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS"]
old-location: base\device_notify_subscribe_parameters.htm
tech.root: base
ms.assetid: 749F7C6F-1A42-43DE-921E-C3654034570D
ms.date: 12/05/2018
ms.keywords: '*PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS structure, PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS structure pointer, base.device_notify_subscribe_parameters, powrprof/DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, powrprof/PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS'
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
req.typenames: DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, *PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
 - powrprof/_DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
 - PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
 - powrprof/PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
 - DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
 - powrprof/DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Powrprof.h
api_name:
 - DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
---

# DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS structure


## -description

Contains parameters used when registering for a power notification.

## -struct-fields

### -field Callback

Indicates the callback function that will be called when the application receives the notification.

### -field Context

The context of the application registering for the notification.

## -see-also

<a href="/windows/desktop/api/powrprof/nc-powrprof-device_notify_callback_routine">DEVICE_NOTIFY_CALLBACK_ROUTINE</a>



<a href="/windows/desktop/api/powerbase/nf-powerbase-powerregistersuspendresumenotification">PowerRegisterSuspendResumeNotification</a>