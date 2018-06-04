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

# DXGI_MEMORY_SEGMENT_GROUP enumeration


## -description


Specifies the memory segment group to use.


## -enum-fields




### -field DXGI_MEMORY_SEGMENT_GROUP_LOCAL

              The grouping of segments which is considered local to the video adapter, and represents the fastest available memory to the GPU. Applications should target the local segment group as the target size for their working set.


### -field DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL

The grouping of segments which is considered non-local to the video adapter, and may have slower performance than the local segment group.


## -remarks



This enum is used by <a href="https://msdn.microsoft.com/A2F95FE5-CF8D-4F17-8CC8-62AAA40B71FC">QueryVideoMemoryInfo</a> and <a href="https://msdn.microsoft.com/5D17F57F-9FFA-4B5C-98B6-33E5B3982A63">SetVideoMemoryReservation</a>.

Refer to the remarks for <a href="https://msdn.microsoft.com/EFA3FF00-F121-4ED8-AF83-1952C73AE06D">D3D12_MEMORY_POOL</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

