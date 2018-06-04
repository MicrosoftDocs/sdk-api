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

# D3D12_COLOR_WRITE_ENABLE enumeration


## -description


Identifies which components of each pixel of a render target are writable during blending.


## -enum-fields




### -field D3D12_COLOR_WRITE_ENABLE_RED

Allow data to be stored in the red component.


### -field D3D12_COLOR_WRITE_ENABLE_GREEN

Allow data to be stored in the green component.


### -field D3D12_COLOR_WRITE_ENABLE_BLUE

Allow data to be stored in the blue component.


### -field D3D12_COLOR_WRITE_ENABLE_ALPHA

Allow data to be stored in the alpha component.


### -field D3D12_COLOR_WRITE_ENABLE_ALL

Allow data to be stored in all components.


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/911158CF-5F4F-4211-8CC6-F73BDB697BC5">D3D12_RENDER_TARGET_BLEND_DESC</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/D37BB62E-904B-4953-9119-21F3B37570C0">CD3DX12_BLEND_DESC</a>



<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

