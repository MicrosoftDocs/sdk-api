---
UID: NF:d3d9.IDirect3DDevice9.TestCooperativeLevel
title: IDirect3DDevice9::TestCooperativeLevel
author: windows-sdk-content
description: Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.
old-location: direct3d9\idirect3ddevice9__testcooperativelevel.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__testcooperativelevel.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 613a6a7b-3b6f-b565-1f3a-2b5322844deb, IDirect3DDevice9 interface [Direct3D 9],TestCooperativeLevel method, IDirect3DDevice9.TestCooperativeLevel, IDirect3DDevice9::TestCooperativeLevel, TestCooperativeLevel, TestCooperativeLevel method [Direct3D 9], TestCooperativeLevel method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::TestCooperativeLevel, direct3d9.idirect3ddevice9__testcooperativelevel
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
 - IDirect3DDevice9.TestCooperativeLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9.h
: 
- IDirect3DDevice9.TestCooperativeLevel
: 
---

# IDirect3DDevice9::TestCooperativeLevel


## -description


Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK, indicating that the device is operational and the calling application can continue.
 If the method fails, the return value can be one of the following values: D3DERR_DEVICELOST, D3DERR_DEVICENOTRESET, D3DERR_DRIVERINTERNALERROR.




## -remarks



If the device is lost but cannot be restored at the current time, <b>IDirect3DDevice9::TestCooperativeLevel</b> returns the D3DERR_DEVICELOST return code. This would be the case, for example, when a full-screen device has lost focus. If an application detects a lost device, it should pause and periodically call <b>IDirect3DDevice9::TestCooperativeLevel</b> until it receives a return value of D3DERR_DEVICENOTRESET. The application may then attempt to reset the device by calling <a href="https://msdn.microsoft.com/en-us/library/Bb174425(v=VS.85).aspx">IDirect3DDevice9::Reset</a> and, if this succeeds, restore the necessary resources and resume normal operation. Note that <a href="https://msdn.microsoft.com/en-us/library/Bb174423(v=VS.85).aspx">IDirect3DDevice9::Present</a> will return D3DERR_DEVICELOST if the device is either "lost" or "not reset".

A call to <b>IDirect3DDevice9::TestCooperativeLevel</b> will fail if called on a different thread than that used to create the device being reset.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

