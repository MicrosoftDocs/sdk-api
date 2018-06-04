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

# D3D12_RANGE_UINT64 structure


## -description


Describes a memory range in a 64-bit address space.


## -struct-fields




### -field Begin

The offset, in bytes, denoting the beginning of a memory range.


### -field End

The offset, in bytes, denoting the end of a memory range.
            <b>End</b> is one-past-the-end.


## -remarks



<b>End</b> is one-past-the-end.
        When <b>Begin</b> equals <b>End</b>, the range is empty.
        The size of the range is (<b>End</b> - <b>Begin</b>).
      


        This structure is used by the <a href="https://msdn.microsoft.com/D8DACE22-9AFD-4DCD-A254-A34AD532ACD7">D3D12_SUBRESOURCE_RANGE_UINT64</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

