---
UID: NF:d3d9.IDirect3DSwapChain9Ex.GetDisplayModeEx
title: IDirect3DSwapChain9Ex::GetDisplayModeEx
author: windows-sdk-content
description: Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.
old-location: direct3d9\idirect3dswapchain9_getdisplaymodeex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9_getdisplaymodeex.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetDisplayModeEx, GetDisplayModeEx method [Direct3D 9], GetDisplayModeEx method [Direct3D 9],IDirect3DSwapChain9Ex interface, IDirect3DSwapChain9Ex interface [Direct3D 9],GetDisplayModeEx method, IDirect3DSwapChain9Ex.GetDisplayModeEx, IDirect3DSwapChain9Ex::GetDisplayModeEx, c69fe0ce-9d41-806c-6f4a-bb9c50054159, d3d9/IDirect3DSwapChain9Ex::GetDisplayModeEx, direct3d9.idirect3dswapchain9_getdisplaymodeex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DSwapChain9Ex.GetDisplayModeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DSwapChain9Ex::GetDisplayModeEx


## -description


Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.


## -parameters




### -param pMode [out]

Type: <b><a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a> structure containing data about the display mode of the adapter. As opposed to the display mode of the device, which may not be active if the device does not own full-screen mode. 


### -param pRotation [out]

Type: <b><a href="https://msdn.microsoft.com/190aa10e-4bf0-45ec-9c07-2582c5536074">D3DDISPLAYROTATION</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/190aa10e-4bf0-45ec-9c07-2582c5536074">D3DDISPLAYROTATION</a> indicating the type of screen rotation the application will do. The value returned through this pointer is important when the <a href="https://msdn.microsoft.com/1294171e-b3f6-4264-8411-b69427cefe7b">D3DPRESENTFLAG_NOAUTOROTATE</a> flag is used; otherwise, it can be set to <b>NULL</b>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/b5af736b-f1d6-4db2-bd57-d88fca65b0a6">IDirect3DSwapChain9Ex</a>
 

 

