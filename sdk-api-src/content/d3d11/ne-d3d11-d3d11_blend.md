---
UID: NE:d3d11.D3D11_BLEND
title: D3D11_BLEND (d3d11.h)
description: Blend factors, which modulate values for the pixel shader and render target.
helpviewer_keywords: ["0861be4c-0489-4fcd-3850-ea56ac9584c3","D3D11_BLEND","D3D11_BLEND enumeration [Direct3D 11]","D3D11_BLEND_BLEND_FACTOR","D3D11_BLEND_DEST_ALPHA","D3D11_BLEND_DEST_COLOR","D3D11_BLEND_INV_BLEND_FACTOR","D3D11_BLEND_INV_DEST_ALPHA","D3D11_BLEND_INV_DEST_COLOR","D3D11_BLEND_INV_SRC1_ALPHA","D3D11_BLEND_INV_SRC1_COLOR","D3D11_BLEND_INV_SRC_ALPHA","D3D11_BLEND_INV_SRC_COLOR","D3D11_BLEND_ONE","D3D11_BLEND_SRC1_ALPHA","D3D11_BLEND_SRC1_COLOR","D3D11_BLEND_SRC_ALPHA","D3D11_BLEND_SRC_ALPHA_SAT","D3D11_BLEND_SRC_COLOR","D3D11_BLEND_ZERO","d3d11/D3D11_BLEND","d3d11/D3D11_BLEND_BLEND_FACTOR","d3d11/D3D11_BLEND_DEST_ALPHA","d3d11/D3D11_BLEND_DEST_COLOR","d3d11/D3D11_BLEND_INV_BLEND_FACTOR","d3d11/D3D11_BLEND_INV_DEST_ALPHA","d3d11/D3D11_BLEND_INV_DEST_COLOR","d3d11/D3D11_BLEND_INV_SRC1_ALPHA","d3d11/D3D11_BLEND_INV_SRC1_COLOR","d3d11/D3D11_BLEND_INV_SRC_ALPHA","d3d11/D3D11_BLEND_INV_SRC_COLOR","d3d11/D3D11_BLEND_ONE","d3d11/D3D11_BLEND_SRC1_ALPHA","d3d11/D3D11_BLEND_SRC1_COLOR","d3d11/D3D11_BLEND_SRC_ALPHA","d3d11/D3D11_BLEND_SRC_ALPHA_SAT","d3d11/D3D11_BLEND_SRC_COLOR","d3d11/D3D11_BLEND_ZERO","direct3d11.d3d11_blend"]
old-location: direct3d11\d3d11_blend.htm
tech.root: direct3d11
ms.assetid: 5fee5cfc-519e-41d9-93d4-f4f28e1826b8
ms.date: 12/05/2018
ms.keywords: 0861be4c-0489-4fcd-3850-ea56ac9584c3, D3D11_BLEND, D3D11_BLEND enumeration [Direct3D 11], D3D11_BLEND_BLEND_FACTOR, D3D11_BLEND_DEST_ALPHA, D3D11_BLEND_DEST_COLOR, D3D11_BLEND_INV_BLEND_FACTOR, D3D11_BLEND_INV_DEST_ALPHA, D3D11_BLEND_INV_DEST_COLOR, D3D11_BLEND_INV_SRC1_ALPHA, D3D11_BLEND_INV_SRC1_COLOR, D3D11_BLEND_INV_SRC_ALPHA, D3D11_BLEND_INV_SRC_COLOR, D3D11_BLEND_ONE, D3D11_BLEND_SRC1_ALPHA, D3D11_BLEND_SRC1_COLOR, D3D11_BLEND_SRC_ALPHA, D3D11_BLEND_SRC_ALPHA_SAT, D3D11_BLEND_SRC_COLOR, D3D11_BLEND_ZERO, d3d11/D3D11_BLEND, d3d11/D3D11_BLEND_BLEND_FACTOR, d3d11/D3D11_BLEND_DEST_ALPHA, d3d11/D3D11_BLEND_DEST_COLOR, d3d11/D3D11_BLEND_INV_BLEND_FACTOR, d3d11/D3D11_BLEND_INV_DEST_ALPHA, d3d11/D3D11_BLEND_INV_DEST_COLOR, d3d11/D3D11_BLEND_INV_SRC1_ALPHA, d3d11/D3D11_BLEND_INV_SRC1_COLOR, d3d11/D3D11_BLEND_INV_SRC_ALPHA, d3d11/D3D11_BLEND_INV_SRC_COLOR, d3d11/D3D11_BLEND_ONE, d3d11/D3D11_BLEND_SRC1_ALPHA, d3d11/D3D11_BLEND_SRC1_COLOR, d3d11/D3D11_BLEND_SRC_ALPHA, d3d11/D3D11_BLEND_SRC_ALPHA_SAT, d3d11/D3D11_BLEND_SRC_COLOR, d3d11/D3D11_BLEND_ZERO, direct3d11.d3d11_blend
req.header: d3d11.h
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
req.typenames: D3D11_BLEND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_BLEND
 - d3d11/D3D11_BLEND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_BLEND
