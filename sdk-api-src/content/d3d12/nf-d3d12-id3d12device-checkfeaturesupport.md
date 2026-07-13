---
UID: NF:d3d12.ID3D12Device.CheckFeatureSupport
title: ID3D12Device::CheckFeatureSupport (d3d12.h)
description: Gets information about the features that are supported by the current graphics driver. (ID3D12Device.CheckFeatureSupport)
helpviewer_keywords: ["CheckFeatureSupport","CheckFeatureSupport method","CheckFeatureSupport method","ID3D12Device interface","ID3D12Device interface","CheckFeatureSupport method","ID3D12Device.CheckFeatureSupport","ID3D12Device::CheckFeatureSupport","d3d12/ID3D12Device::CheckFeatureSupport","direct3d12.id3d12device_checkfeaturesupport"]
old-location: direct3d12\id3d12device_checkfeaturesupport.htm
tech.root: direct3d12
ms.assetid: 2E986E37-30C7-45FE-BC8B-A6DD5670938F
ms.date: 12/05/2018
ms.keywords: CheckFeatureSupport, CheckFeatureSupport method, CheckFeatureSupport method,ID3D12Device interface, ID3D12Device interface,CheckFeatureSupport method, ID3D12Device.CheckFeatureSupport, ID3D12Device::CheckFeatureSupport, d3d12/ID3D12Device::CheckFeatureSupport, direct3d12.id3d12device_checkfeaturesupport
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::CheckFeatureSupport
 - d3d12/ID3D12Device::CheckFeatureSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CheckFeatureSupport
---

# ID3D12Device::CheckFeatureSupport


## -description

Gets information about the features that are supported by the current graphics driver.

## -parameters

### -param Feature

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a></b>

A constant from the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a> enumeration describing the feature(s) that you want to query for support.

### -param pFeatureSupportData [in, out]

Type: <b>void*</b>

A pointer to a data structure that corresponds to the value of the <i>Feature</i> parameter. To determine the corresponding data structure for each constant, see <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>.

### -param FeatureSupportDataSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of the structure pointed to by the <i>pFeatureSupportData</i> parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> if successful. Returns <b>E_INVALIDARG</b> if an unsupported data type is passed to the <i>pFeatureSupportData</i> parameter or if a size mismatch is detected for the <i>FeatureSupportDataSize</i> parameter.

## -remarks

As a usage example, to check for ray tracing support, specify the <a href="../d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5.md">D3D12_FEATURE_DATA_D3D12_OPTIONS5</a> structure in the <i>pFeatureSupportData</i> parameter. When the function completes successfully, access the <i>RaytracingTier</i> field (which specifies the supported ray tracing tier) of the now-populated <b>D3D12_FEATURE_DATA_D3D12_OPTIONS5</b> structure.

For more info, see <a href="/windows/desktop/direct3d12/capability-querying">Capability Querying</a>.

<h3><a id="Hardware_support_for_DXGI_Formats"></a><a id="hardware_support_for_dxgi_formats"></a><a id="HARDWARE_SUPPORT_FOR_DXGI_FORMATS"></a>Hardware support for DXGI Formats</h3>
To view tables of DXGI formats and hardware features, refer to:

<ul>
<li>
<a href="/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats">DXGI Format  Support for Direct3D Feature Level 12.1 Hardware</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats">DXGI Format  Support for Direct3D Feature Level 12.0 Hardware</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware">DXGI Format  Support for Direct3D Feature Level 11.1 Hardware</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware">DXGI Format  Support for Direct3D Feature Level 11.0 Hardware</a>
</li>
<li>
<a href="/previous-versions/ff471324(v=vs.85)">Hardware Support for Direct3D 10Level9 Formats</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/format-support-for-direct3d-feature-level-10-1-hardware">Format Support for Direct3D Feature Level 10.1 Hardware</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/format-support-for-direct3d-feature-level-10-0-hardware">Format Support for Direct3D Feature Level 10.0 Hardware</a>
</li>
</ul>

#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D1211on12</a> sample uses <b>ID3D12Device::CheckFeatureSupport</b> as follows:
        


```cpp
inline UINT8 D3D12GetFormatPlaneCount(
    _In_ ID3D12Device* pDevice,
    DXGI_FORMAT Format
    )
{
    D3D12_FEATURE_DATA_FORMAT_INFO formatInfo = {Format};
    if (FAILED(pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_INFO, &formatInfo, sizeof(formatInfo))))
    {
        return 0;
    }
    return formatInfo.PlaneCount;
}

```

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
