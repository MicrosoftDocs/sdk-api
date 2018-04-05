---
UID: NF:d3d9.IDirect3D9Ex.GetAdapterDisplayModeEx
title: IDirect3D9Ex::GetAdapterDisplayModeEx method
author: windows-driver-content
description: Retrieves the current display mode and rotation settings of the adapter.
old-location: direct3d9\idirect3d9ex_getadapterdisplaymodeex.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_getadapterdisplaymodeex.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetAdapterDisplayModeEx method [Direct3D 9], GetAdapterDisplayModeEx method [Direct3D 9], IDirect3D9Ex interface, GetAdapterDisplayModeEx,IDirect3D9Ex.GetAdapterDisplayModeEx, IDirect3D9Ex, IDirect3D9Ex interface [Direct3D 9], GetAdapterDisplayModeEx method, IDirect3D9Ex::GetAdapterDisplayModeEx, a9a9a87a-36fb-8647-d001-d83d9020a82e, d3d9/IDirect3D9Ex::GetAdapterDisplayModeEx, direct3d9.idirect3d9ex_getadapterdisplaymodeex
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3D9Ex.GetAdapterDisplayModeEx
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3D9Ex::GetAdapterDisplayModeEx method


## -description


Retrieves the current display mode and rotation settings of the adapter.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number that denotes the display adapter to query. D3DADAPTER_DEFAULT is always the primary display adapter. 


### -param pMode [in, out]

Type: <b><a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a> structure containing data about the display mode of the adapter. As opposed to the display mode of the device, which may not be active if the device does not own full-screen mode. Can be set to <b>NULL</b>.


### -param pRotation [in, out]

Type: <b><a href="https://msdn.microsoft.com/190aa10e-4bf0-45ec-9c07-2582c5536074">D3DDISPLAYROTATION</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/190aa10e-4bf0-45ec-9c07-2582c5536074">D3DDISPLAYROTATION</a> structure indicating the type of screen rotation the application will do. The value returned through this pointer is important when the <a href="https://msdn.microsoft.com/1294171e-b3f6-4264-8411-b69427cefe7b">D3DPRESENTFLAG_NOAUTOROTATE</a> flag is used; otherwise, it can be set to <b>NULL</b>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. 



If <i>Adapter</i> is out of range or <i>pMode</i> is invalid, this method returns D3DERR_INVALIDCALL.




## -remarks



<b>GetAdapterDisplayModeEx</b> does not return the correct format when the display is in an extended format, such as 2:10:10:10. Instead, it returns the format X8R8G8B8.

To windowed applications, a value of S_PRESENT_MODE_CHANGED returned from <a href="https://msdn.microsoft.com/845c72ff-669d-44bf-8065-cff456418e8c">PresentEx</a> or <a href="https://msdn.microsoft.com/89a9b112-5f0a-4e57-9b8e-48b3a76a09ce">CheckDeviceState</a> indicates that the display mode changed and that the current display mode might have a different format. To avoid a color-converting Present blt, windowed applications can optionally get new display mode information by using this method and adjusting its swap chain format accordingly. This method returns D3DERR_NOTAVAILABLE if this head is no longer part of the desktop or if the monitor is disconnected.




## -see-also




<a href="https://msdn.microsoft.com/68dbd2d4-0a38-47fc-ad3d-4ac209ed98a8">IDirect3D9Ex</a>
 

 

