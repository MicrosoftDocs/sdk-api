---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISensor interface


## -description


Represents a sensor.

You will generally retrieve a pointer to <b>ISensor</b> by calling <a href="https://msdn.microsoft.com/3117a46d-62f2-4d69-97e1-1a75c08a799e">ISensorCollection::GetAt</a> or <a href="https://msdn.microsoft.com/453f46f3-43e1-466d-9f46-165b7d2bcd56">ISensorManager::GetSensorByID</a>, but other methods can retrieve this pointer, too. Various other Sensor API methods use a pointer to <b>ISensor</b> to provide information about a particular sensor or to enable you to specify which sensor to use for a particular action.

In addition to the methods inherited from <b>IUnknown</b>, the <b>ISensor</b> interface exposes the following methods.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt725374">COM Interfaces</a>
 

 

