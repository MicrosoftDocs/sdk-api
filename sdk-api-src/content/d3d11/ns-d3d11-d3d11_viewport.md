---
UID: NS:d3d11.D3D11_VIEWPORT
title: D3D11_VIEWPORT (d3d11.h)
description: Defines the dimensions of a viewport. (D3D11_VIEWPORT)
helpviewer_keywords: ["D3D11_VIEWPORT","D3D11_VIEWPORT structure [Direct3D 11]","d3d11/D3D11_VIEWPORT","direct3d11.d3d11_viewport","e40eb7eb-7ea6-54bc-b846-b83c9856e3fe"]
old-location: direct3d11\d3d11_viewport.htm
tech.root: direct3d11
ms.assetid: 7ef29e40-4b42-4794-83b6-44581c0d529f
ms.date: 12/05/2018
ms.keywords: D3D11_VIEWPORT, D3D11_VIEWPORT structure [Direct3D 11], d3d11/D3D11_VIEWPORT, direct3d11.d3d11_viewport, e40eb7eb-7ea6-54bc-b846-b83c9856e3fe
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_VIEWPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIEWPORT
 - d3d11/D3D11_VIEWPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_VIEWPORT
---

# D3D11_VIEWPORT structure


## -description

Defines the dimensions of a viewport.

## -struct-fields

### -field TopLeftX

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

X position of the left hand side of the viewport. Ranges between D3D11_VIEWPORT_BOUNDS_MIN and D3D11_VIEWPORT_BOUNDS_MAX.

### -field TopLeftY

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Y position of the top of the viewport. Ranges between D3D11_VIEWPORT_BOUNDS_MIN and D3D11_VIEWPORT_BOUNDS_MAX.

### -field Width

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Width of the viewport.

### -field Height

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Height of the viewport.

### -field MinDepth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Minimum depth of the viewport. Ranges between 0 and 1.

### -field MaxDepth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Maximum depth of the viewport. Ranges between 0 and 1.

## -remarks

In all cases, <b>Width</b> and <b>Height</b> must be &gt;= 0 and <b>TopLeftX</b> + <b>Width</b> and <b>TopLeftY</b> + <b>Height</b> must be &lt;= D3D11_VIEWPORT_BOUNDS_MAX.

<table>
<tr>
<td>
Viewport Sizes and Feature Level Support Differences between Direct3D 11 and Direct3D 10:

The range for the minimum and maximum viewport size is dependent on the feature level defined by <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>.

<ul>
<li>Direct3D 11 supports fractional viewports; the parameter types are  floating-point numbers. The feature level, D3D_FEATURE_LEVEL_11_0, supports (D3D11_VIEWPORT_BOUNDS_MIN, D3D11_VIEWPORT_BOUNDS_MAX) values between (-32768, 32,767).</li>
<li>Direct3D 10 does not support fractional viewports. The feature levels, D3D_FEATURE_LEVEL_10_1 (or below), supports (D3D10_VIEWPORT_BOUNDS_MIN, D3D10_VIEWPORT_BOUNDS_MAX) values between (-16384, 16383).</li>
</ul>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Even though you specify float values to the members of the <b>D3D11_VIEWPORT</b> structure for the <i>pViewports</i> array in a call to  <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetviewports">ID3D11DeviceContext::RSSetViewports</a> for <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature levels</a> 9_x, <b>RSSetViewports</b> uses DWORDs internally. Because of this behavior, when you use a negative top left corner for the viewport, the call to  <b>RSSetViewports</b> for feature levels 9_x fails. This failure occurs because <b>RSSetViewports</b> for 9_x casts the floating point values into unsigned integers without validation, which results in integer overflow. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>
