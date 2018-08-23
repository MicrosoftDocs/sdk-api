---
UID: NF:d3d10.ID3D10Device.OMSetBlendState
title: ID3D10Device::OMSetBlendState
author: windows-sdk-content
description: Set the blend state of the output-merger stage.
old-location: direct3d10\id3d10device_omsetblendstate.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omsetblendstate.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 9b71ab4c-dc5e-607f-4d02-0f408a6d4f30, ID3D10Device interface [Direct3D 10],OMSetBlendState method, ID3D10Device.OMSetBlendState, ID3D10Device::OMSetBlendState, OMSetBlendState, OMSetBlendState method [Direct3D 10], OMSetBlendState method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OMSetBlendState, direct3d10.id3d10device_omsetblendstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.OMSetBlendState
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::OMSetBlendState


## -description


Set the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">blend state</a> of the output-merger stage.


## -parameters




### -param pBlendState [in]

Type: <b><a href="https://msdn.microsoft.com/fe0186f5-cd8f-478d-9009-a0f82830cd1f">ID3D10BlendState</a>*</b>

Pointer to a blend-state interface (see <a href="https://msdn.microsoft.com/fe0186f5-cd8f-478d-9009-a0f82830cd1f">ID3D10BlendState</a>). Passing in <b>NULL</b> implies a default blend state. See remarks for further details.


### -param BlendFactor




### -param SampleMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

32-bit sample coverage. The default value is 0xffffffff. See remarks.


#### - BlendFactor[4] [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Array of blend factors, one for each RGBA component. The blend factors modulate values for the pixel shader, render target, or both. If you created  the blend-state object with <a href="d3d10_blend.htm">D3D10_BLEND_BLEND_FACTOR</a> or <a href="d3d10_blend.htm">D3D10_BLEND_INV_BLEND_FACTOR</a>, the blending stage uses the non-NULL array of blend factors. If you didn't create the blend-state object with <b>D3D10_BLEND_BLEND_FACTOR</b> or <b>D3D10_BLEND_INV_BLEND_FACTOR</b>, the blending stage does not use the non-NULL array of blend factors; the runtime stores the blend factors, and you can later call <a href="https://msdn.microsoft.com/871429b4-8f4a-43bb-ae55-3b07f8d00f68">ID3D11DeviceContext::OMGetBlendState</a> to retrieve the blend factors. If you pass <b>NULL</b>, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.


## -returns



Returns nothing.




## -remarks



Blend state is used by the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a> to determine how to blend together two RGB pixel values and two alpha values. The two RGB pixel values and two alpha values are the RGB pixel value and alpha value that the pixel shader outputs and the RGB pixel value and alpha value already in the output render target. The <a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">blend option</a> controls the data source that the blending stage uses to modulate values for the pixel shader, render target, or both. The <a href="https://msdn.microsoft.com/2d23109a-4d0e-4001-a693-185a942900c0">blend operation</a> controls how the blending stage mathematically combines these modulated values.

To create a blend-state interface, call <a href="https://msdn.microsoft.com/4a5b000d-769b-4e4c-9c9c-d8fced703812">ID3D10Device::CreateBlendState</a>.

Passing in <b>NULL</b> for the blend-state interface indicates to the runtime to set a default blending state.  The following table indicates the default blending parameters.

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
<td>BlendEnable</td>
<td><b>FALSE</b>[8]</td>
</tr>
<tr>
<td>SrcBlend</td>
<td>D3D10_BLEND_ONE</td>
</tr>
<tr>
<td>DstBlend</td>
<td>D3D10_BLEND_ZERO</td>
</tr>
<tr>
<td>BlendOp</td>
<td>D3D10_BLEND_OP_ADD</td>
</tr>
<tr>
<td>SrcBlendAlpha</td>
<td>D3D10_BLEND_ONE</td>
</tr>
<tr>
<td>DstBlendAlpha</td>
<td>D3D10_BLEND_ZERO</td>
</tr>
<tr>
<td>BlendOpAlpha</td>
<td>D3D10_BLEND_OP_ADD</td>
</tr>
<tr>
<td>RenderTargetWriteMask[8]</td>
<td>D3D10_COLOR_WRITE_ENABLE_ALL[8]</td>
</tr>
</table>
 

A sample mask determines which samples get updated in all the active render targets. The mapping of bits in a sample mask to samples in a multisample render target is the responsibility of an individual application. A sample mask is always applied; it is independent of whether multisampling is enabled, and does not depend on whether an application uses multisample render targets.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

