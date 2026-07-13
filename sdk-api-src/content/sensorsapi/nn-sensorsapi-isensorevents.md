---
UID: NN:sensorsapi.ISensorEvents
title: ISensorEvents (sensorsapi.h)
description: The callback interface you must implement if you want to receive sensor events.
helpviewer_keywords: ["ISensorEvents","ISensorEvents interface [WinSensors]","ISensorEvents interface [WinSensors]","described","sensorsapi/ISensorEvents","winsensors.isensorevents"]
old-location: winsensors\isensorevents.htm
tech.root: winsensors
ms.assetid: 41acbb4f-b4f8-4573-a993-ed93ec9494f0
ms.date: 09/19/2025
ms.keywords: ISensorEvents, ISensorEvents interface [WinSensors], ISensorEvents interface [WinSensors],described, sensorsapi/ISensorEvents, winsensors.isensorevents
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISensorEvents
 - sensorsapi/ISensorEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensorEvents
---

# ISensorEvents interface


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

The callback interface you must implement if you want to receive sensor events.

To subscribe to events for a particular sensor, call <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensor-seteventsink">ISensor::SetEventSink</a>.

In addition to the methods inherited from <b>IUnknown</b>, the <b>ISensorEvents</b> interface exposes the following methods.

## -see-also

<a href="/windows/desktop/SensorsAPI/windows-sensors-com-interfaces">COM Interfaces</a>