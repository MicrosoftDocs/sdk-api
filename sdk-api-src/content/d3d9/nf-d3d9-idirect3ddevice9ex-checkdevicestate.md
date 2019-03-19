---
UID: NF:d3d9.IDirect3DDevice9Ex.CheckDeviceState
title: IDirect3DDevice9Ex::CheckDeviceState (d3d9.h)
author: windows-sdk-content
description: Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.
old-location: direct3d9\idirect3ddevice9ex_checkdevicestate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_checkdevicestate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 7c555cdc-567a-be2d-d677-3b3df3746e0b, CheckDeviceState, CheckDeviceState method [Direct3D 9], CheckDeviceState method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],CheckDeviceState method, IDirect3DDevice9Ex.CheckDeviceState, IDirect3DDevice9Ex::CheckDeviceState, d3d9/IDirect3DDevice9Ex::CheckDeviceState, direct3d9.idirect3ddevice9ex_checkdevicestate
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
 - IDirect3DDevice9Ex.CheckDeviceState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9Ex::CheckDeviceState


## -description


Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.


## -parameters




### -param hDestinationWindow [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The destination window handle to check for occlusion. When this parameter is <b>NULL</b>, S_PRESENT_OCCLUDED is returned when another device has fullscreen ownership. When the window handle is not <b>NULL</b>, window's client area is checked for occlusion. A window is occluded if any part of it is obscured by another application.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Possible return values include: D3D_OK, D3DERR_DEVICELOST, D3DERR_DEVICEHUNG, D3DERR_DEVICEREMOVED, or D3DERR_OUTOFVIDEOMEMORY (see <a href="https://msdn.microsoft.com/en-us/library/Bb172554(v=VS.85).aspx">D3DERR</a>), or S_PRESENT_MODE_CHANGED, or S_PRESENT_OCCLUDED (see <a href="https://msdn.microsoft.com/en-us/library/Bb219624(v=VS.85).aspx">S_PRESENT</a>).




## -remarks



This method replaces <a href="https://msdn.microsoft.com/en-us/library/Bb174472(v=VS.85).aspx">IDirect3DDevice9::TestCooperativeLevel</a>, which always returns S_OK in Direct3D 9Ex applications.

We recommend not to call <b>CheckDeviceState</b> every frame. Instead, call <b>CheckDeviceState</b> only if the <a href="https://msdn.microsoft.com/en-us/library/Bb174343(v=VS.85).aspx">IDirect3DDevice9Ex::PresentEx</a> method returns a failure code.

See <a href="https://msdn.microsoft.com/en-us/library/Bb219800(v=VS.85).aspx">Lost Device Behavior Changes</a> for more information about lost, hung, and removed devices.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174337(v=VS.85).aspx">IDirect3DDevice9Ex</a>
 

 

