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

# D3D11_COUNTER enumeration


## -description


Options for performance counters.


## -enum-fields




### -field D3D11_COUNTER_DEVICE_DEPENDENT_0

Define a performance counter that is dependent on the hardware device.


## -remarks



Independent hardware vendors may define their own set of performance counters for their devices, by giving the enumeration value a number that is greater than the value for D3D11_COUNTER_DEVICE_DEPENDENT_0.

This enumeration is used by <a href="https://msdn.microsoft.com/a0816409-fbe1-4b45-9b69-6f85b20008cb">D3D11_COUNTER_DESC</a> and <a href="https://msdn.microsoft.com/64730e19-1a9e-4494-a3aa-314fd72281e1">D3D11_COUNTER_INFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

