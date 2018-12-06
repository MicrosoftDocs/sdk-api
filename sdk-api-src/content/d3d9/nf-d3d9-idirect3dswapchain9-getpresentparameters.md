---
UID: NF:d3d9.IDirect3DSwapChain9.GetPresentParameters
title: IDirect3DSwapChain9::GetPresentParameters
author: windows-sdk-content
description: Retrieves the presentation parameters associated with a swap chain.
old-location: direct3d9\idirect3dswapchain9__getpresentparameters.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9__getpresentparameters.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPresentParameters, GetPresentParameters method [Direct3D 9], GetPresentParameters method [Direct3D 9],IDirect3DSwapChain9 interface, IDirect3DSwapChain9 interface [Direct3D 9],GetPresentParameters method, IDirect3DSwapChain9.GetPresentParameters, IDirect3DSwapChain9::GetPresentParameters, ac85b9e4-b5da-4efa-cb76-254ef41c07cb, d3d9helper/IDirect3DSwapChain9::GetPresentParameters, direct3d9.idirect3dswapchain9__getpresentparameters
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirect3DSwapChain9.GetPresentParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DSwapChain9::GetPresentParameters


## -description


Retrieves the presentation parameters associated with a swap chain.


## -parameters




### -param pPresentationParameters [out, retval]

Type: <b><a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to the presentation parameters. See <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



This method can be used to see the presentation parameters of the parent swap chain of a surface (a back buffer, for instance). The parent swap chain can be retrieved with <a href="https://msdn.microsoft.com/f95f6104-4195-4d01-92c2-512879c9b449">IDirect3DSurface9::GetContainer</a>.




## -see-also




<a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a>
 

 

