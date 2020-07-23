---
UID: NN:sensorsapi.ISensorManager
title: ISensorManager (sensorsapi.h)
description: Provides methods for discovering and retrieving available sensors and a method to request sensor manager events.
helpviewer_keywords: ["ISensorManager","ISensorManager interface [WinSensors]","ISensorManager interface [WinSensors]","described","sensorsapi/ISensorManager","winsensors.isensormanager"]
old-location: winsensors\isensormanager.htm
tech.root: winsensors
ms.assetid: 313742c9-58a7-4ddd-9582-a6ee276e97d0
ms.date: 12/05/2018
ms.keywords: ISensorManager, ISensorManager interface [WinSensors], ISensorManager interface [WinSensors],described, sensorsapi/ISensorManager, winsensors.isensormanager
f1_keywords:
- sensorsapi/ISensorManager
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sensorsapi.dll
api_name:
- ISensorManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensorManager interface


## -description


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




<a href="https://docs.microsoft.com/windows/desktop/SensorsAPI/windows-sensors-com-interfaces">COM Interfaces</a>
 

 

