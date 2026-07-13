---
UID: NF:d3d11.ID3D11DeviceContext.OMSetBlendState
title: ID3D11DeviceContext::OMSetBlendState (d3d11.h)
description: Set the blend state of the output-merger stage. (ID3D11DeviceContext.OMSetBlendState)
helpviewer_keywords: ["1f1e71f6-6b9d-3137-ba6e-8c5e5e8079ac","ID3D11DeviceContext interface [Direct3D 11]","OMSetBlendState method","ID3D11DeviceContext.OMSetBlendState","ID3D11DeviceContext::OMSetBlendState","OMSetBlendState","OMSetBlendState method [Direct3D 11]","OMSetBlendState method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::OMSetBlendState","direct3d11.id3d11devicecontext_omsetblendstate"]
old-location: direct3d11\id3d11devicecontext_omsetblendstate.htm
tech.root: direct3d11
ms.assetid: fabcae1d-2ad8-4f4d-8eef-18945e369225
ms.date: 12/05/2018
ms.keywords: 1f1e71f6-6b9d-3137-ba6e-8c5e5e8079ac, ID3D11DeviceContext interface [Direct3D 11],OMSetBlendState method, ID3D11DeviceContext.OMSetBlendState, ID3D11DeviceContext::OMSetBlendState, OMSetBlendState, OMSetBlendState method [Direct3D 11], OMSetBlendState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMSetBlendState, direct3d11.id3d11devicecontext_omsetblendstate
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::OMSetBlendState
 - d3d11/ID3D11DeviceContext::OMSetBlendState
dev_langs:
 - c++
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
---

# ID3D11DeviceContext::OMSetBlendState


## -description

Set the blend state of the output-merger stage.

## -parameters

### -param pBlendState [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>*</b>

Pointer to a blend-state interface (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>). Pass <b>NULL</b> for a default blend state. For more info about default blend state, see Remarks.

### -param BlendFactor [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a>[4]</b>

Array of blend factors, one for each RGBA component. The blend factors modulate values for the pixel shader, render target, or both. If you created  the blend-state object with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_blend">D3D11_BLEND_BLEND_FACTOR</a> or <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_blend">D3D11_BLEND_INV_BLEND_FACTOR</a>, the blending stage uses the non-NULL array of blend factors. If you didn't create the blend-state object with <b>D3D11_BLEND_BLEND_FACTOR</b> or <b>D3D11_BLEND_INV_BLEND_FACTOR</b>, the blending stage does not use the non-NULL array of blend factors; the runtime stores the blend factors, and you can later call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omgetblendstate">ID3D11DeviceContext::OMGetBlendState</a> to retrieve the blend factors. If you pass <b>NULL</b>, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.

### -param SampleMask [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

32-bit sample coverage. The default value is 0xffffffff. See remarks.

## -remarks

Blend state is used by the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a> to determine how to blend together two RGB pixel values and two alpha values. The two RGB pixel values and two alpha values are the RGB pixel value and alpha value that the pixel shader outputs and the RGB pixel value and alpha value already in the output render target. The <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_blend">blend option</a> controls the data source that the blending stage uses to modulate values for the pixel shader, render target, or both. The <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_blend_op">blend operation</a> controls how the blending stage mathematically combines these modulated values.

To create a blend-state interface, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createblendstate">ID3D11Device::CreateBlendState</a>.

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

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
