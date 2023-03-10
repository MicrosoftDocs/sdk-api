---
UID: NF:d3d11.ID3D11DeviceContext.RSSetViewports
title: ID3D11DeviceContext::RSSetViewports (d3d11.h)
description: Bind an array of viewports to the rasterizer stage of the pipeline. (ID3D11DeviceContext.RSSetViewports)
helpviewer_keywords: ["ID3D11DeviceContext interface [Direct3D 11]","RSSetViewports method","ID3D11DeviceContext.RSSetViewports","ID3D11DeviceContext::RSSetViewports","RSSetViewports","RSSetViewports method [Direct3D 11]","RSSetViewports method [Direct3D 11]","ID3D11DeviceContext interface","cdf57cc3-a89c-db1a-5bd9-f1eec144bfe0","d3d11/ID3D11DeviceContext::RSSetViewports","direct3d11.id3d11devicecontext_rssetviewports"]
old-location: direct3d11\id3d11devicecontext_rssetviewports.htm
tech.root: direct3d11
ms.assetid: 7326e9a8-edfa-4e5a-a29e-fe7c54a055f5
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],RSSetViewports method, ID3D11DeviceContext.RSSetViewports, ID3D11DeviceContext::RSSetViewports, RSSetViewports, RSSetViewports method [Direct3D 11], RSSetViewports method [Direct3D 11],ID3D11DeviceContext interface, cdf57cc3-a89c-db1a-5bd9-f1eec144bfe0, d3d11/ID3D11DeviceContext::RSSetViewports, direct3d11.id3d11devicecontext_rssetviewports
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
 - ID3D11DeviceContext::RSSetViewports
 - d3d11/ID3D11DeviceContext::RSSetViewports
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
 - ID3D11DeviceContext.RSSetViewports
---

# ID3D11DeviceContext::RSSetViewports


## -description

Bind an array of viewports to the rasterizer stage of the pipeline.

## -parameters

### -param NumViewports [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of viewports to bind.

### -param pViewports [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_viewport">D3D11_VIEWPORT</a>*</b>

An array of <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_viewport">D3D11_VIEWPORT</a> structures to bind to the device. See the structure page for details about how the viewport size is dependent on the device feature level which has changed between Direct3D 11 and Direct3D 10.

## -remarks

All viewports must be set atomically as one operation. Any viewports not defined by the call are disabled.

Which viewport to use is determined by the <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">SV_ViewportArrayIndex</a> semantic output by a geometry shader; if a geometry shader does not specify the semantic, Direct3D will use the first viewport in the array.

<div class="alert"><b>Note</b>  Even though you specify float values to the members of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_viewport">D3D11_VIEWPORT</a> structure for the <i>pViewports</i> array in a call to  <b>ID3D11DeviceContext::RSSetViewports</b> for <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature levels</a> 9_x, <b>RSSetViewports</b> uses DWORDs internally. Because of this behavior, when you use a negative top left corner for the viewport, the call to  <b>RSSetViewports</b> for feature levels 9_x fails. This failure occurs because <b>RSSetViewports</b> for 9_x casts the floating point values into unsigned integers without validation, which results in integer overflow. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
