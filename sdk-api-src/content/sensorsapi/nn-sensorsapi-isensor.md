---
UID: NN:sensorsapi.ISensor
title: ISensor (sensorsapi.h)
description: Represents a sensor.
old-location: winsensors\isensor.htm
tech.root: SensorsAPI
ms.assetid: 3216afbb-d524-486d-99ad-0ee0cfb884e0
ms.date: 12/05/2018
ms.keywords: ISensor, ISensor interface [WinSensors], ISensor interface [WinSensors],described, sensorsapi/ISensor, winsensors.isensor
f1_keywords:
- sensorsapi/ISensor
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
- ISensor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensor interface


## -description


Represents a sensor.

You will generally retrieve a pointer to <b>ISensor</b> by calling <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nf-sensorsapi-isensorcollection-getat">ISensorCollection::GetAt</a> or <a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nf-sensorsapi-isensormanager-getsensorbyid">ISensorManager::GetSensorByID</a>, but other methods can retrieve this pointer, too. Various other Sensor API methods use a pointer to <b>ISensor</b> to provide information about a particular sensor or to enable you to specify which sensor to use for a particular action.

In addition to the methods inherited from <b>IUnknown</b>, the <b>ISensor</b> interface exposes the following methods.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SensorsAPI/windows-sensors-com-interfaces">COM Interfaces</a>
 

 