---

# D3D11_BLEND enumeration


## -description

Blend factors, which modulate values for the pixel shader and render target.

## -enum-fields

### -field D3D11_BLEND_ZERO

The blend factor is (0, 0, 0, 0). No pre-blend operation.

### -field D3D11_BLEND_ONE

The blend factor is (1, 1, 1, 1). No pre-blend operation.

### -field D3D11_BLEND_SRC_COLOR

The blend factor is (Rₛ, Gₛ, Bₛ, Aₛ), that is color data (RGB) from a pixel shader. No pre-blend operation.

### -field D3D11_BLEND_INV_SRC_COLOR

The blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ), that is color data (RGB) from a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB.

### -field D3D11_BLEND_SRC_ALPHA

The blend factor is (Aₛ, Aₛ, Aₛ, Aₛ), that is alpha data (A) from a pixel shader. No pre-blend operation.

### -field D3D11_BLEND_INV_SRC_ALPHA

The blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), that is alpha data (A) from a pixel shader. The pre-blend operation inverts the data, generating 1 - A.

### -field D3D11_BLEND_DEST_ALPHA

The blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>), that is alpha data from a render target. No pre-blend operation.

### -field D3D11_BLEND_INV_DEST_ALPHA

The blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>), that is alpha data from a render target. The pre-blend operation inverts the data, generating 1 - A.

### -field D3D11_BLEND_DEST_COLOR

The blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>), that is color data from a render target. No pre-blend operation.

### -field D3D11_BLEND_INV_DEST_COLOR

The blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>), that is color data from a render target. The pre-blend operation inverts the data, generating 1 - RGB.

### -field D3D11_BLEND_SRC_ALPHA_SAT

The blend factor is (f, f, f, 1); where f = min(Aₛ, 1
    - A<sub>d</sub>). The pre-blend operation clamps the data to 1 or less.

### -field D3D11_BLEND_BLEND_FACTOR

The blend factor is the blend factor set with <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetblendstate">ID3D11DeviceContext::OMSetBlendState</a>. No pre-blend operation.

### -field D3D11_BLEND_INV_BLEND_FACTOR

The blend factor is the blend factor set with <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetblendstate">ID3D11DeviceContext::OMSetBlendState</a>. The pre-blend operation inverts the blend factor, generating 1 - blend_factor.

### -field D3D11_BLEND_SRC1_COLOR

The blend factor is data sources both as color data output by a pixel shader. There is no pre-blend operation. This blend factor supports dual-source color blending.

### -field D3D11_BLEND_INV_SRC1_COLOR

The blend factor is data sources both as color data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - RGB. This blend factor supports dual-source color blending.

### -field D3D11_BLEND_SRC1_ALPHA

The blend factor is data sources as alpha data output by a pixel shader. There is no pre-blend operation. This blend factor supports dual-source color blending.

### -field D3D11_BLEND_INV_SRC1_ALPHA

The blend factor is data sources as alpha data output by a pixel shader. The pre-blend operation inverts the data, generating 1 - A. This blend factor supports dual-source color blending.

## -remarks

Blend operations are specified in a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_blend_desc">blend description</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>