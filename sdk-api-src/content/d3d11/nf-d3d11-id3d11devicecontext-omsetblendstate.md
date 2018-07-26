---
UID: NF:d3d11.ID3D11DeviceContext.OMSetBlendState
title: ID3D11DeviceContext::OMSetBlendState
author: windows-sdk-content
description: Set the blend state of the output-merger stage.
old-location: direct3d11\id3d11devicecontext_omsetblendstate.htm
old-project: direct3d11
ms.assetid: fabcae1d-2ad8-4f4d-8eef-18945e369225
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 1f1e71f6-6b9d-3137-ba6e-8c5e5e8079ac, ID3D11DeviceContext interface [Direct3D 11],OMSetBlendState method, ID3D11DeviceContext.OMSetBlendState, ID3D11DeviceContext::OMSetBlendState, OMSetBlendState, OMSetBlendState method [Direct3D 11], OMSetBlendState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMSetBlendState, direct3d11.id3d11devicecontext_omsetblendstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.OMSetBlendState
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::OMSetBlendState


## -description


Set the blend state of the output-merger stage.


## -parameters




### -param pBlendState [in, optional]

Type: <b><a href="https://msdn.microsoft.com/ccb39c89-eba7-473c-8358-dc3513da4be7">ID3D11BlendState</a>*</b>

Pointer to a blend-state interface (see <a href="https://msdn.microsoft.com/ccb39c89-eba7-473c-8358-dc3513da4be7">ID3D11BlendState</a>). Pass <b>NULL</b> for a default blend state. For more info about default blend state, see Remarks.


### -param BlendFactor [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a>[4]</b>

Array of blend factors, one for each RGBA component. The blend factors modulate values for the pixel shader, render target, or both. If you created  the blend-state object with <a href="https://msdn.microsoft.com/library/Ff476086(v=VS.85).aspx">D3D11_BLEND_BLEND_FACTOR</a> or <a href="https://msdn.microsoft.com/library/Ff476086(v=VS.85).aspx">D3D11_BLEND_INV_BLEND_FACTOR</a>, the blending stage uses the non-NULL array of blend factors. If you didn't create the blend-state object with <b>D3D11_BLEND_BLEND_FACTOR</b> or <b>D3D11_BLEND_INV_BLEND_FACTOR</b>, the blending stage does not use the non-NULL array of blend factors; the runtime stores the blend factors, and you can later call <a href="https://msdn.microsoft.com/871429b4-8f4a-43bb-ae55-3b07f8d00f68">ID3D11DeviceContext::OMGetBlendState</a> to retrieve the blend factors. If you pass <b>NULL</b>, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.


### -param SampleMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

32-bit sample coverage. The default value is 0xffffffff. See remarks.


## -returns



Returns nothing.




## -remarks



Blend state is used by the <a href="https://msdn.microsoft.com/library/Bb205120(v=VS.85).aspx">output-merger stage</a> to determine how to blend together two RGB pixel values and two alpha values. The two RGB pixel values and two alpha values are the RGB pixel value and alpha value that the pixel shader outputs and the RGB pixel value and alpha value already in the output render target. The <a href="https://msdn.microsoft.com/5fee5cfc-519e-41d9-93d4-f4f28e1826b8">blend option</a> controls the data source that the blending stage uses to modulate values for the pixel shader, render target, or both. The <a href="https://msdn.microsoft.com/e0a201da-0d5d-4a85-a0cb-fddd9bd2f460">blend operation</a> controls how the blending stage mathematically combines these modulated values.

To create a blend-state interface, call <a href="https://msdn.microsoft.com/05b27d72-6ae5-4bab-8906-2d1373ea8d4c">ID3D11Device::CreateBlendState</a>.

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
 

A sample mask determines which samples get updated in all the active render targets. The mapping of bits in a sample mask to samples in a multisample render target is the responsibility of an individual application. A sample mask is always applied; it is independent of whether multisampling is enabled, and does not depend on whether an application uses multisample render targets.

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

