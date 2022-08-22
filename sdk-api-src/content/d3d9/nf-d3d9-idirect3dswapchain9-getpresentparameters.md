---
UID: NF:d3d9.IDirect3DSwapChain9.GetPresentParameters
title: IDirect3DSwapChain9::GetPresentParameters (d3d9.h)
description: The IDirect3DSwapChain9::GetPresentParameters (d3d9.h) method retrieves the presentation parameters associated with a swap chain.
helpviewer_keywords: ["GetPresentParameters","GetPresentParameters method [Direct3D 9]","GetPresentParameters method [Direct3D 9]","IDirect3DSwapChain9 interface","IDirect3DSwapChain9 interface [Direct3D 9]","GetPresentParameters method","IDirect3DSwapChain9.GetPresentParameters","IDirect3DSwapChain9::GetPresentParameters","ac85b9e4-b5da-4efa-cb76-254ef41c07cb","d3d9helper/IDirect3DSwapChain9::GetPresentParameters","direct3d9.idirect3dswapchain9__getpresentparameters"]
old-location: direct3d9\idirect3dswapchain9__getpresentparameters.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9__getpresentparameters.htm
ms.date: 08/11/2022
ms.keywords: GetPresentParameters, GetPresentParameters method [Direct3D 9], GetPresentParameters method [Direct3D 9],IDirect3DSwapChain9 interface, IDirect3DSwapChain9 interface [Direct3D 9],GetPresentParameters method, IDirect3DSwapChain9.GetPresentParameters, IDirect3DSwapChain9::GetPresentParameters, ac85b9e4-b5da-4efa-cb76-254ef41c07cb, d3d9helper/IDirect3DSwapChain9::GetPresentParameters, direct3d9.idirect3dswapchain9__getpresentparameters
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DSwapChain9::GetPresentParameters
 - d3d9/IDirect3DSwapChain9::GetPresentParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DSwapChain9.GetPresentParameters
---

# IDirect3DSwapChain9::GetPresentParameters


## -description

Retrieves the presentation parameters associated with a swap chain.

## -parameters

### -param pPresentationParameters [out, retval]

Type: <b><a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to the presentation parameters. See <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

This method can be used to see the presentation parameters of the parent swap chain of a surface (a back buffer, for instance). The parent swap chain can be retrieved with <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getcontainer">IDirect3DSurface9::GetContainer</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a>
