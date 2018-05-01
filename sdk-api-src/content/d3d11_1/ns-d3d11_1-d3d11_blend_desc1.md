---
UID: NS:d3d11_1.D3D11_BLEND_DESC1
title: D3D11_BLEND_DESC1
author: windows-driver-content
description: Describes the blend state that you use in a call to ID3D11Device1::CreateBlendState1 to create a blend-state object.
old-location: direct3d11\d3d11_blend_desc1.htm
old-project: direct3d11
ms.assetid: BBBECB86-B33D-4AA3-8D0A-45AEC3BBC4AB
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: CD3D11_BLEND_DESC1, D3D11_BLEND_DESC1, D3D11_BLEND_DESC1 structure [Direct3D 11], d3d11_1/D3D11_BLEND_DESC1, direct3d11.d3d11_blend_desc1
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D11_BLEND_DESC1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11_1.h
api_name:
-	D3D11_BLEND_DESC1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_BLEND_DESC1 structure


## -description


<div class="alert"><b>Note</b>  
        This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.
      </div><div> </div>
        Describes the blend state that you use in a call to <a href="https://msdn.microsoft.com/2E891104-3706-46A5-88FB-C621C95B4EFB">ID3D11Device1::CreateBlendState1</a> to create a blend-state object.
      


## -struct-fields




#### - AlphaToCoverageEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>


            Specifies whether to use alpha-to-coverage as a multisampling technique when setting a pixel to a render target. 
            For more info about using alpha-to-coverage, see <a href="d3d10_graphics_programming_guide_blend_state.htm">Alpha-To-Coverage</a>.
          


#### - IndependentBlendEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>


            Specifies whether to enable independent blending in simultaneous render targets.  Set to <b>TRUE</b> to enable independent blending. If set to <b>FALSE</b>, only the <b>RenderTarget</b>[0] members are used; <b>RenderTarget</b>[1..7] are ignored.
          


#### - RenderTarget

Type: <b><a href="https://msdn.microsoft.com/A8323E69-F385-4E91-8B1F-A7CD3D508A09">D3D11_RENDER_TARGET_BLEND_DESC1</a>[8]</b>


            An array of <a href="https://msdn.microsoft.com/A8323E69-F385-4E91-8B1F-A7CD3D508A09">D3D11_RENDER_TARGET_BLEND_DESC1</a> structures that describe the blend states for render targets; these correspond to the eight render targets
            that can be bound to the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a> at one time.
          


## -remarks




          Here are the default values for blend state.
        

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
<td>RenderTarget[0].LogicOpEnable</td>
<td><b>FALSE</b></td>
</tr>
<tr>
<td>RenderTarget[0].SrcBlend</td>
<td>D3D11_BLEND_ONE</td>
</tr>
<tr>
<td>RenderTarget[0].DestBlend</td>
<td>D3D11_BLEND_ZERO</td>
</tr>
<tr>
<td>RenderTarget[0].BlendOp</td>
<td>D3D11_BLEND_OP_ADD</td>
</tr>
<tr>
<td>RenderTarget[0].SrcBlendAlpha</td>
<td>D3D11_BLEND_ONE</td>
</tr>
<tr>
<td>RenderTarget[0].DestBlendAlpha</td>
<td>D3D11_BLEND_ZERO</td>
</tr>
<tr>
<td>RenderTarget[0].BlendOpAlpha</td>
<td>D3D11_BLEND_OP_ADD</td>
</tr>
<tr>
<td>RenderTarget[0].LogicOp</td>
<td>D3D11_LOGIC_OP_NOOP</td>
</tr>
<tr>
<td>RenderTarget[0].RenderTargetWriteMask</td>
<td>D3D11_COLOR_WRITE_ENABLE_ALL</td>
</tr>
</table>
 


          If the driver type is set to <a href="https://msdn.microsoft.com/ceeec7d6-4bdc-488c-80a8-6c5e11986d6a">D3D_DRIVER_TYPE_HARDWARE</a>, the feature level is set to less than or equal to <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL_9_3</a>, and the pixel format of the render target is set to <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</a>, <b>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</b>, or <b>DXGI_FORMAT_B8G8R8X8_UNORM_SRGB</b>, the display device performs the blend in standard RGB (sRGB) space and not in linear space. However, if the feature level is set to greater than <b>D3D_FEATURE_LEVEL_9_3</b>, the display device performs the blend in linear space, which is ideal.
        


          When you set the <b>LogicOpEnable</b> member of the first element of the <b>RenderTarget</b> array (<b>RenderTarget</b>[0]) to <b>TRUE</b>, you must also set the <b>BlendEnable</b> member of  <b>RenderTarget</b>[0] to <b>FALSE</b>, and the <b>IndependentBlendEnable</b> member of  this <b>D3D11_BLEND_DESC1</b> to <b>FALSE</b>.  This reflects the limitation in hardware that you can't mix logic operations with blending across multiple render targets, and that when you use a logic operation, you must apply the same logic operation to all render targets.
        




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>



<a href="https://msdn.microsoft.com/A8323E69-F385-4E91-8B1F-A7CD3D508A09">D3D11_RENDER_TARGET_BLEND_DESC1</a>



<a href="https://msdn.microsoft.com/BD256EB6-2FDD-4BBA-99E7-D7AA2CBDD629">ID3D11BlendState1::GetDesc1</a>
 

 

