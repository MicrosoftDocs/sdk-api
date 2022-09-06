---
UID: NE:d3d10.D3D10_CLEAR_FLAG
title: D3D10_CLEAR_FLAG (d3d10.h)
description: Specifies the parts of the depth stencil to clear. Usually used with ID3D10Device::ClearDepthStencilView.
helpviewer_keywords: ["6f00bddb-2778-cf66-6ca7-e2d2fe7b3c5a","D3D10_CLEAR_DEPTH","D3D10_CLEAR_FLAG","D3D10_CLEAR_FLAG enumeration [Direct3D 10]","D3D10_CLEAR_STENCIL","d3d10/D3D10_CLEAR_DEPTH","d3d10/D3D10_CLEAR_FLAG","d3d10/D3D10_CLEAR_STENCIL","direct3d10.d3d10_clear_flag"]
old-location: direct3d10\d3d10_clear_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_clear_flag.htm
ms.date: 12/05/2018
ms.keywords: 6f00bddb-2778-cf66-6ca7-e2d2fe7b3c5a, D3D10_CLEAR_DEPTH, D3D10_CLEAR_FLAG, D3D10_CLEAR_FLAG enumeration [Direct3D 10], D3D10_CLEAR_STENCIL, d3d10/D3D10_CLEAR_DEPTH, d3d10/D3D10_CLEAR_FLAG, d3d10/D3D10_CLEAR_STENCIL, direct3d10.d3d10_clear_flag
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
req.typenames: D3D10_CLEAR_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_CLEAR_FLAG
 - d3d10/D3D10_CLEAR_FLAG
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
 - D3D10_CLEAR_FLAG
---

# D3D10_CLEAR_FLAG enumeration


## -description

Specifies the parts of the depth stencil to clear. Usually used with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-cleardepthstencilview">ID3D10Device::ClearDepthStencilView</a>.

## -enum-fields

### -field D3D10_CLEAR_DEPTH:0x1L

Clear the depth buffer.

### -field D3D10_CLEAR_STENCIL:0x2L

Clear the stencil buffer.

## -remarks

These flags can be bitwise ORed together.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
