---
UID: NE:d3d10.D3D10_BLEND
title: D3D10_BLEND (d3d10.h)
description: Blend options. A blend option identifies the data source and an optional pre-blend operation.
helpviewer_keywords: ["8864d9f9-c1b1-93ad-93b2-7e0e590a562d","D3D10_BLEND","D3D10_BLEND enumeration [Direct3D 10]","D3D10_BLEND_BLEND_FACTOR","D3D10_BLEND_DEST_ALPHA","D3D10_BLEND_DEST_COLOR","D3D10_BLEND_INV_BLEND_FACTOR","D3D10_BLEND_INV_DEST_ALPHA","D3D10_BLEND_INV_DEST_COLOR","D3D10_BLEND_INV_SRC1_ALPHA","D3D10_BLEND_INV_SRC1_COLOR","D3D10_BLEND_INV_SRC_ALPHA","D3D10_BLEND_INV_SRC_COLOR","D3D10_BLEND_ONE","D3D10_BLEND_SRC1_ALPHA","D3D10_BLEND_SRC1_COLOR","D3D10_BLEND_SRC_ALPHA","D3D10_BLEND_SRC_ALPHA_SAT","D3D10_BLEND_SRC_COLOR","D3D10_BLEND_ZERO","d3d10/D3D10_BLEND","d3d10/D3D10_BLEND_BLEND_FACTOR","d3d10/D3D10_BLEND_DEST_ALPHA","d3d10/D3D10_BLEND_DEST_COLOR","d3d10/D3D10_BLEND_INV_BLEND_FACTOR","d3d10/D3D10_BLEND_INV_DEST_ALPHA","d3d10/D3D10_BLEND_INV_DEST_COLOR","d3d10/D3D10_BLEND_INV_SRC1_ALPHA","d3d10/D3D10_BLEND_INV_SRC1_COLOR","d3d10/D3D10_BLEND_INV_SRC_ALPHA","d3d10/D3D10_BLEND_INV_SRC_COLOR","d3d10/D3D10_BLEND_ONE","d3d10/D3D10_BLEND_SRC1_ALPHA","d3d10/D3D10_BLEND_SRC1_COLOR","d3d10/D3D10_BLEND_SRC_ALPHA","d3d10/D3D10_BLEND_SRC_ALPHA_SAT","d3d10/D3D10_BLEND_SRC_COLOR","d3d10/D3D10_BLEND_ZERO","direct3d10.d3d10_blend"]
old-location: direct3d10\d3d10_blend.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_blend.htm
ms.date: 12/05/2018
ms.keywords: 8864d9f9-c1b1-93ad-93b2-7e0e590a562d, D3D10_BLEND, D3D10_BLEND enumeration [Direct3D 10], D3D10_BLEND_BLEND_FACTOR, D3D10_BLEND_DEST_ALPHA, D3D10_BLEND_DEST_COLOR, D3D10_BLEND_INV_BLEND_FACTOR, D3D10_BLEND_INV_DEST_ALPHA, D3D10_BLEND_INV_DEST_COLOR, D3D10_BLEND_INV_SRC1_ALPHA, D3D10_BLEND_INV_SRC1_COLOR, D3D10_BLEND_INV_SRC_ALPHA, D3D10_BLEND_INV_SRC_COLOR, D3D10_BLEND_ONE, D3D10_BLEND_SRC1_ALPHA, D3D10_BLEND_SRC1_COLOR, D3D10_BLEND_SRC_ALPHA, D3D10_BLEND_SRC_ALPHA_SAT, D3D10_BLEND_SRC_COLOR, D3D10_BLEND_ZERO, d3d10/D3D10_BLEND, d3d10/D3D10_BLEND_BLEND_FACTOR, d3d10/D3D10_BLEND_DEST_ALPHA, d3d10/D3D10_BLEND_DEST_COLOR, d3d10/D3D10_BLEND_INV_BLEND_FACTOR, d3d10/D3D10_BLEND_INV_DEST_ALPHA, d3d10/D3D10_BLEND_INV_DEST_COLOR, d3d10/D3D10_BLEND_INV_SRC1_ALPHA, d3d10/D3D10_BLEND_INV_SRC1_COLOR, d3d10/D3D10_BLEND_INV_SRC_ALPHA, d3d10/D3D10_BLEND_INV_SRC_COLOR, d3d10/D3D10_BLEND_ONE, d3d10/D3D10_BLEND_SRC1_ALPHA, d3d10/D3D10_BLEND_SRC1_COLOR, d3d10/D3D10_BLEND_SRC_ALPHA, d3d10/D3D10_BLEND_SRC_ALPHA_SAT, d3d10/D3D10_BLEND_SRC_COLOR, d3d10/D3D10_BLEND_ZERO, direct3d10.d3d10_blend
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
targetos: Windows
req.typenames: D3D10_BLEND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_BLEND
 - d3d10/D3D10_BLEND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_BLEND
