---
UID: NF:d3d9.IDirect3DDevice9.GetSwapChain
title: IDirect3DDevice9::GetSwapChain
author: windows-sdk-content
description: Gets a pointer to a swap chain.
old-location: direct3d9\idirect3ddevice9__getswapchain.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getswapchain.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 141571bf-172b-c679-109b-248388ab3cc3, GetSwapChain, GetSwapChain method [Direct3D 9], GetSwapChain method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetSwapChain method, IDirect3DDevice9.GetSwapChain, IDirect3DDevice9::GetSwapChain, d3d9helper/IDirect3DDevice9::GetSwapChain, direct3d9.idirect3ddevice9__getswapchain
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
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
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetSwapChain


## -description


Gets a pointer to a swap chain.


## -parameters




### -param iSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The swap chain ordinal value.  For more information, see NumberOfAdaptersInGroup in <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a>.


### -param pSwapChain






#### - ppSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205899(v=VS.85).aspx">IDirect3DSwapChain9</a>**</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb205899(v=VS.85).aspx">IDirect3DSwapChain9</a> interface that will receive a copy of swap chain. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

