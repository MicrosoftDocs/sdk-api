---
UID: NS:d3d12.D3D12_VERSIONED_ROOT_SIGNATURE_DESC
title: D3D12_VERSIONED_ROOT_SIGNATURE_DESC (d3d12.h)
description: Holds any version of a root signature description, and is designed to be used with serialization/deserialization functions.
helpviewer_keywords: ["D3D12_VERSIONED_ROOT_SIGNATURE_DESC","D3D12_VERSIONED_ROOT_SIGNATURE_DESC structure","d3d12/D3D12_VERSIONED_ROOT_SIGNATURE_DESC","direct3d12.d3d12_versioned_root_signature_desc"]
old-location: direct3d12\d3d12_versioned_root_signature_desc.htm
tech.root: direct3d12
ms.assetid: 46F692DD-55FF-4DFF-AF11-78CAD10922C1
ms.date: 12/05/2018
ms.keywords: D3D12_VERSIONED_ROOT_SIGNATURE_DESC, D3D12_VERSIONED_ROOT_SIGNATURE_DESC structure, d3d12/D3D12_VERSIONED_ROOT_SIGNATURE_DESC, direct3d12.d3d12_versioned_root_signature_desc
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
req.typenames: D3D12_VERSIONED_ROOT_SIGNATURE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_VERSIONED_ROOT_SIGNATURE_DESC
 - d3d12/D3D12_VERSIONED_ROOT_SIGNATURE_DESC
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
 - D3D12_VERSIONED_ROOT_SIGNATURE_DESC
---

# D3D12_VERSIONED_ROOT_SIGNATURE_DESC structure


## -description

Holds any version of a root signature description, and is designed to be used with serialization/deserialization functions.

## -struct-fields

### -field Version

Specifies one member of D3D_ROOT_SIGNATURE_VERSION that determines the contents of the union.

### -field Desc_1_0

Specifies a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a> (version 1.0).

### -field Desc_1_1

Specifies a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1">D3D12_ROOT_SIGNATURE_DESC1</a> (version 1.1).

## -remarks

Use this structure with the following methods.

<ul>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion">GetRootSignatureDescAtVersion</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc">GetUnconvertedRootSignatureDesc</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature">D3D12SerializeVersionedRootSignature</a>
</li>
</ul>
Refer to the helper structure <a href="/windows/desktop/direct3d12/cd3dx12-versioned-root-signature-desc">CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>