---

# D3D10_BLEND enumeration


## -description

Blend options. A blend option identifies the data source and an optional pre-blend operation.

## -enum-fields

### -field D3D10_BLEND_ZERO:1

The data source is the color black (0, 0, 0, 0). No pre-blend operation.

### -field D3D10_BLEND_ONE:2

The data source is the color white (1, 1, 1, 1). No pre-blend operation.

### -field D3D10_BLEND_SRC_COLOR:3

The data source is color data (RGB) from a pixel shader. No pre-blend operation.

### -field D3D10_BLEND_INV_SRC_COLOR:4

The data source is color data (RGB) from a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB.

### -field D3D10_BLEND_SRC_ALPHA:5

The data source is alpha data (A) from a pixel shader. No pre-blend operation.

### -field D3D10_BLEND_INV_SRC_ALPHA:6

The data source is alpha data (A) from a pixel shader. The pre-blend operation inverts the data, generating 1 - A.

### -field D3D10_BLEND_DEST_ALPHA:7

The data source is alpha data from a rendertarget. No pre-blend operation.

### -field D3D10_BLEND_INV_DEST_ALPHA:8

The data source is alpha data from a rendertarget. The pre-blend operation inverts the data, generating 1 - A.

### -field D3D10_BLEND_DEST_COLOR:9

The data source is color data from a rendertarget. No pre-blend operation.

### -field D3D10_BLEND_INV_DEST_COLOR:10

The data source is color data from a rendertarget. The pre-blend operation inverts the data, generating 1 - RGB.

### -field D3D10_BLEND_SRC_ALPHA_SAT:11

The data source is alpha data from a pixel shader. The pre-blend operation clamps the data to 1 or less.

### -field D3D10_BLEND_BLEND_FACTOR:14

The data source is the blend factor set with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetblendstate">ID3D10Device::OMSetBlendState</a>. No pre-blend operation.

### -field D3D10_BLEND_INV_BLEND_FACTOR:15

The data source is the blend factor set with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetblendstate">ID3D10Device::OMSetBlendState</a>. The pre-blend operation inverts the blend factor, generating 1 - blend_factor.

### -field D3D10_BLEND_SRC1_COLOR:16

The data sources are both color data output by a pixel shader. There is no pre-blend operation. This options supports <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">dual-source color blending</a>.

### -field D3D10_BLEND_INV_SRC1_COLOR:17

The data sources are both color data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB. This options supports <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">dual-source color blending</a>.

### -field D3D10_BLEND_SRC1_ALPHA:18

The data sources are alpha data output by a pixel shader. There is no pre-blend operation. This options supports <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">dual-source color blending</a>.

### -field D3D10_BLEND_INV_SRC1_ALPHA:19

The data sources are alpha data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - A. This options supports <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">dual-source color blending</a>.

## -remarks

Blend operations are specified in a <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_blend_desc">blend description</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
