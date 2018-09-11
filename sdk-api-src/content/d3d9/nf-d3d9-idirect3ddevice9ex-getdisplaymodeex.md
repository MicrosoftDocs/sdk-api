---
UID: NF:d3d9.IDirect3DDevice9Ex.GetDisplayModeEx
title: IDirect3DDevice9Ex::GetDisplayModeEx
author: windows-sdk-content
description: Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.
old-location: direct3d9\idirect3ddevice9ex_getdisplaymodeex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_getdisplaymodeex.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 3de20b27-6ffa-11bb-e9a5-d1af96f798ac, GetDisplayModeEx, GetDisplayModeEx method [Direct3D 9], GetDisplayModeEx method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],GetDisplayModeEx method, IDirect3DDevice9Ex.GetDisplayModeEx, IDirect3DDevice9Ex::GetDisplayModeEx, d3d9/IDirect3DDevice9Ex::GetDisplayModeEx, direct3d9.idirect3ddevice9ex_getdisplaymodeex
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
 - IDirect3DDevice9Ex.GetDisplayModeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9Ex::GetDisplayModeEx


## -description


Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.


## -parameters




### -param iSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An unsigned integer specifying the swap chain.


### -param pMode [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172549(v=VS.85).aspx">D3DDISPLAYMODEEX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172549(v=VS.85).aspx">D3DDISPLAYMODEEX</a> structure containing data about the display mode of the adapter. As opposed to the display mode of the device, which may not be active if the device does not own full-screen mode. Can be set to <b>NULL</b>.


### -param pRotation [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172551(v=VS.85).aspx">D3DDISPLAYROTATION</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172551(v=VS.85).aspx">D3DDISPLAYROTATION</a> indicating the type of screen rotation the application will do. The value returned through this pointer is important when the <a href="https://msdn.microsoft.com/en-us/library/Bb172586(v=VS.85).aspx">D3DPRESENTFLAG_NOAUTOROTATE</a> flag is used; otherwise, it can be set to <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174337(v=VS.85).aspx">IDirect3DDevice9Ex</a>
 

 

