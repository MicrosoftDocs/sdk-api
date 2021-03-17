---
UID: NS:d3d12.D3D12_ROOT_SIGNATURE_DESC1
title: D3D12_ROOT_SIGNATURE_DESC1 (d3d12.h)
description: Describes the layout of a root signature version 1.1.
helpviewer_keywords: ["D3D12_ROOT_SIGNATURE_DESC1","D3D12_ROOT_SIGNATURE_DESC1 structure","d3d12/D3D12_ROOT_SIGNATURE_DESC1","direct3d12.d3d12_root_signature_desc1"]
old-location: direct3d12\d3d12_root_signature_desc1.htm
tech.root: direct3d12
ms.assetid: F085D077-1DA8-41A1-9FA3-4423EA003345
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_SIGNATURE_DESC1, D3D12_ROOT_SIGNATURE_DESC1 structure, d3d12/D3D12_ROOT_SIGNATURE_DESC1, direct3d12.d3d12_root_signature_desc1
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
req.typenames: D3D12_ROOT_SIGNATURE_DESC1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ROOT_SIGNATURE_DESC1
 - d3d12/D3D12_ROOT_SIGNATURE_DESC1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_ROOT_SIGNATURE_DESC1
---

# D3D12_ROOT_SIGNATURE_DESC1 structure


## -description

Describes the layout of a root signature version 1.1.

## -struct-fields

### -field NumParameters

The number of slots in the root signature. This number is also the number of elements in the <i>pParameters</i> array.

### -field pParameters

An array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1">D3D12_ROOT_PARAMETER1</a> structures for the slots in the root signature.

### -field NumStaticSamplers

Specifies the number of static samplers.

### -field pStaticSamplers

Pointer to one or more <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc">D3D12_STATIC_SAMPLER_DESC</a> structures.

### -field Flags

Specifies the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags">D3D12_ROOT_SIGNATURE_FLAGS</a> that determine the data volatility.

## -remarks

Use this structure with the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>