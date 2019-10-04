---
UID: NF:d3d9.IDirect3DDevice9.GetSwapChain
title: IDirect3DDevice9::GetSwapChain (d3d9.h)
author: windows-sdk-content
description: Gets a pointer to a swap chain.
old-location: direct3d9\idirect3ddevice9__getswapchain.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getswapchain.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 141571bf-172b-c679-109b-248388ab3cc3, GetSwapChain, GetSwapChain method [Direct3D 9], GetSwapChain method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetSwapChain method, IDirect3DDevice9.GetSwapChain, IDirect3DDevice9::GetSwapChain, d3d9helper/IDirect3DDevice9::GetSwapChain, direct3d9.idirect3ddevice9__getswapchain
ms.topic: method
f1_keywords:
- d3d9/IDirect3DDevice9.GetSwapChain
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D9.lib
- D3D9.dll
api_name:
- IDirect3DDevice9.GetSwapChain
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9::GetSwapChain


## -description


Gets a pointer to a swap chain.


## -parameters




### -param iSwapChain [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The swap chain ordinal value.  For more information, see NumberOfAdaptersInGroup in <a href="https://docs.microsoft.com/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a>.


### -param pSwapChain [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a>**</b>

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a> interface that will receive a copy of swap chain. 


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
 

 

