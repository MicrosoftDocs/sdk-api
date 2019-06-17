---
UID: NE:d3d12.D3D12_BLEND
title: D3D12_BLEND (d3d12.h)
author: windows-sdk-content
description: Specifies blend factors, which modulate values for the pixel shader and render target.
old-location: direct3d12\d3d12_blend.htm
tech.root: direct3d12
ms.assetid: BA114E1C-0E0B-4260-ACED-0FF3D426C764
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_BLEND, D3D12_BLEND enumeration, D3D12_BLEND_BLEND_FACTOR, D3D12_BLEND_DEST_ALPHA, D3D12_BLEND_DEST_COLOR, D3D12_BLEND_INV_BLEND_FACTOR, D3D12_BLEND_INV_DEST_ALPHA, D3D12_BLEND_INV_DEST_COLOR, D3D12_BLEND_INV_SRC1_ALPHA, D3D12_BLEND_INV_SRC1_COLOR, D3D12_BLEND_INV_SRC_ALPHA, D3D12_BLEND_INV_SRC_COLOR, D3D12_BLEND_ONE, D3D12_BLEND_SRC1_ALPHA, D3D12_BLEND_SRC1_COLOR, D3D12_BLEND_SRC_ALPHA, D3D12_BLEND_SRC_ALPHA_SAT, D3D12_BLEND_SRC_COLOR, D3D12_BLEND_ZERO, d3d12/D3D12_BLEND, d3d12/D3D12_BLEND_BLEND_FACTOR, d3d12/D3D12_BLEND_DEST_ALPHA, d3d12/D3D12_BLEND_DEST_COLOR, d3d12/D3D12_BLEND_INV_BLEND_FACTOR, d3d12/D3D12_BLEND_INV_DEST_ALPHA, d3d12/D3D12_BLEND_INV_DEST_COLOR, d3d12/D3D12_BLEND_INV_SRC1_ALPHA, d3d12/D3D12_BLEND_INV_SRC1_COLOR, d3d12/D3D12_BLEND_INV_SRC_ALPHA, d3d12/D3D12_BLEND_INV_SRC_COLOR, d3d12/D3D12_BLEND_ONE, d3d12/D3D12_BLEND_SRC1_ALPHA, d3d12/D3D12_BLEND_SRC1_COLOR, d3d12/D3D12_BLEND_SRC_ALPHA, d3d12/D3D12_BLEND_SRC_ALPHA_SAT, d3d12/D3D12_BLEND_SRC_COLOR, d3d12/D3D12_BLEND_ZERO, direct3d12.d3d12_blend
ms.topic: enum
f1_keywords: ["d3d12/D3D12_BLEND"]
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_BLEND
product: Windows
targetos: Windows
req.typenames: D3D12_BLEND
req.redist: 
ms.custom: 19H1
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

The blend factor is the blend factor set with <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">ID3D12GraphicsCommandList::OMSetBlendFactor</a>. No pre-blend operation.


### -field D3D12_BLEND_INV_BLEND_FACTOR

The blend factor is the blend factor set with <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">ID3D12GraphicsCommandList::OMSetBlendFactor</a>. The pre-blend operation inverts the blend factor, generating 1 - blend_factor.


### -field D3D12_BLEND_SRC1_COLOR

The blend factor is data sources both as color data output by a pixel shader. There is no pre-blend operation. This blend factor supports dual-source color blending.


### -field D3D12_BLEND_INV_SRC1_COLOR

The blend factor is data sources both as color data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB. This blend factor supports dual-source color blending.


### -field D3D12_BLEND_SRC1_ALPHA

The blend factor is data sources as alpha data output by a pixel shader. There is no pre-blend operation. This blend factor supports dual-source color blending.


### -field D3D12_BLEND_INV_SRC1_ALPHA

The blend factor is data sources as alpha data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - A. This blend factor supports dual-source color blending.


## -remarks



Source and destination blend operations are specified in a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc">D3D12_RENDER_TARGET_BLEND_DESC</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
 

 

