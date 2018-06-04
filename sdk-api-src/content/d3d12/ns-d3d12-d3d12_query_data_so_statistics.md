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

# D3D12_QUERY_DATA_SO_STATISTICS structure


## -description


Describes query data for stream output.


## -struct-fields




### -field NumPrimitivesWritten

Specifies the number of primitives written.


### -field PrimitivesStorageNeeded

Specifies the total amount of storage needed by the primitives.


## -remarks



Use this structure with <a href="https://msdn.microsoft.com/FDD5F81B-F356-49D9-B6FE-FE2847934E61">D3D12_QUERY_HEAP_TYPE</a> and <a href="https://msdn.microsoft.com/98B238D0-8E4D-46C1-AC2C-09473A972E71">CreateQueryHeap</a>.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

