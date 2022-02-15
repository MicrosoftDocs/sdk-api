---
UID: NE:d3d11.D3D11_STENCIL_OP
title: D3D11_STENCIL_OP (d3d11.h)
description: The stencil operations that can be performed during depth-stencil testing.
helpviewer_keywords: ["040086f5-0f64-f459-6184-d4091d98d3d4","D3D11_STENCIL_OP","D3D11_STENCIL_OP enumeration [Direct3D 11]","D3D11_STENCIL_OP_DECR","D3D11_STENCIL_OP_DECR_SAT","D3D11_STENCIL_OP_INCR","D3D11_STENCIL_OP_INCR_SAT","D3D11_STENCIL_OP_INVERT","D3D11_STENCIL_OP_KEEP","D3D11_STENCIL_OP_REPLACE","D3D11_STENCIL_OP_ZERO","d3d11/D3D11_STENCIL_OP","d3d11/D3D11_STENCIL_OP_DECR","d3d11/D3D11_STENCIL_OP_DECR_SAT","d3d11/D3D11_STENCIL_OP_INCR","d3d11/D3D11_STENCIL_OP_INCR_SAT","d3d11/D3D11_STENCIL_OP_INVERT","d3d11/D3D11_STENCIL_OP_KEEP","d3d11/D3D11_STENCIL_OP_REPLACE","d3d11/D3D11_STENCIL_OP_ZERO","direct3d11.d3d11_stencil_op"]
old-location: direct3d11\d3d11_stencil_op.htm
tech.root: direct3d11
ms.assetid: 4a08ce69-a3e1-43d3-bf7e-e14b106fbecf
ms.date: 12/05/2018
ms.keywords: 040086f5-0f64-f459-6184-d4091d98d3d4, D3D11_STENCIL_OP, D3D11_STENCIL_OP enumeration [Direct3D 11], D3D11_STENCIL_OP_DECR, D3D11_STENCIL_OP_DECR_SAT, D3D11_STENCIL_OP_INCR, D3D11_STENCIL_OP_INCR_SAT, D3D11_STENCIL_OP_INVERT, D3D11_STENCIL_OP_KEEP, D3D11_STENCIL_OP_REPLACE, D3D11_STENCIL_OP_ZERO, d3d11/D3D11_STENCIL_OP, d3d11/D3D11_STENCIL_OP_DECR, d3d11/D3D11_STENCIL_OP_DECR_SAT, d3d11/D3D11_STENCIL_OP_INCR, d3d11/D3D11_STENCIL_OP_INCR_SAT, d3d11/D3D11_STENCIL_OP_INVERT, d3d11/D3D11_STENCIL_OP_KEEP, d3d11/D3D11_STENCIL_OP_REPLACE, d3d11/D3D11_STENCIL_OP_ZERO, direct3d11.d3d11_stencil_op
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
req.typenames: D3D11_STENCIL_OP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_STENCIL_OP
 - d3d11/D3D11_STENCIL_OP
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
 - D3D11_STENCIL_OP
---

# D3D11_STENCIL_OP enumeration


## -description

The stencil operations that can be performed during depth-stencil testing.

## -enum-fields

### -field D3D11_STENCIL_OP_KEEP:1

Keep the existing stencil data.

### -field D3D11_STENCIL_OP_ZERO:2

Set the stencil data to 0.

### -field D3D11_STENCIL_OP_REPLACE:3

Set the stencil data to the reference value set by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate">ID3D11DeviceContext::OMSetDepthStencilState</a>.

### -field D3D11_STENCIL_OP_INCR_SAT:4

Increment the stencil value by 1, and clamp the result.

### -field D3D11_STENCIL_OP_DECR_SAT:5

Decrement the stencil value by 1, and clamp the result.

### -field D3D11_STENCIL_OP_INVERT:6

Invert the stencil data.

### -field D3D11_STENCIL_OP_INCR:7

Increment the stencil value by 1, and wrap the result if necessary.

### -field D3D11_STENCIL_OP_DECR:8

Decrement the stencil value by 1, and wrap the result if necessary.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
