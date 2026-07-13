---
UID: NF:d3d11.ID3D11Device.CheckMultisampleQualityLevels
title: ID3D11Device::CheckMultisampleQualityLevels (d3d11.h)
description: Get the number of quality levels available during multisampling. (ID3D11Device.CheckMultisampleQualityLevels)
helpviewer_keywords: ["CheckMultisampleQualityLevels","CheckMultisampleQualityLevels method [Direct3D 11]","CheckMultisampleQualityLevels method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CheckMultisampleQualityLevels method","ID3D11Device.CheckMultisampleQualityLevels","ID3D11Device::CheckMultisampleQualityLevels","cc99aa72-2da0-c091-e4b1-047fa6f80bfa","d3d11/ID3D11Device::CheckMultisampleQualityLevels","direct3d11.id3d11device_checkmultisamplequalitylevels"]
old-location: direct3d11\id3d11device_checkmultisamplequalitylevels.htm
tech.root: direct3d11
ms.assetid: 346f5dae-3ce2-4c03-ab17-1c46e18efc64
ms.date: 12/05/2018
ms.keywords: CheckMultisampleQualityLevels, CheckMultisampleQualityLevels method [Direct3D 11], CheckMultisampleQualityLevels method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CheckMultisampleQualityLevels method, ID3D11Device.CheckMultisampleQualityLevels, ID3D11Device::CheckMultisampleQualityLevels, cc99aa72-2da0-c091-e4b1-047fa6f80bfa, d3d11/ID3D11Device::CheckMultisampleQualityLevels, direct3d11.id3d11device_checkmultisamplequalitylevels
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::CheckMultisampleQualityLevels
 - d3d11/ID3D11Device::CheckMultisampleQualityLevels
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CheckMultisampleQualityLevels
---

## -description

Get the number of quality levels available during multisampling.

## -parameters

### -param Format [in]

Type: <b><a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

The texture format. See <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>.

### -param SampleCount [in]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a></b>

The number of samples during multisampling.

### -param pNumQualityLevels [out]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a>*</b>

Number of quality levels supported by the adapter. See **Remarks**.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/win32/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

When multisampling a texture, the number of quality levels available for an adapter is dependent on the texture format used and the number of samples requested. The maximum number of quality levels is defined by **D3D11_MAX_MULTISAMPLE_SAMPLE_COUNT** in `D3D11.h`. If this method returns 0 (S_OK), and the output parameter `pNumQualityLevels` receives a positive value, then the format and sample count combination is supported for the device. When the combination is not supported, this method returns a failure **HRESULT** code (that is, a negative integer), or sets `pNumQualityLevels` output parameter to zero, or both.

Furthermore, the definition of a quality level is left to each hardware vendor to define; however no facility is provided by Direct3D to help discover this information.

Note that FEATURE_LEVEL_10_1 devices are required to support 4x MSAA for all render targets except R32G32B32A32 and R32G32B32. FEATURE_LEVEL_11_0 devices are required to support 4x MSAA for all render target formats, and 8x MSAA for all render target formats except R32G32B32A32 formats.

## -see-also

<a href="/windows/win32/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
