---
UID: NS:d3d11_1.CD3D11_RASTERIZER_DESC1
title: CD3D11_RASTERIZER_DESC1 (d3d11_1.h)
description: The CD3D11_RASTERIZER_DESC1 (d3d11_1.h) structure describes rasterizer state.
helpviewer_keywords: ["CD3D11_RASTERIZER_DESC1","D3D11_RASTERIZER_DESC1","D3D11_RASTERIZER_DESC1 structure [Direct3D 11]","d3d11_1/D3D11_RASTERIZER_DESC1","direct3d11.d3d11_rasterizer_desc1"]
old-location: direct3d11\d3d11_rasterizer_desc1.htm
tech.root: direct3d11
ms.assetid: 7A0E526E-9352-408F-8B11-1B7A9FBC2BE1
ms.date: 08/10/2022
ms.keywords: CD3D11_RASTERIZER_DESC1, D3D11_RASTERIZER_DESC1, D3D11_RASTERIZER_DESC1 structure [Direct3D 11], d3d11_1/D3D11_RASTERIZER_DESC1, direct3d11.d3d11_rasterizer_desc1
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CD3D11_RASTERIZER_DESC1
 - d3d11_1/CD3D11_RASTERIZER_DESC1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_1.h
api_name:
 - D3D11_RASTERIZER_DESC1
---

## -description

<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Describes rasterizer state.

## -struct-fields

## -remarks

AntialiasedLineEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether to enable line antialiasing; only applies if doing line drawing and <b>MultisampleEnable</b> is <b>FALSE</b>. For more info about this member, see Remarks.

CullMode

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_cull_mode">D3D11_CULL_MODE</a></b>

Indicates that triangles facing the specified direction are not drawn.

DepthBias

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Depth value added to a given pixel. For info about depth bias, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage-depth-bias">Depth Bias</a>.

DepthBiasClamp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Maximum depth bias of a pixel. For info about depth bias, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage-depth-bias">Depth Bias</a>.

DepthClipEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether to enable clipping based on distance.

The hardware always performs x and y clipping of rasterized coordinates. When <b>DepthClipEnable</b> is set to the default–<b>TRUE</b>, the hardware also clips the z value (that is, the hardware performs the last step of the following algorithm).


``` syntax

0 < w
-w <= x <= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
-w <= y <= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
0 <= z <= w

```

When you set <b>DepthClipEnable</b> to <b>FALSE</b>, the hardware skips the z clipping (that is, the last step in the preceding algorithm). However, the hardware still performs the "0 &lt; w" clipping. When z clipping is disabled, improper depth ordering at the pixel level might result. However, when z clipping is disabled, stencil shadow implementations are simplified. In other words, you can avoid complex special-case handling for geometry that goes beyond the back clipping plane.

FillMode

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_fill_mode">D3D11_FILL_MODE</a></b>

Determines the fill mode to use when rendering.

ForcedSampleCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The sample count that is forced while UAV rendering or rasterizing. Valid values are 0, 1, 2, 4, 8, and optionally 16. 0 indicates that the sample count is not forced.

<div class="alert"><b>Note</b>  If you want to render with <b>ForcedSampleCount</b> set to 1 or greater, you must follow these guidelines: 

<ul>
<li>Don't bind depth-stencil views.</li>
<li>Disable depth testing.</li>
<li>Ensure the shader doesn't output depth.</li>
<li>If you have any render-target views bound (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_RENDER_TARGET</a>) and <b>ForcedSampleCount</b> is greater than 1, ensure that every render target has only a single sample.</li>
<li>Don't operate the shader at sample frequency. Therefore, <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader">ID3D11ShaderReflection::IsSampleFrequencyShader</a> returns <b>FALSE</b>.</li>
</ul>Otherwise, rendering behavior is undefined. For info about how to configure depth-stencil, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-depth-stencil">Configuring Depth-Stencil Functionality</a>.</div>
<div> </div>

FrontCounterClockwise

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether a triangle is front- or back-facing. If <b>TRUE</b>, a triangle will be considered front-facing if its vertices are counter-clockwise on the render target and considered back-facing if they are clockwise. If <b>FALSE</b>, the opposite is true.

MultisampleEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether to use the quadrilateral or alpha line anti-aliasing algorithm on multisample antialiasing (MSAA) render targets. Set to <b>TRUE</b> to use the quadrilateral line anti-aliasing algorithm and to <b>FALSE</b> to use the alpha line anti-aliasing algorithm. For more info about this member, see Remarks.

ScissorEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether to enable scissor-rectangle culling. All pixels outside an active scissor rectangle are culled.

SlopeScaledDepthBias

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Scalar on a given pixel's slope. For info about depth bias, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage-depth-bias">Depth Bias</a>.

Rasterizer state defines the behavior of the rasterizer stage. To create a rasterizer-state object, call <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1">ID3D11Device1::CreateRasterizerState1</a>. To set rasterizer state, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-rssetstate">ID3D11DeviceContext::RSSetState</a>.

If you do not specify some rasterizer state,  the Direct3D runtime uses the following default values for rasterizer state.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td><b>FillMode</b></td>
<td>Solid</td>
</tr>
<tr>
<td><b>CullMode</b></td>
<td>Back</td>
</tr>
<tr>
<td><b>FrontCounterClockwise</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>DepthBias</b></td>
<td>0</td>
</tr>
<tr>
<td><b>SlopeScaledDepthBias</b></td>
<td>0.0f</td>
</tr>
<tr>
<td><b>DepthBiasClamp</b></td>
<td>0.0f</td>
</tr>
<tr>
<td><b>DepthClipEnable</b></td>
<td><b>TRUE</b></td>
</tr>
<tr>
<td><b>ScissorEnable</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>MultisampleEnable</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>AntialiasedLineEnable</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td><b>ForcedSampleCount</b></td>
<td>0</td>
</tr>
</table>

<div class="alert"><b>Note</b>  For <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature levels</a> 9.1, 9.2, 9.3, and 10.0, if you set <b>MultisampleEnable</b> to <b>FALSE</b>, the runtime renders all points, lines, and triangles without anti-aliasing even for render targets with a sample count greater than 1. For feature levels 10.1 and higher, the setting of <b>MultisampleEnable</b> has no effect on points and triangles with regard to MSAA and impacts only the selection of the line-rendering algorithm as shown in this table:</div>
<div> </div>

<table>
<tr>
<th>Line-rendering algorithm</th>
<th><b>MultisampleEnable</b></th>
<th><b>AntialiasedLineEnable</b></th>
</tr>
<tr>
<td>Aliased</td>
<td><b>FALSE</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>Alpha antialiased</td>
<td><b>FALSE</b></td>
<td><b>TRUE</b></td>
</tr>
<tr>
<td>Quadrilateral</td>
<td><b>TRUE</b></td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>Quadrilateral</td>
<td><b>TRUE</b></td>
<td><b>TRUE</b></td>
</tr>
</table>
 
The settings of the <b>MultisampleEnable</b> and <b>AntialiasedLineEnable</b> members apply only to multisample antialiasing (MSAA) render targets (that is, render targets with sample counts greater than 1). Because of the differences in <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature-level</a> behavior and as long as you aren’t performing any line drawing or don’t mind that lines render as quadrilaterals, we recommend that you always set <b>MultisampleEnable</b> to <b>TRUE</b> whenever you render on MSAA render targets.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>
