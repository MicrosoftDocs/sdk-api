---
UID: NS:d3d11.D3D11_RASTERIZER_DESC
title: D3D11_RASTERIZER_DESC
author: windows-sdk-content
description: Describes rasterizer state.
old-location: direct3d11\d3d11_rasterizer_desc.htm
tech.root: direct3d11
ms.assetid: 53252fef-f557-46d1-b6a7-ccc8a059752a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 2dbc005c-d339-7868-c653-8b43d3f9e828, D3D11_RASTERIZER_DESC, D3D11_RASTERIZER_DESC structure [Direct3D 11], d3d11/D3D11_RASTERIZER_DESC, direct3d11.d3d11_rasterizer_desc
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_RASTERIZER_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_RASTERIZER_DESC
req.redist: 
---

# D3D11_RASTERIZER_DESC structure


## -description


Describes rasterizer state.


## -struct-fields




### -field FillMode

Type: <b><a href="https://msdn.microsoft.com/853a7df5-4740-40dd-9188-2b399f3aae68">D3D11_FILL_MODE</a></b>

Determines the fill mode to use when rendering (see <a href="https://msdn.microsoft.com/853a7df5-4740-40dd-9188-2b399f3aae68">D3D11_FILL_MODE</a>).


### -field CullMode

Type: <b><a href="https://msdn.microsoft.com/437c4e2f-f120-44db-b0ce-f4dd4e666814">D3D11_CULL_MODE</a></b>

Indicates triangles facing the specified direction are not drawn (see <a href="https://msdn.microsoft.com/437c4e2f-f120-44db-b0ce-f4dd4e666814">D3D11_CULL_MODE</a>).


### -field FrontCounterClockwise

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Determines if a triangle is front- or back-facing. If this parameter is <b>TRUE</b>, a triangle will be considered front-facing if its vertices are counter-clockwise on the render target and considered back-facing if they are clockwise. If this parameter is <b>FALSE</b>, the opposite is true.


### -field DepthBias

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Depth value added to a given pixel. For info about depth bias, see <a href="https://msdn.microsoft.com/en-us/library/Cc308048(v=VS.85).aspx">Depth Bias</a>.


### -field DepthBiasClamp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Maximum depth bias of a pixel. For info about depth bias, see <a href="https://msdn.microsoft.com/en-us/library/Cc308048(v=VS.85).aspx">Depth Bias</a>.


### -field SlopeScaledDepthBias

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Scalar on a given pixel's slope. For info about depth bias, see <a href="https://msdn.microsoft.com/en-us/library/Cc308048(v=VS.85).aspx">Depth Bias</a>.


### -field DepthClipEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Enable clipping based on distance.

The hardware always performs x and y clipping of rasterized coordinates. When <b>DepthClipEnable</b> is set to the default–<b>TRUE</b>, the hardware also clips the z value (that is, the hardware performs the last step of the following algorithm).


<pre class="syntax" xml:space="preserve"><code>
0 &lt; w
-w &lt;= x &lt;= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
-w &lt;= y &lt;= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
0 &lt;= z &lt;= w
</code></pre>
When you set <b>DepthClipEnable</b> to <b>FALSE</b>, the hardware skips the z clipping (that is, the last step in the preceding algorithm). However, the hardware still performs the "0 &lt; w" clipping. When z clipping is disabled, improper depth ordering at the pixel level might result. However, when z clipping is disabled, stencil shadow implementations are simplified. In other words, you can avoid complex special-case handling for geometry that goes beyond the back clipping plane.



### -field ScissorEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Enable scissor-rectangle culling. All pixels outside an active scissor rectangle are culled.


### -field MultisampleEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to use the quadrilateral or alpha line anti-aliasing algorithm on multisample antialiasing (MSAA) render targets. Set to <b>TRUE</b> to use the quadrilateral line anti-aliasing algorithm and to <b>FALSE</b> to use the alpha line anti-aliasing algorithm. For more info about this member, see Remarks.


### -field AntialiasedLineEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to enable line antialiasing; only applies if doing line drawing and <b>MultisampleEnable</b> is <b>FALSE</b>. For more info about this member, see Remarks.


## -remarks



Rasterizer state defines the behavior of the rasterizer stage. To create a rasterizer-state object, call <a href="https://msdn.microsoft.com/b49a8dbb-2280-4d5d-ae65-58cde2e9ed10">ID3D11Device::CreateRasterizerState</a>. To set rasterizer state, call <a href="https://msdn.microsoft.com/aa76cd3f-5d08-48e7-bd38-ff4d7119eae3">ID3D11DeviceContext::RSSetState</a>.

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
</table>
 

<div class="alert"><b>Note</b>  For <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature levels</a> 9.1, 9.2, 9.3, and 10.0, if you set <b>MultisampleEnable</b> to <b>FALSE</b>, the runtime renders all points, lines, and triangles without anti-aliasing even for render targets with a sample count greater than 1. For feature levels 10.1 and higher, the setting of <b>MultisampleEnable</b> has no effect on points and triangles with regard to MSAA and impacts only the selection of the line-rendering algorithm as shown in this table:</div>
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
 



The settings of the <b>MultisampleEnable</b> and <b>AntialiasedLineEnable</b> members apply only to multisample antialiasing (MSAA) render targets (that is, render targets with sample counts greater than 1). Because of the differences in <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature-level</a> behavior and as long as you aren’t performing any line drawing or don’t mind that lines render as quadrilaterals, we recommend that you always set <b>MultisampleEnable</b> to <b>TRUE</b> whenever you render on MSAA render targets.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

