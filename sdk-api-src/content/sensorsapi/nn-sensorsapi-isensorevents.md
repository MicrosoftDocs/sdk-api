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

# ISensorEvents interface


## -description


The callback interface you must implement if you want to receive sensor events.

To subscribe to events for a particular sensor, call <a href="https://msdn.microsoft.com/8e2f7edc-894f-4258-8948-2a3d4df532c3">ISensor::SetEventSink</a>.

In addition to the methods inherited from <b>IUnknown</b>, the <b>ISensorEvents</b> interface exposes the following methods.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt725374">COM Interfaces</a>
 

 

