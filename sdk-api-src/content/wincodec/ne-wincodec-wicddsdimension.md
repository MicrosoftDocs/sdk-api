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

# WICDdsDimension enumeration


## -description


Specifies the dimension type of the data contained in DDS image.


## -enum-fields




### -field WICDdsTexture1D

DDS image contains a 1-dimensional texture .  


### -field WICDdsTexture2D

DDS image contains a 2-dimensional texture .  


### -field WICDdsTexture3D

DDS image contains a 3-dimensional texture .  


### -field WICDdsTextureCube

The DDS image contains a cube texture represented as an array of 6 faces.  


### -field WICDDSTEXTURE_FORCE_DWORD




## -remarks



Both <b>WICDdsTexture2d</b> and <b>WICDdsTextureCube</b> correspond to <a href="https://msdn.microsoft.com/56f138a2-9f2b-4f3b-8619-d9f394704b8a">D3D11_RESOURCE_DIMENSION_TEXTURE2D</a>. When using <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a>, they are distinguished by the flag <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_TEXTURECUBE</a> in the structure <a href="https://msdn.microsoft.com/90c0f877-daf5-4b3d-9846-5bb414c55461">D3D11_TEXTURE2D_DESC</a>.




## -see-also




<a href="https://msdn.microsoft.com/D4EE39D6-54DC-450D-A430-2996D349BEC6">IWICDdsDecoder::GetParameters</a>



<a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>
 

 

