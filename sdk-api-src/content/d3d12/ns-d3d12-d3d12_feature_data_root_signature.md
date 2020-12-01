---
UID: NS:d3d12.D3D12_FEATURE_DATA_ROOT_SIGNATURE
title: D3D12_FEATURE_DATA_ROOT_SIGNATURE (d3d12.h)
description: Indicates root signature version support.
helpviewer_keywords: ["D3D12_FEATURE_DATA_ROOT_SIGNATURE","D3D12_FEATURE_DATA_ROOT_SIGNATURE structure","d3d12/D3D12_FEATURE_DATA_ROOT_SIGNATURE","direct3d12.d3d12_feature_data_root_signature"]
old-location: direct3d12\d3d12_feature_data_root_signature.htm
tech.root: direct3d12
ms.assetid: 3CC49B10-18B9-4A10-9013-D8F265FD1A28
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_ROOT_SIGNATURE, D3D12_FEATURE_DATA_ROOT_SIGNATURE structure, d3d12/D3D12_FEATURE_DATA_ROOT_SIGNATURE, direct3d12.d3d12_feature_data_root_signature
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
req.typenames: D3D12_FEATURE_DATA_ROOT_SIGNATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_ROOT_SIGNATURE
 - d3d12/D3D12_FEATURE_DATA_ROOT_SIGNATURE
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
 - D3D12_FEATURE_DATA_ROOT_SIGNATURE
---

# D3D12_FEATURE_DATA_ROOT_SIGNATURE structure


## -description

Indicates root signature version support.

## -struct-fields

### -field HighestVersion

On input, specifies the highest version <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version">D3D_ROOT_SIGNATURE_VERSION</a> to check for. On output specifies the highest version, up to the input version specified, actually available.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>