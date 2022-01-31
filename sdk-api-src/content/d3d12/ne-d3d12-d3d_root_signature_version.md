---
UID: NE:d3d12.D3D_ROOT_SIGNATURE_VERSION
title: D3D_ROOT_SIGNATURE_VERSION (d3d12.h)
description: Specifies the version of root signature layout.
helpviewer_keywords: ["D3D_ROOT_SIGNATURE_VERSION","D3D_ROOT_SIGNATURE_VERSION enumeration","D3D_ROOT_SIGNATURE_VERSION_1","D3D_ROOT_SIGNATURE_VERSION_1_0","D3D_ROOT_SIGNATURE_VERSION_1_1","d3d12/D3D_ROOT_SIGNATURE_VERSION","d3d12/D3D_ROOT_SIGNATURE_VERSION_1","d3d12/D3D_ROOT_SIGNATURE_VERSION_1_0","d3d12/D3D_ROOT_SIGNATURE_VERSION_1_1","direct3d12.d3d_root_signature_version"]
old-location: direct3d12\d3d_root_signature_version.htm
tech.root: direct3d12
ms.assetid: 44A22509-5CAE-4C4E-ADC6-E86B5BD8CE3B
ms.date: 12/05/2018
ms.keywords: D3D_ROOT_SIGNATURE_VERSION, D3D_ROOT_SIGNATURE_VERSION enumeration, D3D_ROOT_SIGNATURE_VERSION_1, D3D_ROOT_SIGNATURE_VERSION_1_0, D3D_ROOT_SIGNATURE_VERSION_1_1, d3d12/D3D_ROOT_SIGNATURE_VERSION, d3d12/D3D_ROOT_SIGNATURE_VERSION_1, d3d12/D3D_ROOT_SIGNATURE_VERSION_1_0, d3d12/D3D_ROOT_SIGNATURE_VERSION_1_1, direct3d12.d3d_root_signature_version
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
req.typenames: D3D_ROOT_SIGNATURE_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D_ROOT_SIGNATURE_VERSION
 - d3d12/D3D_ROOT_SIGNATURE_VERSION
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
 - D3D_ROOT_SIGNATURE_VERSION
---

# D3D_ROOT_SIGNATURE_VERSION enumeration


## -description

Specifies the version of root signature layout.

## -enum-fields

### -field D3D_ROOT_SIGNATURE_VERSION_1:0x1

Version one of root signature layout.

### -field D3D_ROOT_SIGNATURE_VERSION_1_0:0x1

Version one of root signature layout.

### -field D3D_ROOT_SIGNATURE_VERSION_1_1:0x2

Version 1.1  of root signature layout. Refer to <a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>.

## -remarks

This enum is used by the following structures and methods.

<ul>
<li>
<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature">D3D12_FEATURE_DATA_ROOT_SIGNATURE</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion">GetRootSignatureDescAtVersion</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature">D3D12SerializeRootSignature</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
