---
UID: NN:sensorsapi.ISensorCollection
title: ISensorCollection (sensorsapi.h)
description: Represents a collection of sensors, such as all the sensors connected to a computer.
helpviewer_keywords: ["ISensorCollection","ISensorCollection interface [WinSensors]","ISensorCollection interface [WinSensors]","described","sensorsapi/ISensorCollection","winsensors.isensorcollection"]
old-location: winsensors\isensorcollection.htm
tech.root: winsensors
ms.assetid: 54d8572a-40a2-49d0-a8bf-2161b63eee42
ms.date: 09/19/2025
ms.keywords: ISensorCollection, ISensorCollection interface [WinSensors], ISensorCollection interface [WinSensors],described, sensorsapi/ISensorCollection, winsensors.isensorcollection
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
 - ISensorCollection
 - sensorsapi/ISensorCollection
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
 - ISensorCollection
---

# ISensorCollection interface


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Represents a collection of sensors, such as all the sensors connected to a computer.

Retrieve a pointer to <b>ISensorCollection</b> by calling methods of the <a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager">ISensorManager</a> interface.
In addition to the methods inherited from <b>IUnknown</b>, the <b>ISensorCollection</b> interface exposes the following methods.

## -see-also

<a href="/windows/desktop/SensorsAPI/windows-sensors-com-interfaces">COM Interfaces</a>