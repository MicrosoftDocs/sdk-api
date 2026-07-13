---
UID: NF:d3d9.IDirect3DDevice9.CreateAdditionalSwapChain
title: IDirect3DDevice9::CreateAdditionalSwapChain (d3d9.h)
description: The IDirect3DDevice9::CreateAdditionalSwapChain method (d3d9.h) creates an additional swap chain for rendering multiple views.
helpviewer_keywords: ["CreateAdditionalSwapChain","CreateAdditionalSwapChain method [Direct3D 9]","CreateAdditionalSwapChain method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateAdditionalSwapChain method","IDirect3DDevice9.CreateAdditionalSwapChain","IDirect3DDevice9::CreateAdditionalSwapChain","d3d9helper/IDirect3DDevice9::CreateAdditionalSwapChain","dfcccfc0-344b-6e23-2c24-36b11bf7c90b","direct3d9.idirect3ddevice9__createadditionalswapchain"]
old-location: direct3d9\idirect3ddevice9__createadditionalswapchain.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createadditionalswapchain.htm
ms.date: 08/10/2022
ms.keywords: CreateAdditionalSwapChain, CreateAdditionalSwapChain method [Direct3D 9], CreateAdditionalSwapChain method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateAdditionalSwapChain method, IDirect3DDevice9.CreateAdditionalSwapChain, IDirect3DDevice9::CreateAdditionalSwapChain, d3d9helper/IDirect3DDevice9::CreateAdditionalSwapChain, dfcccfc0-344b-6e23-2c24-36b11bf7c90b, direct3d9.idirect3ddevice9__createadditionalswapchain
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
 - IDirect3DDevice9::CreateAdditionalSwapChain
 - d3d9/IDirect3DDevice9::CreateAdditionalSwapChain
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
 - IDirect3DDevice9.CreateAdditionalSwapChain
---

# IDirect3DDevice9::CreateAdditionalSwapChain


## -description

Creates an additional swap chain for rendering multiple views.

## -parameters

### -param pPresentationParameters [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> structure, containing the presentation parameters for the new swap chain. This value cannot be <b>NULL</b>.

Calling this method changes the value of members of the D3DPRESENT_PARAMETERS structure.

<ul>
<li>If BackBufferCount == 0, calling CreateAdditionalSwapChain will increase it to 1.</li>
<li>If the application is in windowed mode, and if either the BackBufferWidth or the BackBufferHeight == 0, they will be set to the client area width and height of the hwnd.</li>
</ul>

### -param pSwapChain [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a> interface, representing the additional swap chain.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_NOTAVAILABLE, D3DERR_DEVICELOST, D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.

## -remarks

There is always at least one swap chain (the implicit swap chain) for each device because Direct3D 9 has one swap chain as a property of the device. 

Note that any given device can support only one full-screen swap chain.

D3DFMT_UNKNOWN can be specified for the windowed mode back buffer format when calling <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a>, <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-reset">IDirect3DDevice9::Reset</a> and CreateAdditionalSwapChain. This means the application does not have to query the current desktop format before calling CreateDevice for windowed mode. For full-screen mode, the back buffer format must be specified.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/direct3d9/presenting-multiple-views-in-windowed-mode">Presenting Multiple Views in Windowed Mode (Direct3D 9)</a>
