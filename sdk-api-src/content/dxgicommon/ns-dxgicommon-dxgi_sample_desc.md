---
UID: NS:dxgicommon.DXGI_SAMPLE_DESC
title: DXGI_SAMPLE_DESC (dxgicommon.h)
description: Describes multi-sampling parameters for a resource.
helpviewer_keywords: ["3b41465a-e6b5-e6d1-981e-8fb841dbb6f4","DXGI_SAMPLE_DESC","DXGI_SAMPLE_DESC structure [DXGI]","direct3ddxgi.dxgi_sample_desc","dxgicommon/DXGI_SAMPLE_DESC"]
old-location: direct3ddxgi\dxgi_sample_desc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_sample_desc.htm
ms.date: 12/05/2018
ms.keywords: 3b41465a-e6b5-e6d1-981e-8fb841dbb6f4, DXGI_SAMPLE_DESC, DXGI_SAMPLE_DESC structure [DXGI], direct3ddxgi.dxgi_sample_desc, dxgicommon/DXGI_SAMPLE_DESC
req.header: dxgicommon.h
req.include-header: DXGI.h
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
req.typenames: DXGI_SAMPLE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_SAMPLE_DESC
 - dxgicommon/DXGI_SAMPLE_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgicommon.h
api_name:
 - DXGI_SAMPLE_DESC
---

# DXGI_SAMPLE_DESC structure


## -description

Describes multi-sampling parameters for a resource.

## -struct-fields

### -field Count

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of multisamples per pixel.

### -field Quality

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The image quality level. The higher the quality, the lower the performance. The valid range is between zero and one less than the level returned 
        by <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkmultisamplequalitylevels">ID3D10Device::CheckMultisampleQualityLevels</a> for Direct3D 10 or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkmultisamplequalitylevels">ID3D11Device::CheckMultisampleQualityLevels</a> for Direct3D 11.

For Direct3D 10.1 and Direct3D 11, you can use two special quality level values. For more information about these quality level values, see Remarks.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structure.

The default sampler mode, with no anti-aliasing, has a count of 1 and a quality level of 0.

If multi-sample antialiasing is being used, all bound render targets and depth buffers must have the same sample counts and quality levels.

<table>
<tr>
<td>
Differences between Direct3D 10.0 and Direct3D 10.1 and between Direct3D 10.0 and Direct3D 11:

Direct3D 10.1 has defined two standard quality levels:  
            <b>D3D10_STANDARD_MULTISAMPLE_PATTERN</b> and <b>D3D10_CENTER_MULTISAMPLE_PATTERN</b> in the <b>D3D10_STANDARD_MULTISAMPLE_QUALITY_LEVELS</b> enumeration in D3D10_1.h.

Direct3D 11 has defined two standard quality levels:  
            <b>D3D11_STANDARD_MULTISAMPLE_PATTERN</b> and <b>D3D11_CENTER_MULTISAMPLE_PATTERN</b> in the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_standard_multisample_quality_levels">D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS</a> enumeration in D3D11.h.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>