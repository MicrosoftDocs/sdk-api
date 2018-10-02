---
UID: NN:sensorsapi.ISensor
title: ISensor
author: windows-sdk-content
description: Represents a sensor.
old-location: winsensors\isensor.htm
tech.root: SensorsAPI
ms.assetid: 3216afbb-d524-486d-99ad-0ee0cfb884e0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISensor, ISensor interface [WinSensors], ISensor interface [WinSensors],described, sensorsapi/ISensor, winsensors.isensor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensor interface


## -description


Represents a sensor.

You will generally retrieve a pointer to <b>ISensor</b> by calling <a href="https://msdn.microsoft.com/3117a46d-62f2-4d69-97e1-1a75c08a799e">ISensorCollection::GetAt</a> or <a href="https://msdn.microsoft.com/453f46f3-43e1-466d-9f46-165b7d2bcd56">ISensorManager::GetSensorByID</a>, but other methods can retrieve this pointer, too. Various other Sensor API methods use a pointer to <b>ISensor</b> to provide information about a particular sensor or to enable you to specify which sensor to use for a particular action.

In addition to the methods inherited from <b>IUnknown</b>, the <b>ISensor</b> interface exposes the following methods.


## -see-also




<a href="https://msdn.microsoft.com/872de1e9-20f9-409b-9917-24b13a8cc08a">COM Interfaces</a>
 

 

