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

# DXGI_RESIDENCY enumeration


## -description


Flags indicating the memory location of a resource.


## -enum-fields




### -field DXGI_RESIDENCY_FULLY_RESIDENT

The resource is located in video memory.


### -field DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY

At least some of the resource is located in CPU memory.


### -field DXGI_RESIDENCY_EVICTED_TO_DISK

At least some of the resource has been paged out to the hard drive.


## -remarks



This enum is used by <a href="https://msdn.microsoft.com/a03af142-657b-459d-abba-fdee72e77db9">QueryResourceResidency</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

