---
UID: NS:d3d12.D3D12_FEATURE_DATA_FORMAT_INFO
title: D3D12_FEATURE_DATA_FORMAT_INFO (d3d12.h)
description: Describes a DXGI data format and plane count.
helpviewer_keywords: ["D3D12_FEATURE_DATA_FORMAT_INFO","D3D12_FEATURE_DATA_FORMAT_INFO structure","d3d12/D3D12_FEATURE_DATA_FORMAT_INFO","direct3d12.d3d12_feature_data_format_info"]
old-location: direct3d12\d3d12_feature_data_format_info.htm
tech.root: direct3d12
ms.assetid: 8695994A-CC83-451C-AD1B-65359656F3CC
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_FORMAT_INFO, D3D12_FEATURE_DATA_FORMAT_INFO structure, d3d12/D3D12_FEATURE_DATA_FORMAT_INFO, direct3d12.d3d12_feature_data_format_info
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
req.typenames: D3D12_FEATURE_DATA_FORMAT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_FORMAT_INFO
 - d3d12/D3D12_FEATURE_DATA_FORMAT_INFO
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
 - D3D12_FEATURE_DATA_FORMAT_INFO
---

# D3D12_FEATURE_DATA_FORMAT_INFO structure


## -description

Describes a DXGI data format and plane count.

## -struct-fields

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value for the format to return info about.

### -field PlaneCount

The number of planes to provide information about.

## -remarks

See <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>.


#### Examples


```cpp
inline UINT8 D3D12GetFormatPlaneCount(
    _In_ ID3D12Device* pDevice,
    DXGI_FORMAT Format
    )
{
    D3D12_FEATURE_DATA_FORMAT_INFO formatInfo{ Format };
    if (FAILED(pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_INFO, &formatInfo, sizeof(formatInfo))))
    {
        return 0;
    }
    return formatInfo.PlaneCount;
}

```

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>