---
UID: NS:d3d10.D3D10_RASTERIZER_DESC
title: D3D10_RASTERIZER_DESC
author: windows-sdk-content
description: Describes the rasterizer state.
old-location: direct3d10\d3d10_rasterizer_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_rasterizer_desc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10_RASTERIZER_DESC, D3D10_RASTERIZER_DESC structure [Direct3D 10], c7cc2dab-949f-f064-3ae8-72b463253e0d, d3d10/D3D10_RASTERIZER_DESC, direct3d10.d3d10_rasterizer_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_RASTERIZER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_RASTERIZER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_RASTERIZER_DESC structure


## -description


Describes the rasterizer state.


## -struct-fields




### -field FillMode

Type: <b><a href="https://msdn.microsoft.com/9e9c5c9e-0733-4b63-9fc3-8b3a3daf9519">D3D10_FILL_MODE</a></b>

A member of the <a href="https://msdn.microsoft.com/9e9c5c9e-0733-4b63-9fc3-8b3a3daf9519">D3D10_FILL_MODE</a> enumerated type that determines the fill mode to use when rendering.  The default value is <b>D3D10_FILL_SOLID</b>.


### -field CullMode

Type: <b><a href="https://msdn.microsoft.com/b8b70479-e24b-4e60-98f4-9d184e3f1656">D3D10_CULL_MODE</a></b>

A member of the <a href="https://msdn.microsoft.com/b8b70479-e24b-4e60-98f4-9d184e3f1656">D3D10_CULL_MODE</a> enumerated type that indicates whether triangles facing the specified direction are drawn.  The default value is <b>D3D10_CULL_BACK</b>.


### -field FrontCounterClockwise

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Determines if a triangle is front-facing or back-facing. If this parameter is <b>TRUE</b>, then a triangle is considered front-facing if its vertices are counter-clockwise on the render target, and considered back-facing if they are clockwise. If this parameter is <b>FALSE</b>, then the opposite is true.  The default value is <b>FALSE</b>.


### -field DepthBias

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Specifies the depth value added to a given pixel. The default value is 0. For info about depth bias, see <a href="https://msdn.microsoft.com/ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6">Depth Bias</a>.


### -field DepthBiasClamp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Specifies the maximum depth bias of a pixel. The default value is 0.0f. For info about depth bias, see <a href="https://msdn.microsoft.com/ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6">Depth Bias</a>.


### -field SlopeScaledDepthBias

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Specifies a scalar on a given pixel's slope. The default value is 0.0f. For info about depth bias, see <a href="https://msdn.microsoft.com/ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6">Depth Bias</a>.


### -field DepthClipEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Enables or disables clipping based on distance.  The default value is <b>TRUE</b>.

The hardware always performs x and y clipping of rasterized coordinates. When <b>DepthClipEnable</b> is set to the default value, the hardware also clips the z value (that is, the hardware performs the last step of the following algorithm).


<pre class="syntax" xml:space="preserve"><code>
0 &lt; w
-w &lt;= x &lt;= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
-w &lt;= y &lt;= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
0 &lt;= z &lt;= w
</code></pre>
When you set <b>DepthClipEnable</b> to FALSE, the hardware skips the z clipping (that is, the last step in the preceding algorithm). However, the hardware still performs the "0 &lt; w" clipping. When z clipping is disabled, improper depth ordering at the pixel level might result. However, when z clipping is disabled, stencil shadow implementations are simplified. In other words, you can avoid complex special-case handling for geometry that goes beyond the back clipping plane.



### -field ScissorEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Enable or disables scissor-rectangle culling. All pixels outside an active scissor rectangle are culled. The default value is <b>FALSE</b>. For more information, see <a href="https://msdn.microsoft.com/d78c3845-76fd-4bd7-a603-bb1d8c66ac49">Set the Scissor Rectangle</a>.


### -field MultisampleEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to use the quadrilateral or alpha line anti-aliasing algorithm on multisample antialiasing (MSAA) render targets. The default value is <b>FALSE</b>. Set to <b>TRUE</b> to use the quadrilateral line anti-aliasing algorithm and to <b>FALSE</b> to use the alpha line anti-aliasing algorithm. For more info about this member, see Remarks.


### -field AntialiasedLineEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to enable line antialiasing; only applies when alpha blending is enabled, you are drawing lines, and the <b>MultisampleEnable</b> member is <b>FALSE</b>.  The default value is <b>FALSE</b>. For more info about this member, see Remarks.


## -remarks



Rasterizer state defines the behavior of the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a>. To create a rasterizer-state object, call <a href="https://msdn.microsoft.com/bd304e42-e4f6-4bc4-baf0-b4c8287e3351">ID3D10Device::CreateRasterizerState</a>. To set rasterizer state, call <a href="https://msdn.microsoft.com/6b873af4-9724-4a36-bfdd-ea47c667124f">ID3D10Device::RSSetState</a>.

<div class="alert"><b>Note</b>  For <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature levels</a> 9.1, 9.2, 9.3, and 10.0, if you set <b>MultisampleEnable</b> to <b>FALSE</b>, the runtime renders all points, lines, and triangles without anti-aliasing even for render targets with a sample count greater than 1. For feature level 10.1, the setting of <b>MultisampleEnable</b> has no effect on points and triangles with regard to MSAA and impacts only the selection of the line-rendering algorithm as shown in this table:</div>
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
 



The settings of the <b>MultisampleEnable</b> and <b>AntialiasedLineEnable</b> members apply only to multisample antialiasing (MSAA) render targets (that is, render targets with sample counts greater than 1). Because of the differences in <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature-level</a> behavior and as long as you aren’t performing any line drawing or don’t mind that lines render as quadrilaterals, we recommend that you always set <b>MultisampleEnable</b> to <b>TRUE</b> whenever you render on MSAA render targets.




## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

