---
UID: NS:d3d12.D3D12_RASTERIZER_DESC
title: D3D12_RASTERIZER_DESC
author: windows-sdk-content
description: Describes rasterizer state.
old-location: direct3d12\d3d12_rasterizer_desc.htm
tech.root: direct3d12
ms.assetid: 52ECF841-72BE-44B7-BFB1-305B6981C1F4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12_RASTERIZER_DESC, D3D12_RASTERIZER_DESC structure, d3d12/D3D12_RASTERIZER_DESC, direct3d12.d3d12_rasterizer_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_RASTERIZER_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_RASTERIZER_DESC
req.redist: 
---

# D3D12_RASTERIZER_DESC structure


## -description


Describes rasterizer state.


## -struct-fields




### -field FillMode

A <a href="https://msdn.microsoft.com/5B296AFC-4DAB-48CC-9253-93CACFDC60A8">D3D12_FILL_MODE</a>-typed value that specifies the fill mode to use when rendering.
          


### -field CullMode

A <a href="https://msdn.microsoft.com/C605D9C3-6188-4307-81C0-753D2043EF4E">D3D12_CULL_MODE</a>-typed value that specifies that triangles facing the specified direction are not drawn.
          


### -field FrontCounterClockwise

Determines if a triangle is front- or back-facing. If this member is <b>TRUE</b>, a triangle will be considered front-facing if its vertices are counter-clockwise on the render target and considered back-facing if they are clockwise. If this parameter is <b>FALSE</b>, the opposite is true.
          


### -field DepthBias

Depth value added to a given pixel. For info about depth bias, see <a href="https://msdn.microsoft.com/ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6">Depth Bias</a>.
          


### -field DepthBiasClamp

Maximum depth bias of a pixel. For info about depth bias, see <a href="https://msdn.microsoft.com/ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6">Depth Bias</a>.
          


### -field SlopeScaledDepthBias

Scalar on a given pixel's slope. For info about depth bias, see <a href="https://msdn.microsoft.com/ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6">Depth Bias</a>.
          


### -field DepthClipEnable

Specifies whether to enable clipping based on distance.
            

The hardware always performs x and y clipping of rasterized coordinates. When <b>DepthClipEnable</b> is set to the default–<b>TRUE</b>, the hardware also clips the z value (that is, the hardware performs the last step of the following algorithm).
            

<pre class="syntax" xml:space="preserve"><code>
0 &lt; w
-w &lt;= x &lt;= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
-w &lt;= y &lt;= w (or arbitrarily wider range if implementation uses a guard band to reduce clipping burden)
0 &lt;= z &lt;= w
</code></pre>
When you set <b>DepthClipEnable</b> to <b>FALSE</b>, the hardware skips the z clipping (that is, the last step in the preceding algorithm). However, the hardware still performs the "0 &lt; w" clipping. When z clipping is disabled, improper depth ordering at the pixel level might result. However, when z clipping is disabled, stencil shadow implementations are simplified. In other words, you can avoid complex special-case handling for geometry that goes beyond the back clipping plane.
            


### -field MultisampleEnable

Specifies whether to use the quadrilateral or alpha line anti-aliasing algorithm on multisample antialiasing (MSAA) render targets. Set to <b>TRUE</b> to use the quadrilateral line anti-aliasing algorithm and to <b>FALSE</b> to use the alpha line anti-aliasing algorithm. For more info about this member, see Remarks.
          


### -field AntialiasedLineEnable

Specifies whether to enable line antialiasing; only applies if doing line drawing and <b>MultisampleEnable</b> is <b>FALSE</b>. For more info about this member, see Remarks.
          


### -field ForcedSampleCount

The sample count that is forced while UAV rendering or rasterizing. Valid values are 0, 1, 2, 4, 8, and optionally 16. 0 indicates that the sample count is not forced.
          


### -field ConservativeRaster

A <a href="https://msdn.microsoft.com/E0F033D5-8042-4C39-A35D-C8FE2A95C1D2">D3D12_CONSERVATIVE_RASTERIZATION_MODE</a>-typed value that identifies whether conservative rasterization is on or off.
          


## -remarks



A <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> contains a rasterizer-state structure.
      

Rasterizer state defines the behavior of the rasterizer stage.
        

If you do not specify some rasterizer state,  the Direct3D runtime uses the following default values for rasterizer state.
        

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td><b>FillMode</b></td>
<td>D3D12_FILL_MODE_SOLID</td>
</tr>
<tr>
<td><b>CullMode</b></td>
<td>D3D12_CULL_MODE_BACK</td>
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
<td><b>DepthBiasClamp</b></td>
<td>0.0f</td>
</tr>
<tr>
<td><b>SlopeScaledDepthBias</b></td>
<td>0.0f</td>
</tr>
<tr>
<td><b>DepthClipEnable</b></td>
<td><b>TRUE</b></td>
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
<tr>
<td><b>ConservativeRaster</b></td>
<td><b>D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF</b></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/28AA8256-1CAF-484F-B219-0F0461BA947C">CD3DX12_RASTERIZER_DESC</a>



<a href="https://msdn.microsoft.com/081199AD-1702-4EC8-95AD-B1148C676199">Conservative Rasterization</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/D308BF3E-8CBE-4DF0-B020-4D202E858D99">Rasterizer Ordered Views</a>
 

 

