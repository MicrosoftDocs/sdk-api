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

# D3D12_BLEND enumeration


## -description


Specifies blend factors, which modulate values for the pixel shader and render target.


## -enum-fields




### -field D3D12_BLEND_ZERO

The blend factor is (0, 0, 0, 0). No pre-blend operation.


### -field D3D12_BLEND_ONE

The blend factor is (1, 1, 1, 1). No pre-blend operation.


### -field D3D12_BLEND_SRC_COLOR

The blend factor is (Rₛ, Gₛ, Bₛ, Aₛ), that is color data (RGB) from a pixel shader. No pre-blend operation.


### -field D3D12_BLEND_INV_SRC_COLOR

The blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ), that is color data (RGB) from a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB.


### -field D3D12_BLEND_SRC_ALPHA

The blend factor is (Aₛ, Aₛ, Aₛ, Aₛ), that is alpha data (A) from a pixel shader. No pre-blend operation.


### -field D3D12_BLEND_INV_SRC_ALPHA

The blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), that is alpha data (A) from a pixel shader. The pre-blend operation inverts the data, generating 1 - A.


### -field D3D12_BLEND_DEST_ALPHA

The blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>), that is alpha data from a render target. No pre-blend operation.


### -field D3D12_BLEND_INV_DEST_ALPHA

The blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>), that is alpha data from a render target. The pre-blend operation inverts the data, generating 1 - A.


### -field D3D12_BLEND_DEST_COLOR

The blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>), that is color data from a render target. No pre-blend operation.


### -field D3D12_BLEND_INV_DEST_COLOR

The blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>), that is color data from a render target. The pre-blend operation inverts the data, generating 1 - RGB.


### -field D3D12_BLEND_SRC_ALPHA_SAT

The blend factor is (f, f, f, 1); where f = min(Aₛ, 1
    - A<sub>d</sub>). The pre-blend operation clamps the data to 1 or less. 



### -field D3D12_BLEND_BLEND_FACTOR

The blend factor is the blend factor set with <a href="https://msdn.microsoft.com/344FD8B5-7225-4BEC-9D1F-C9CEDFE8C60F">ID3D12GraphicsCommandList::OMSetBlendFactor</a>. No pre-blend operation.


### -field D3D12_BLEND_INV_BLEND_FACTOR

The blend factor is the blend factor set with <a href="https://msdn.microsoft.com/344FD8B5-7225-4BEC-9D1F-C9CEDFE8C60F">ID3D12GraphicsCommandList::OMSetBlendFactor</a>. The pre-blend operation inverts the blend factor, generating 1 - blend_factor.


### -field D3D12_BLEND_SRC1_COLOR

The blend factor is data sources both as color data output by a pixel shader. There is no pre-blend operation. This blend factor supports dual-source color blending.


### -field D3D12_BLEND_INV_SRC1_COLOR

The blend factor is data sources both as color data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB. This blend factor supports dual-source color blending.


### -field D3D12_BLEND_SRC1_ALPHA

The blend factor is data sources as alpha data output by a pixel shader. There is no pre-blend operation. This blend factor supports dual-source color blending.


### -field D3D12_BLEND_INV_SRC1_ALPHA

The blend factor is data sources as alpha data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - A. This blend factor supports dual-source color blending.


## -remarks



Source and destination blend operations are specified in a <a href="https://msdn.microsoft.com/911158CF-5F4F-4211-8CC6-F73BDB697BC5">D3D12_RENDER_TARGET_BLEND_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

