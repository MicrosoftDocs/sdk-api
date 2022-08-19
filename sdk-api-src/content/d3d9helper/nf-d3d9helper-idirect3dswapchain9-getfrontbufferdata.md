---
UID: NF:d3d9helper.IDirect3DSwapChain9.GetFrontBufferData
title: IDirect3DSwapChain9::GetFrontBufferData (d3d9helper.h)
description: The IDirect3DSwapChain9::GetFrontBufferData method (d3d9helper.h) generates a copy of the swapchain's front buffer and places that copy in a system memory buffer provided by the application. 
helpviewer_keywords: ["8f442969-657a-a5ab-1aa3-ff227fe2f705","GetFrontBufferData","GetFrontBufferData method [Direct3D 9]","GetFrontBufferData method [Direct3D 9]","IDirect3DSwapChain9 interface","IDirect3DSwapChain9 interface [Direct3D 9]","GetFrontBufferData method","IDirect3DSwapChain9.GetFrontBufferData","IDirect3DSwapChain9::GetFrontBufferData","d3d9helper/IDirect3DSwapChain9::GetFrontBufferData","direct3d9.idirect3dswapchain9__getfrontbufferdata"]
old-location: direct3d9\idirect3dswapchain9__getfrontbufferdata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9__getfrontbufferdata.htm
ms.date: 08/12/2022
ms.keywords: 8f442969-657a-a5ab-1aa3-ff227fe2f705, GetFrontBufferData, GetFrontBufferData method [Direct3D 9], GetFrontBufferData method [Direct3D 9],IDirect3DSwapChain9 interface, IDirect3DSwapChain9 interface [Direct3D 9],GetFrontBufferData method, IDirect3DSwapChain9.GetFrontBufferData, IDirect3DSwapChain9::GetFrontBufferData, d3d9helper/IDirect3DSwapChain9::GetFrontBufferData, direct3d9.idirect3dswapchain9__getfrontbufferdata
req.header: d3d9helper.h
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
 - IDirect3DSwapChain9::GetFrontBufferData
 - d3d9helper/IDirect3DSwapChain9::GetFrontBufferData
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
 - IDirect3DSwapChain9.GetFrontBufferData
---

# IDirect3DSwapChain9::GetFrontBufferData


## -description

Generates a copy of the swapchain's front buffer and places that copy in a system memory buffer provided by the application.

## -parameters

### -param pDestSurface [in, out]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface that will receive a copy of the swapchain's front buffer. The data is returned in successive rows with no intervening space, starting from the vertically highest row to the lowest.  For windowed mode, the size of the destination surface should be the size of the desktop. For full screen mode, the size of the destination surface should be the screen size.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 If BackBuffer exceeds or equals the total number of back buffers, the function fails and returns D3DERR_INVALIDCALL.

## -remarks

Calling this method will increase the internal reference count on the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface. Failure to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DSurface9</b> interface results in a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a>
