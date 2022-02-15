---
UID: NS:d3d10_1.D3D10_BLEND_DESC1
title: D3D10_BLEND_DESC1 (d3d10_1.h)
description: Describes the blend state for a Direct3D 10.1 device.
helpviewer_keywords: ["4a90d15b-26ee-a91b-b9c6-dc1b5ff0e612","D3D10_BLEND_DESC1","D3D10_BLEND_DESC1 structure [Direct3D 10]","d3d10_1/D3D10_BLEND_DESC1","direct3d10.d3d10_blend_desc1"]
old-location: direct3d10\d3d10_blend_desc1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_blend_desc1.htm
ms.date: 12/05/2018
ms.keywords: 4a90d15b-26ee-a91b-b9c6-dc1b5ff0e612, D3D10_BLEND_DESC1, D3D10_BLEND_DESC1 structure [Direct3D 10], d3d10_1/D3D10_BLEND_DESC1, direct3d10.d3d10_blend_desc1
req.header: d3d10_1.h
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
req.typenames: D3D10_BLEND_DESC1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_BLEND_DESC1
 - d3d10_1/D3D10_BLEND_DESC1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10_1.h
api_name:
 - D3D10_BLEND_DESC1
---

# D3D10_BLEND_DESC1 structure


## -description

Describes the blend state for a Direct3D 10.1 device.

## -struct-fields

### -field AlphaToCoverageEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Determines whether or not to use the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state">alpha-to-coverage</a> multisampling technique when setting a render-target pixel.

### -field IndependentBlendEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Set to <b>TRUE</b> to enable independent blending in simultaneous render targets. If set to <b>FALSE</b>, only the RenderTarget[0] members are used. RenderTarget[1..7] are ignored.

### -field RenderTarget

Type: <b><a href="/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1">D3D10_RENDER_TARGET_BLEND_DESC1</a></b>

An array of render-target-blend descriptions (see <a href="/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1">D3D10_RENDER_TARGET_BLEND_DESC1</a>); these correspond to the eight rendertargets 
        that can be set to the output-merger stage at one time.

## -remarks

To see how blending is done, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">Output-Merger Stage (Direct3D 10)</a>.

These are the default values for the blend description.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>AlphaToCoverageEnable</td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>IndependentBlendEnable</td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>RenderTarget[0].BlendEnable</td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>RenderTarget[0].SrcBlend</td>
<td>D3D10_BLEND_ONE</td>
</tr>
<tr>
<td>RenderTarget[0].DestBlend</td>
<td>D3D10_BLEND_ZERO</td>
</tr>
<tr>
<td>RenderTarget[0].BlendOp</td>
<td>D3D10_BLEND_OP_ADD</td>
</tr>
<tr>
<td>RenderTarget[0].SrcBlendAlpha</td>
<td>D3D10_BLEND_ONE</td>
</tr>
<tr>
<td>RenderTarget[0].DestBlendAlpha</td>
<td>D3D10_BLEND_ZERO</td>
</tr>
<tr>
<td>RenderTarget[0].BlendOpAlpha</td>
<td>D3D10_BLEND_OP_ADD</td>
</tr>
<tr>
<td>RenderTarget[0].RenderTargetWriteMask</td>
<td>D3D10_COLOR_WRITE_ENABLE_ALL</td>
</tr>
</table>
 

This structure requires Windows Vista Service Pack 1.

If the driver type is set to <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE_HARDWARE</a>, the feature level is set to less than or equal to <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL_9_3</a>, and the pixel format of the render target is set to <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</a>, <b>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</b>, or <b>DXGI_FORMAT_B8G8R8X8_UNORM_SRGB</b>, the device performs the blend in standard RGB (sRGB) space and not in linear space. However, if the feature level is set to greater than <b>D3D_FEATURE_LEVEL_9_3</b>, the device performs the blend in linear space.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>