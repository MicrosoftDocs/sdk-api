---
UID: NN:sensorsapi.ISensor
title: ISensor (sensorsapi.h)
description: Represents a sensor.
helpviewer_keywords: ["ISensor","ISensor interface [WinSensors]","ISensor interface [WinSensors]","described","sensorsapi/ISensor","winsensors.isensor"]
old-location: winsensors\isensor.htm
tech.root: winsensors
ms.assetid: 3216afbb-d524-486d-99ad-0ee0cfb884e0
ms.date: 09/19/2025
ms.keywords: ISensor, ISensor interface [WinSensors], ISensor interface [WinSensors],described, sensorsapi/ISensor, winsensors.isensor
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
 - ISensor
 - sensorsapi/ISensor
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
 - ISensor
---

# ISensor interface


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Represents a sensor.

You will generally retrieve a pointer to <b>ISensor</b> by calling <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensorcollection-getat">ISensorCollection::GetAt</a> or <a href="/windows/desktop/api/sensorsapi/nf-sensorsapi-isensormanager-getsensorbyid">ISensorManager::GetSensorByID</a>, but other methods can retrieve this pointer, too. Various other Sensor API methods use a pointer to <b>ISensor</b> to provide information about a particular sensor or to enable you to specify which sensor to use for a particular action.

In addition to the methods inherited from <b>IUnknown</b>, the <b>ISensor</b> interface exposes the following methods.

## -see-also

<a href="/windows/desktop/SensorsAPI/windows-sensors-com-interfaces">COM Interfaces</a>