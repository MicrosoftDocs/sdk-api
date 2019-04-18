---
UID: NS:d3d11.D3D11_BLEND_DESC
title: D3D11_BLEND_DESC (d3d11.h)
author: windows-sdk-content
description: Describes the blend state that you use in a call to ID3D11Device::CreateBlendState to create a blend-state object.
old-location: direct3d11\d3d11_blend_desc.htm
tech.root: direct3d11
ms.assetid: 388f862c-58b0-48a8-a865-ba7568484ef5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D11_BLEND_DESC, D3D11_BLEND_DESC structure [Direct3D 11], d3d11/D3D11_BLEND_DESC, direct3d11.d3d11_blend_desc, ed99badb-a124-6d18-9617-fc6a75dc845f
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
 - D3D11_BLEND_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_BLEND_DESC
req.redist: 
ms.custom: 19H1
---

# D3D11_BLEND_DESC structure


## -description


Describes the blend state that you use in a call to <a href="https://msdn.microsoft.com/05b27d72-6ae5-4bab-8906-2d1373ea8d4c">ID3D11Device::CreateBlendState</a> to create a blend-state object.
      


## -struct-fields




### -field AlphaToCoverageEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to use alpha-to-coverage as a multisampling technique when setting a pixel to a render target. For more info about using alpha-to-coverage, see <a href="https://msdn.microsoft.com/en-us/library/Bb205072(v=VS.85).aspx">Alpha-To-Coverage</a>.
          


### -field IndependentBlendEnable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether to enable independent blending in simultaneous render targets.  Set to <b>TRUE</b> to enable independent blending. If set to <b>FALSE</b>, only the RenderTarget[0] members are used; RenderTarget[1..7] are ignored.
          


### -field RenderTarget

Type: <b><a href="https://msdn.microsoft.com/380435e9-e723-4b8b-a0bb-9ff7b4658cdc">D3D11_RENDER_TARGET_BLEND_DESC</a>[8]</b>

An array of <a href="https://msdn.microsoft.com/380435e9-e723-4b8b-a0bb-9ff7b4658cdc">D3D11_RENDER_TARGET_BLEND_DESC</a> structures that describe the blend states for render targets; these correspond to the eight render targets
            that can be bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a> at one time.
          


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
<td>RenderTarget[0].RenderTargetWriteMask</td>
<td>D3D11_COLOR_WRITE_ENABLE_ALL</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  <b>D3D11_BLEND_DESC</b> is identical to <a href="https://msdn.microsoft.com/en-us/library/Bb694528(v=VS.85).aspx">D3D10_BLEND_DESC1</a>.
        </div>
<div> </div>
If the driver type is set to <a href="https://msdn.microsoft.com/ceeec7d6-4bdc-488c-80a8-6c5e11986d6a">D3D_DRIVER_TYPE_HARDWARE</a>, the feature level is set to less than or equal to <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL_9_3</a>, and the pixel format of the render target is set to <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</a>, <b>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</b>, or <b>DXGI_FORMAT_B8G8R8X8_UNORM_SRGB</b>, the display device performs the blend in standard RGB (sRGB) space and not in linear space. However, if the feature level is set to greater than <b>D3D_FEATURE_LEVEL_9_3</b>, the display device performs the blend in linear space, which is ideal.
        




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

