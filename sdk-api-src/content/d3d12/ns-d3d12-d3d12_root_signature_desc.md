---
UID: NS:d3d12.D3D12_ROOT_SIGNATURE_DESC
title: D3D12_ROOT_SIGNATURE_DESC (d3d12.h)
description: Describes the layout of a root signature version 1.0.
helpviewer_keywords: ["D3D12_ROOT_SIGNATURE_DESC","D3D12_ROOT_SIGNATURE_DESC structure","d3d12/D3D12_ROOT_SIGNATURE_DESC","direct3d12.d3d12_root_signature_desc"]
old-location: direct3d12\d3d12_root_signature_desc.htm
tech.root: direct3d12
ms.assetid: D74D9D3B-96AB-489A-A91C-4F68AC3D05EE
ms.date: 12/05/2018
ms.keywords: D3D12_ROOT_SIGNATURE_DESC, D3D12_ROOT_SIGNATURE_DESC structure, d3d12/D3D12_ROOT_SIGNATURE_DESC, direct3d12.d3d12_root_signature_desc
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
req.typenames: D3D12_ROOT_SIGNATURE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ROOT_SIGNATURE_DESC
 - d3d12/D3D12_ROOT_SIGNATURE_DESC
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
 - D3D12_ROOT_SIGNATURE_DESC
---

# D3D12_ROOT_SIGNATURE_DESC structure


## -description

Describes the layout of a root signature version 1.0.

## -struct-fields

### -field NumParameters

The number of slots in the root signature. This number is also the number of elements in the <i>pParameters</i> array.

### -field pParameters

An array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter">D3D12_ROOT_PARAMETER</a> structures for the slots in the root signature.

### -field NumStaticSamplers

Specifies the number of static samplers.

### -field pStaticSamplers

Pointer to one or more <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc">D3D12_STATIC_SAMPLER_DESC</a> structures.

### -field Flags

A combination of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags">D3D12_ROOT_SIGNATURE_FLAGS</a>-typed values that are combined by using a bitwise OR operation.
            The resulting value specifies options for the root signature layout.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature">D3D12SerializeRootSignature</a> function
        and is returned by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12rootsignaturedeserializer-getrootsignaturedesc">ID3D12RootSignatureDeserializer::GetRootSignatureDesc</a> method.
      

There is one graphics root signature, and one compute root signature.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-root-signature-desc">CD3DX12_ROOT_SIGNATURE_DESC</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/creating-a-root-signature">Creating a Root Signature</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type">D3D12_ROOT_PARAMETER_TYPE</a>



<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1">D3D12_ROOT_SIGNATURE_DESC1</a>



<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a>



<a href="/windows/desktop/direct3d12/using-constants-directly-in-the-root-signature">Using constants directly in the root signature</a>



<a href="/windows/desktop/direct3d12/using-descriptors-directly-in-the-root-signature">Using descriptors directly in the root signature</a>
