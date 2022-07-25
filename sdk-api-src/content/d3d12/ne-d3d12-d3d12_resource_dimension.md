---
UID: NE:d3d12.D3D12_RESOURCE_DIMENSION
title: D3D12_RESOURCE_DIMENSION (d3d12.h)
description: Identifies the type of resource being used.
helpviewer_keywords: ["D3D12_RESOURCE_DIMENSION","D3D12_RESOURCE_DIMENSION enumeration","D3D12_RESOURCE_DIMENSION_BUFFER","D3D12_RESOURCE_DIMENSION_TEXTURE1D","D3D12_RESOURCE_DIMENSION_TEXTURE2D","D3D12_RESOURCE_DIMENSION_TEXTURE3D","D3D12_RESOURCE_DIMENSION_UNKNOWN","d3d12/D3D12_RESOURCE_DIMENSION","d3d12/D3D12_RESOURCE_DIMENSION_BUFFER","d3d12/D3D12_RESOURCE_DIMENSION_TEXTURE1D","d3d12/D3D12_RESOURCE_DIMENSION_TEXTURE2D","d3d12/D3D12_RESOURCE_DIMENSION_TEXTURE3D","d3d12/D3D12_RESOURCE_DIMENSION_UNKNOWN","direct3d12.d3d12_resource_dimension"]
old-location: direct3d12\d3d12_resource_dimension.htm
tech.root: direct3d12
ms.assetid: E04F3124-01FB-4EE7-BDF8-4821F2F1FCEB
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_DIMENSION, D3D12_RESOURCE_DIMENSION enumeration, D3D12_RESOURCE_DIMENSION_BUFFER, D3D12_RESOURCE_DIMENSION_TEXTURE1D, D3D12_RESOURCE_DIMENSION_TEXTURE2D, D3D12_RESOURCE_DIMENSION_TEXTURE3D, D3D12_RESOURCE_DIMENSION_UNKNOWN, d3d12/D3D12_RESOURCE_DIMENSION, d3d12/D3D12_RESOURCE_DIMENSION_BUFFER, d3d12/D3D12_RESOURCE_DIMENSION_TEXTURE1D, d3d12/D3D12_RESOURCE_DIMENSION_TEXTURE2D, d3d12/D3D12_RESOURCE_DIMENSION_TEXTURE3D, d3d12/D3D12_RESOURCE_DIMENSION_UNKNOWN, direct3d12.d3d12_resource_dimension
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
targetos: Windows
req.typenames: D3D12_RESOURCE_DIMENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOURCE_DIMENSION
 - d3d12/D3D12_RESOURCE_DIMENSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_RESOURCE_DIMENSION
---

# D3D12_RESOURCE_DIMENSION enumeration


## -description

Identifies the type of resource being used.

## -enum-fields

### -field D3D12_RESOURCE_DIMENSION_UNKNOWN:0

Resource is of unknown type.

### -field D3D12_RESOURCE_DIMENSION_BUFFER:1

Resource is a buffer.

### -field D3D12_RESOURCE_DIMENSION_TEXTURE1D:2

Resource is a 1D texture.

### -field D3D12_RESOURCE_DIMENSION_TEXTURE2D:3

Resource is a 2D texture.

### -field D3D12_RESOURCE_DIMENSION_TEXTURE3D:4

Resource is a 3D texture.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc">CD3DX12_RESOURCE_DESC</a>



<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
