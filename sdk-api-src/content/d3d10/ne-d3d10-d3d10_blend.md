---
UID: NE:d3d10.D3D10_BLEND
title: D3D10_BLEND (d3d10.h)
author: windows-sdk-content
description: Blend options. A blend option identifies the data source and an optional pre-blend operation.
old-location: direct3d10\d3d10_blend.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_blend.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 8864d9f9-c1b1-93ad-93b2-7e0e590a562d, D3D10_BLEND, D3D10_BLEND enumeration [Direct3D 10], D3D10_BLEND_BLEND_FACTOR, D3D10_BLEND_DEST_ALPHA, D3D10_BLEND_DEST_COLOR, D3D10_BLEND_INV_BLEND_FACTOR, D3D10_BLEND_INV_DEST_ALPHA, D3D10_BLEND_INV_DEST_COLOR, D3D10_BLEND_INV_SRC1_ALPHA, D3D10_BLEND_INV_SRC1_COLOR, D3D10_BLEND_INV_SRC_ALPHA, D3D10_BLEND_INV_SRC_COLOR, D3D10_BLEND_ONE, D3D10_BLEND_SRC1_ALPHA, D3D10_BLEND_SRC1_COLOR, D3D10_BLEND_SRC_ALPHA, D3D10_BLEND_SRC_ALPHA_SAT, D3D10_BLEND_SRC_COLOR, D3D10_BLEND_ZERO, d3d10/D3D10_BLEND, d3d10/D3D10_BLEND_BLEND_FACTOR, d3d10/D3D10_BLEND_DEST_ALPHA, d3d10/D3D10_BLEND_DEST_COLOR, d3d10/D3D10_BLEND_INV_BLEND_FACTOR, d3d10/D3D10_BLEND_INV_DEST_ALPHA, d3d10/D3D10_BLEND_INV_DEST_COLOR, d3d10/D3D10_BLEND_INV_SRC1_ALPHA, d3d10/D3D10_BLEND_INV_SRC1_COLOR, d3d10/D3D10_BLEND_INV_SRC_ALPHA, d3d10/D3D10_BLEND_INV_SRC_COLOR, d3d10/D3D10_BLEND_ONE, d3d10/D3D10_BLEND_SRC1_ALPHA, d3d10/D3D10_BLEND_SRC1_COLOR, d3d10/D3D10_BLEND_SRC_ALPHA, d3d10/D3D10_BLEND_SRC_ALPHA_SAT, d3d10/D3D10_BLEND_SRC_COLOR, d3d10/D3D10_BLEND_ZERO, direct3d10.d3d10_blend
ms.topic: enum
f1_keywords: 
 - "d3d10/D3D10_BLEND"
req.header: d3d10.h
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
 - D3D10.h
api_name:
 - D3D10_BLEND
targetos: Windows
req.typenames: D3D10_BLEND
req.redist: 
ms.custom: 19H1
---

# D3D10_BLEND enumeration


## -description


Blend options. A blend option identifies the data source and an optional pre-blend operation.


## -enum-fields




### -field D3D10_BLEND_ZERO

The data source is the color black (0, 0, 0, 0). No pre-blend operation.


### -field D3D10_BLEND_ONE

The data source is the color white (1, 1, 1, 1). No pre-blend operation.


### -field D3D10_BLEND_SRC_COLOR

The data source is color data (RGB) from a pixel shader. No pre-blend operation.


### -field D3D10_BLEND_INV_SRC_COLOR

The data source is color data (RGB) from a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB.


### -field D3D10_BLEND_SRC_ALPHA

The data source is alpha data (A) from a pixel shader. No pre-blend operation.


### -field D3D10_BLEND_INV_SRC_ALPHA

The data source is alpha data (A) from a pixel shader. The pre-blend operation inverts the data, generating 1 - A.


### -field D3D10_BLEND_DEST_ALPHA

The data source is alpha data from a rendertarget. No pre-blend operation.


### -field D3D10_BLEND_INV_DEST_ALPHA

The data source is alpha data from a rendertarget. The pre-blend operation inverts the data, generating 1 - A.


### -field D3D10_BLEND_DEST_COLOR

The data source is color data from a rendertarget. No pre-blend operation.


### -field D3D10_BLEND_INV_DEST_COLOR

The data source is color data from a rendertarget. The pre-blend operation inverts the data, generating 1 - RGB.


### -field D3D10_BLEND_SRC_ALPHA_SAT

The data source is alpha data from a pixel shader. The pre-blend operation clamps the data to 1 or less. 



### -field D3D10_BLEND_BLEND_FACTOR

The data source is the blend factor set with <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetblendstate">ID3D10Device::OMSetBlendState</a>. No pre-blend operation.


### -field D3D10_BLEND_INV_BLEND_FACTOR

The data source is the blend factor set with <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetblendstate">ID3D10Device::OMSetBlendState</a>. The pre-blend operation inverts the blend factor, generating 1 - blend_factor.


### -field D3D10_BLEND_SRC1_COLOR

The data sources are both color data output by a pixel shader. There is no pre-blend operation. This options supports <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">dual-source color blending</a>.


### -field D3D10_BLEND_INV_SRC1_COLOR

The data sources are both color data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB. This options supports <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">dual-source color blending</a>.


### -field D3D10_BLEND_SRC1_ALPHA

The data sources are alpha data output by a pixel shader. There is no pre-blend operation. This options supports <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">dual-source color blending</a>.


### -field D3D10_BLEND_INV_SRC1_ALPHA

The data sources are alpha data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - A. This options supports <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">dual-source color blending</a>.


## -remarks



Blend operations are specified in a <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_blend_desc">blend description</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
 

 

