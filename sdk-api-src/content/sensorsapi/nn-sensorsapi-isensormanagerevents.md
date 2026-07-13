---
UID: NN:sensorsapi.ISensorManagerEvents
title: ISensorManagerEvents (sensorsapi.h)
description: The callback interface for receiving sensor manager events.
helpviewer_keywords: ["ISensorManagerEvents","ISensorManagerEvents interface [WinSensors]","ISensorManagerEvents interface [WinSensors]","described","sensorsapi/ISensorManagerEvents","winsensors.isensormanagerevents"]
old-location: winsensors\isensormanagerevents.htm
tech.root: winsensors
ms.assetid: b111a717-00c0-47cb-be6a-3050d54cd2ec
ms.date: 09/19/2025
ms.keywords: ISensorManagerEvents, ISensorManagerEvents interface [WinSensors], ISensorManagerEvents interface [WinSensors],described, sensorsapi/ISensorManagerEvents, winsensors.isensormanagerevents
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
 - ISensorManagerEvents
 - sensorsapi/ISensorManagerEvents
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
 - ISensorManagerEvents
---

# ISensorManagerEvents interface


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

The callback interface for receiving sensor manager events.

To receive event notifications, first call <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink">ISensorManager::SetEventSink</a>.

## -see-also

<a href="/windows/desktop/SensorsAPI/windows-sensors-com-interfaces">COM Interfaces</a>