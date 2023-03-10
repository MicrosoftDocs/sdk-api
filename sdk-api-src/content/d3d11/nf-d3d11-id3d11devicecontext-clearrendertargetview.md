---
UID: NF:d3d11.ID3D11DeviceContext.ClearRenderTargetView
title: ID3D11DeviceContext::ClearRenderTargetView (d3d11.h)
description: Set all the elements in a render target to one value. (ID3D11DeviceContext.ClearRenderTargetView)
helpviewer_keywords: ["2d296302-263e-a0b0-10ad-d1afbdf56ebf","ClearRenderTargetView","ClearRenderTargetView method [Direct3D 11]","ClearRenderTargetView method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","ClearRenderTargetView method","ID3D11DeviceContext.ClearRenderTargetView","ID3D11DeviceContext::ClearRenderTargetView","d3d11/ID3D11DeviceContext::ClearRenderTargetView","direct3d11.id3d11devicecontext_clearrendertargetview"]
old-location: direct3d11\id3d11devicecontext_clearrendertargetview.htm
tech.root: direct3d11
ms.assetid: bbc6d3fb-b64f-47b0-9feb-a248dce0bf4b
ms.date: 12/05/2018
ms.keywords: 2d296302-263e-a0b0-10ad-d1afbdf56ebf, ClearRenderTargetView, ClearRenderTargetView method [Direct3D 11], ClearRenderTargetView method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],ClearRenderTargetView method, ID3D11DeviceContext.ClearRenderTargetView, ID3D11DeviceContext::ClearRenderTargetView, d3d11/ID3D11DeviceContext::ClearRenderTargetView, direct3d11.id3d11devicecontext_clearrendertargetview
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
 - ID3D11DeviceContext::ClearRenderTargetView
 - d3d11/ID3D11DeviceContext::ClearRenderTargetView
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
 - ID3D11DeviceContext.ClearRenderTargetView
---

# ID3D11DeviceContext::ClearRenderTargetView


## -description

Set all the elements in a render target to one value.

## -parameters

### -param pRenderTargetView [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rendertargetview">ID3D11RenderTargetView</a>*</b>

Pointer to the render target.

### -param ColorRGBA [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a>[4]</b>

A 4-component array that represents the color to fill the render target with.

## -remarks

Applications that wish to clear a render target to a specific integer value bit pattern should render a screen-aligned quad instead of using this method.  The reason for this is because this method accepts as input a floating point value, which may not have the same bit pattern as the original integer.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 11/10:

Unlike Direct3D 9, the full extent of the resource view is always cleared. Viewport and scissor settings are not applied.

</td>
</tr>
</table>
 

When using <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL_9_x</a>, <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview">ClearRenderTargetView</a> only clears the first array slice in the render target view. This can impact (for example) cube map rendering scenarios. Applications should create a render target view for each face or array slice, then clear each view individually.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
