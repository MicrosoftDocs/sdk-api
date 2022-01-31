---
UID: NE:d3d11.D3D11_CLEAR_FLAG
title: D3D11_CLEAR_FLAG (d3d11.h)
description: Specifies the parts of the depth stencil to clear.
helpviewer_keywords: ["88ebcd50-b0dd-e04e-4b30-028ca4147553","D3D11_CLEAR_DEPTH","D3D11_CLEAR_FLAG","D3D11_CLEAR_FLAG enumeration [Direct3D 11]","D3D11_CLEAR_STENCIL","d3d11/D3D11_CLEAR_DEPTH","d3d11/D3D11_CLEAR_FLAG","d3d11/D3D11_CLEAR_STENCIL","direct3d11.d3d11_clear_flag"]
old-location: direct3d11\d3d11_clear_flag.htm
tech.root: direct3d11
ms.assetid: 6da515f3-d71d-4b59-b2ea-cacdf78fcb42
ms.date: 12/05/2018
ms.keywords: 88ebcd50-b0dd-e04e-4b30-028ca4147553, D3D11_CLEAR_DEPTH, D3D11_CLEAR_FLAG, D3D11_CLEAR_FLAG enumeration [Direct3D 11], D3D11_CLEAR_STENCIL, d3d11/D3D11_CLEAR_DEPTH, d3d11/D3D11_CLEAR_FLAG, d3d11/D3D11_CLEAR_STENCIL, direct3d11.d3d11_clear_flag
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
req.typenames: D3D11_CLEAR_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_CLEAR_FLAG
 - d3d11/D3D11_CLEAR_FLAG
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
 - D3D11_CLEAR_FLAG
---

# D3D11_CLEAR_FLAG enumeration


## -description

Specifies the parts of the depth stencil to clear.

## -enum-fields

### -field D3D11_CLEAR_DEPTH:0x1L

Clear the depth buffer, using fast clear if possible, then place the resource in a compressed state.

### -field D3D11_CLEAR_STENCIL:0x2L

Clear the stencil buffer, using fast clear if possible, then place the resource in a compressed state.

## -remarks

These flags are used when calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cleardepthstencilview">ID3D11DeviceContext::ClearDepthStencilView</a>; the flags can be combined with a bitwise OR.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
