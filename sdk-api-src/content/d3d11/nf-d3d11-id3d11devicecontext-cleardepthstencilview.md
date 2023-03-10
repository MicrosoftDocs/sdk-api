---
UID: NF:d3d11.ID3D11DeviceContext.ClearDepthStencilView
title: ID3D11DeviceContext::ClearDepthStencilView (d3d11.h)
description: Clears the depth-stencil resource. (ID3D11DeviceContext.ClearDepthStencilView)
helpviewer_keywords: ["ClearDepthStencilView","ClearDepthStencilView method [Direct3D 11]","ClearDepthStencilView method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","ClearDepthStencilView method","ID3D11DeviceContext.ClearDepthStencilView","ID3D11DeviceContext::ClearDepthStencilView","d3d11/ID3D11DeviceContext::ClearDepthStencilView","d4e31518-5c9c-aa0c-b817-a09a4886e3f2","direct3d11.id3d11devicecontext_cleardepthstencilview"]
old-location: direct3d11\id3d11devicecontext_cleardepthstencilview.htm
tech.root: direct3d11
ms.assetid: 1e2269cf-edef-466e-be59-95dc644c7a0c
ms.date: 12/05/2018
ms.keywords: ClearDepthStencilView, ClearDepthStencilView method [Direct3D 11], ClearDepthStencilView method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],ClearDepthStencilView method, ID3D11DeviceContext.ClearDepthStencilView, ID3D11DeviceContext::ClearDepthStencilView, d3d11/ID3D11DeviceContext::ClearDepthStencilView, d4e31518-5c9c-aa0c-b817-a09a4886e3f2, direct3d11.id3d11devicecontext_cleardepthstencilview
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
 - ID3D11DeviceContext::ClearDepthStencilView
 - d3d11/ID3D11DeviceContext::ClearDepthStencilView
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
 - ID3D11DeviceContext.ClearDepthStencilView
---

# ID3D11DeviceContext::ClearDepthStencilView


## -description

Clears the depth-stencil resource.

## -parameters

### -param pDepthStencilView [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview">ID3D11DepthStencilView</a>*</b>

Pointer to the depth stencil to be cleared.

### -param ClearFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Identify the type of data to clear (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_clear_flag">D3D11_CLEAR_FLAG</a>).

### -param Depth [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Clear the depth buffer with this value. This value will be clamped between 0 and 1.

### -param Stencil [in]

Type: <b>UINT8</b>

Clear the stencil buffer with this value.

## -remarks

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 11/10:

Unlike Direct3D 9, the full extent of the resource view is always cleared. Viewport and scissor settings are not applied.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
