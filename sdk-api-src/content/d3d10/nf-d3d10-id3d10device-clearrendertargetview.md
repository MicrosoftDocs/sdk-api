---
UID: NF:d3d10.ID3D10Device.ClearRenderTargetView
title: ID3D10Device::ClearRenderTargetView (d3d10.h)
description: Set all the elements in a render target to one value. (ID3D10Device.ClearRenderTargetView)
helpviewer_keywords: ["3433c2e0-695b-85b1-b1ed-77a71348bc1f","ClearRenderTargetView","ClearRenderTargetView method [Direct3D 10]","ClearRenderTargetView method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","ClearRenderTargetView method","ID3D10Device.ClearRenderTargetView","ID3D10Device::ClearRenderTargetView","d3d10/ID3D10Device::ClearRenderTargetView","direct3d10.id3d10device_clearrendertargetview"]
old-location: direct3d10\id3d10device_clearrendertargetview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_clearrendertargetview.htm
ms.date: 12/05/2018
ms.keywords: 3433c2e0-695b-85b1-b1ed-77a71348bc1f, ClearRenderTargetView, ClearRenderTargetView method [Direct3D 10], ClearRenderTargetView method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],ClearRenderTargetView method, ID3D10Device.ClearRenderTargetView, ID3D10Device::ClearRenderTargetView, d3d10/ID3D10Device::ClearRenderTargetView, direct3d10.id3d10device_clearrendertargetview
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::ClearRenderTargetView
 - d3d10/ID3D10Device::ClearRenderTargetView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.ClearRenderTargetView
---

# ID3D10Device::ClearRenderTargetView


## -description

Set all the elements in a render target to one value.

## -parameters

### -param pRenderTargetView [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rendertargetview">ID3D10RenderTargetView</a>*</b>

Pointer to the render target.

### -param ColorRGBA [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

A 4-component array that represents the color to fill the render target with.

## -remarks

Applications that wish to clear a render target to a specific integer value bit pattern should render a screen-aligned quad instead of using this method.  The reason for this is because this method accepts as input a floating point value, which may not have the same bit pattern as the original integer.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

Unlike Direct3D 9, the full extent of the resource view is always cleared. Viewport and scissor settings are not applied.

</td>
</tr>
</table>
 

When using <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-10level9">10Level9</a>, <b>ClearRenderTargetView</b> only clears the first array slice in the render target view. This can impact (for example) cube map rendering scenarios. Applications should create a render target view for each face or array slice, then clear each view individually.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
