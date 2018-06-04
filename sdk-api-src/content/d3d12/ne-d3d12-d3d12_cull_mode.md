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

# D3D12_CULL_MODE enumeration


## -description


Specifies triangles facing a particular direction are not drawn.


## -enum-fields




### -field D3D12_CULL_MODE_NONE

Always draw all triangles.


### -field D3D12_CULL_MODE_FRONT

Do not draw triangles that are front-facing.


### -field D3D12_CULL_MODE_BACK

Do not draw triangles that are back-facing.


## -remarks




        Cull mode is specified in a <a href="https://msdn.microsoft.com/52ECF841-72BE-44B7-BFB1-305B6981C1F4">D3D12_RASTERIZER_DESC</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/28AA8256-1CAF-484F-B219-0F0461BA947C">CD3DX12_RASTERIZER_DESC</a>



<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

