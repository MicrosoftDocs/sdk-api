---
UID: NE:d3d11_3.D3D11_FENCE_FLAG
title: D3D11_FENCE_FLAG (d3d11_3.h)
description: Specifies fence options.
helpviewer_keywords: ["D3D11_FENCE_FLAG","D3D11_FENCE_FLAG enumeration [Direct3D 11]","D3D11_FENCE_FLAG_NONE","D3D11_FENCE_FLAG_SHARED","D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER","d3d11_3/D3D11_FENCE_FLAG","d3d11_3/D3D11_FENCE_FLAG_NONE","d3d11_3/D3D11_FENCE_FLAG_SHARED","d3d11_3/D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER","direct3d11.d3d11_fence_flag"]
old-location: direct3d11\d3d11_fence_flag.htm
tech.root: direct3d11
ms.assetid: 745B72A2-628C-477E-8534-336E73B5268A
ms.date: 12/05/2018
ms.keywords: D3D11_FENCE_FLAG, D3D11_FENCE_FLAG enumeration [Direct3D 11], D3D11_FENCE_FLAG_NONE, D3D11_FENCE_FLAG_SHARED, D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER, d3d11_3/D3D11_FENCE_FLAG, d3d11_3/D3D11_FENCE_FLAG_NONE, d3d11_3/D3D11_FENCE_FLAG_SHARED, d3d11_3/D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER, direct3d11.d3d11_fence_flag
req.header: d3d11_3.h
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
req.typenames: D3D11_FENCE_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FENCE_FLAG
 - d3d11_3/D3D11_FENCE_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_3.h
api_name:
 - D3D11_FENCE_FLAG
---

# D3D11_FENCE_FLAG enumeration


## -description

Specifies fence options.

## -enum-fields

### -field D3D11_FENCE_FLAG_NONE:0

No options are specified.

### -field D3D11_FENCE_FLAG_SHARED:0x2

The fence is shared.

### -field D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER:0x4

The fence is shared with another GPU adapter.

### -field D3D11_FENCE_FLAG_NON_MONITORED:0x8

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device5-createfence">ID3D11Device::CreateFence</a> method.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
