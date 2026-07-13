---
UID: NF:d3d9.IDirect3DDevice9.GetNumberOfSwapChains
title: IDirect3DDevice9::GetNumberOfSwapChains (d3d9.h)
description: The IDirect3DDevice9::GetNumberOfSwapChains method (d3d9.h) gets the number of implicit swap chains.
helpviewer_keywords: ["84771686-c1f5-0be3-b170-1de4e0c8acc9","GetNumberOfSwapChains","GetNumberOfSwapChains method [Direct3D 9]","GetNumberOfSwapChains method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetNumberOfSwapChains method","IDirect3DDevice9.GetNumberOfSwapChains","IDirect3DDevice9::GetNumberOfSwapChains","d3d9helper/IDirect3DDevice9::GetNumberOfSwapChains","direct3d9.idirect3ddevice9__getnumberofswapchains"]
old-location: direct3d9\idirect3ddevice9__getnumberofswapchains.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getnumberofswapchains.htm
ms.date: 08/10/2022
ms.keywords: 84771686-c1f5-0be3-b170-1de4e0c8acc9, GetNumberOfSwapChains, GetNumberOfSwapChains method [Direct3D 9], GetNumberOfSwapChains method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetNumberOfSwapChains method, IDirect3DDevice9.GetNumberOfSwapChains, IDirect3DDevice9::GetNumberOfSwapChains, d3d9helper/IDirect3DDevice9::GetNumberOfSwapChains, direct3d9.idirect3ddevice9__getnumberofswapchains
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
 - IDirect3DDevice9::GetNumberOfSwapChains
 - d3d9/IDirect3DDevice9::GetNumberOfSwapChains
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
 - IDirect3DDevice9.GetNumberOfSwapChains
---

# IDirect3DDevice9::GetNumberOfSwapChains


## -description

Gets the number of implicit swap chains.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of implicit swap chains. See Remarks.

## -remarks

Implicit swap chains are created by the device during <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a>. This method returns the number of swap chains created by CreateDevice. 
    


An application may create additional swap chains using <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createadditionalswapchain">IDirect3DDevice9::CreateAdditionalSwapChain</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
