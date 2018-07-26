---
UID: NF:d3d9helper.IDirect3DDevice9.GetDisplayMode
title: IDirect3DDevice9::GetDisplayMode
author: windows-sdk-content
description: Retrieves the display mode's spatial resolution, color resolution, and refresh frequency.
old-location: direct3d9\idirect3ddevice9__getdisplaymode.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getdisplaymode.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 9b212895-5a3c-2630-7af4-0caee7db56cb, GetDisplayMode, GetDisplayMode method [Direct3D 9], GetDisplayMode method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetDisplayMode method, IDirect3DDevice9.GetDisplayMode, IDirect3DDevice9::GetDisplayMode, d3d9helper/IDirect3DDevice9::GetDisplayMode, direct3d9.idirect3ddevice9__getdisplaymode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.GetDisplayMode
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetDisplayMode


## -description


Retrieves the display mode's spatial resolution, color resolution, and refresh frequency.


## -parameters




### -param iSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An unsigned integer specifying the swap chain.


### -param pMode [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb172548(v=VS.85).aspx">D3DDISPLAYMODE</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/Bb172548(v=VS.85).aspx">D3DDISPLAYMODE</a> structure containing data about the display mode of the adapter. As opposed to the display mode of the device, which may not be active if the device does not own full-screen mode. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

