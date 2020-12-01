---
UID: NF:d3d9.IDirect3DSwapChain9Ex.GetLastPresentCount
title: IDirect3DSwapChain9Ex::GetLastPresentCount (d3d9.h)
description: Returns the number of times the swapchain has been processed.
helpviewer_keywords: ["GetLastPresentCount","GetLastPresentCount method [Direct3D 9]","GetLastPresentCount method [Direct3D 9]","IDirect3DSwapChain9Ex interface","IDirect3DSwapChain9Ex interface [Direct3D 9]","GetLastPresentCount method","IDirect3DSwapChain9Ex.GetLastPresentCount","IDirect3DSwapChain9Ex::GetLastPresentCount","d305fb15-e0d6-5a21-767a-ac221539a549","d3d9/IDirect3DSwapChain9Ex::GetLastPresentCount","direct3d9.idirect3dswapchain9_getlastpresentcount"]
old-location: direct3d9\idirect3dswapchain9_getlastpresentcount.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9_getlastpresentcount.htm
ms.date: 12/05/2018
ms.keywords: GetLastPresentCount, GetLastPresentCount method [Direct3D 9], GetLastPresentCount method [Direct3D 9],IDirect3DSwapChain9Ex interface, IDirect3DSwapChain9Ex interface [Direct3D 9],GetLastPresentCount method, IDirect3DSwapChain9Ex.GetLastPresentCount, IDirect3DSwapChain9Ex::GetLastPresentCount, d305fb15-e0d6-5a21-767a-ac221539a549, d3d9/IDirect3DSwapChain9Ex::GetLastPresentCount, direct3d9.idirect3dswapchain9_getlastpresentcount
req.header: d3d9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DSwapChain9Ex::GetLastPresentCount
 - d3d9/IDirect3DSwapChain9Ex::GetLastPresentCount
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
 - IDirect3DSwapChain9Ex.GetLastPresentCount
---

# IDirect3DSwapChain9Ex::GetLastPresentCount


## -description

Returns the number of times the swapchain has been processed.

## -parameters

### -param pLastPresentCount [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to a UINT to be filled with the number of times the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex">IDirect3DDevice9Ex::PresentEx</a> method has been called. The count will also be incremented by calling some other APIs such as <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setdialogboxmode">IDirect3DDevice9::SetDialogBoxMode</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

S_OK the method was successful.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex">IDirect3DSwapChain9Ex</a>