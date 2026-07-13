---
UID: NN:sensorsapi.ISensorManager
title: ISensorManager (sensorsapi.h)
description: Provides methods for discovering and retrieving available sensors and a method to request sensor manager events.
helpviewer_keywords: ["ISensorManager","ISensorManager interface [WinSensors]","ISensorManager interface [WinSensors]","described","sensorsapi/ISensorManager","winsensors.isensormanager"]
old-location: winsensors\isensormanager.htm
tech.root: winsensors
ms.assetid: 313742c9-58a7-4ddd-9582-a6ee276e97d0
ms.date: 09/19/2025
ms.keywords: ISensorManager, ISensorManager interface [WinSensors], ISensorManager interface [WinSensors],described, sensorsapi/ISensorManager, winsensors.isensormanager
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
 - ISensorManager
 - sensorsapi/ISensorManager
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
 - ISensorManager
---

# ISensorManager interface


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Provides methods for discovering and retrieving available sensors and a method to request sensor manager events.

## -remarks

You retrieve a pointer to this interface by calling the COM <b>CoCreateInstance</b> method. If group policy does not allow creation of this object, <b>CoCreateInstance</b> will return <b>HRESULT_FROM_WIN32
(ERROR_ACCESS_DISABLED_BY_POLICY)</b>.


#### Examples

The following example code creates an instance of the sensor manager. 


```cpp
// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}

```

## -see-also

<a href="/windows/desktop/SensorsAPI/windows-sensors-com-interfaces">COM Interfaces</a>