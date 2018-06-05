---
UID: NS:d3d11_1.D3D11_RASTERIZER_DESC1
title: D3D11_RASTERIZER_DESC1
author: windows-sdk-content
description: Describes rasterizer state.
old-location: direct3d11\d3d11_rasterizer_desc1.htm
old-project: direct3d11
ms.assetid: 7A0E526E-9352-408F-8B11-1B7A9FBC2BE1
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: CD3D11_RASTERIZER_DESC1, D3D11_RASTERIZER_DESC1, D3D11_RASTERIZER_DESC1 structure [Direct3D 11], d3d11_1/D3D11_RASTERIZER_DESC1, direct3d11.d3d11_rasterizer_desc1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3D11_RASTERIZER_DESC1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11_1.h
api_name:
-	D3D11_RASTERIZER_DESC1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_RASTERIZER_DESC1 structure


## -description


<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Describes rasterizer state.


## -struct-fields




#### - FillMode

Type: <b><a href="https://msdn.microsoft.com/853a7df5-4740-40dd-9188-2b399f3aae68">D3D11_FILL_MODE</a></b>

Determines the fill mode to use when rendering.


#### - CullMode

Type: <b><a href="https://msdn.microsoft.com/437c4e2f-f120-44db-b0ce-f4dd4e666814">D3D11_CULL_MODE</a></b>

Indicates that triangles facing the specified direction are not drawn.


#### - FrontCounterClockwise

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether a triangle is front- or back-facing. If <b>TRUE</b>, a triangle will be considered front-facing if its vertices are counter-clockwise on the render target and considered back-facing if they are clockwise. If <b>FALSE</b>, the opposite is true.


#### - DepthBias

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Depth value added to a given pixel. For info about depth bias, see <a href="https://msdn.microsoft.com/library/windows/hardware/jj123786">Depth Bias</a>.


#### - DepthBiasClamp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Maximum depth bias of a pixel. For info about depth bias, see <a href="https://msdn.microsoft.com/library/windows/hardware/jj123786">Depth Bias</a>.


#### - SlopeScaledDepthBias

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Scalar on a given pixel's slope. For info about depth bias, see <a href="https://msdn.microsoft.com/library/windows/hardware/jj123786">Depth Bias</a>.


#### - DepthClipEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to enable clipping based on distance.

The hardware always performs x and y clipping of rasterized coordinates. When <b>DepthClipEnable</b> is set to the default–<b>TRUE</b>, the hardware also clips the z value (that is, the hardware performs the last step of the following algorithm).


<pre class="syntax" xml:space="preserve"><code>
0 &lt; w
-w &lt;= x &lt;= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
-w &lt;= y &lt;= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
0 &lt;= z &lt;= w
</code></pre>
When you set <b>DepthClipEnable</b> to <b>FALSE</b>, the hardware skips the z clipping (that is, the last step in the preceding algorithm). However, the hardware still performs the "0 &lt; w" clipping. When z clipping is disabled, improper depth ordering at the pixel level might result. However, when z clipping is disabled, stencil shadow implementations are simplified. In other words, you can avoid complex special-case handling for geometry that goes beyond the back clipping plane.



#### - ScissorEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to enable scissor-rectangle culling. All pixels outside an active scissor rectangle are culled.


#### - MultisampleEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to use the quadrilateral or alpha line anti-aliasing algorithm on multisample antialiasing (MSAA) render targets. Set to <b>TRUE</b> to use the quadrilateral line anti-aliasing algorithm and to <b>FALSE</b> to use the alpha line anti-aliasing algorithm. For more info about this member, see Remarks.


#### - AntialiasedLineEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to enable line antialiasing; only applies if doing line drawing and <b>MultisampleEnable</b> is <b>FALSE</b>. For more info about this member, see Remarks.


#### - ForcedSampleCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The sample count that is forced while UAV rendering or rasterizing. Valid values are 0, 1, 2, 4, 8, and optionally 16. 0 indicates that the sample count is not forced.

<div class="alert"><b>Note</b>  If you want to render with <b>ForcedSampleCount</b> set to 1 or greater, you must follow these guidelines: 

<ul>
<li>Don't bind depth-stencil views.</li>
<li>Disable depth testing.</li>
<li>Ensure the shader doesn't output depth.</li>
<li>If you have any render-target views bound (<a href="d3d11_bind_flag.htm">D3D11_BIND_RENDER_TARGET</a>) and <b>ForcedSampleCount</b> is greater than 1, ensure that every render target has only a single sample.</li>
<li>Don't operate the shader at sample frequency. Therefore, <a href="https://msdn.microsoft.com/e57cdb67-90b6-4d5d-967b-5de3a9bbaf78">ID3D11ShaderReflection::IsSampleFrequencyShader</a> returns <b>FALSE</b>.</li>
</ul>Otherwise, rendering behavior is undefined. For info about how to configure depth-stencil, see <a href="https://msdn.microsoft.com/e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f">Configuring Depth-Stencil Functionality</a>.</div>
<div> </div>

## -remarks



Rasterizer state defines the behavior of the rasterizer stage. To create a rasterizer-state object, call <a href="https://msdn.microsoft.com/EBA793F1-35AA-4586-9D5C-803BD58B1D95">ID3D11Device1::CreateRasterizerState1</a>. To set rasterizer state, call <a href="https://msdn.microsoft.com/aa76cd3f-5d08-48e7-bd38-ff4d7119eae3">ID3D11DeviceContext::RSSetState</a>.

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
 

<div class="alert"><b>Note</b>  For <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature levels</a> 9.1, 9.2, 9.3, and 10.0, if you set <b>MultisampleEnable</b> to <b>FALSE</b>, the runtime renders all points, lines, and triangles without anti-aliasing even for render targets with a sample count greater than 1. For feature levels 10.1 and higher, the setting of <b>MultisampleEnable</b> has no effect on points and triangles with regard to MSAA and impacts only the selection of the line-rendering algorithm as shown in this table:</div>
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
 



The settings of the <b>MultisampleEnable</b> and <b>AntialiasedLineEnable</b> members apply only to multisample antialiasing (MSAA) render targets (that is, render targets with sample counts greater than 1). Because of the differences in <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature-level</a> behavior and as long as you aren’t performing any line drawing or don’t mind that lines render as quadrilaterals, we recommend that you always set <b>MultisampleEnable</b> to <b>TRUE</b> whenever you render on MSAA render targets.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

