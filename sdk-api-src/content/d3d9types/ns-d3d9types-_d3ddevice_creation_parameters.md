---
UID: NS:d3d9types._D3DDEVICE_CREATION_PARAMETERS
title: "_D3DDEVICE_CREATION_PARAMETERS"
author: windows-driver-content
description: Describes the creation parameters for a device.
old-location: direct3d9\d3ddevice_creation_parameters.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddevice_creation_parameters.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 0968748e-3ab2-c292-373c-380ccfb387f0, D3DDEVICE_CREATION_PARAMETERS, D3DDEVICE_CREATION_PARAMETERS structure [Direct3D 9], LPD3DDEVICE_CREATION_PARAMETERS, LPD3DDEVICE_CREATION_PARAMETERS structure pointer [Direct3D 9], _D3DDEVICE_CREATION_PARAMETERS, d3d9types/D3DDEVICE_CREATION_PARAMETERS, d3d9types/LPD3DDEVICE_CREATION_PARAMETERS, direct3d9.d3ddevice_creation_parameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DDEVICE_CREATION_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDEVICE_CREATION_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDEVICE_CREATION_PARAMETERS structure


## -description


Describes the creation parameters for a device.


## -struct-fields




### -field AdapterOrdinal

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number that denotes the display adapter. D3DADAPTER_DEFAULT is always the primary display adapter. 
    
 Use this ordinal as the Adapter parameter for any of the <a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a> methods. Note that different instances of Direct3D 9.0 objects can use different ordinals. Adapters can enter or leave a system when users, for example, add or remove monitors from a multiple-monitor system or when they hot-swap a laptop. Consequently, use this ordinal only in a Direct3D 9.0 instance known to be valid, that is, either the Direct3D 9.0 that created this <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a> interface or the Direct3D 9.0 returned from <a href="https://msdn.microsoft.com/42666561-fb2b-47b4-b2c4-49926ea67964">GetDirect3D</a>, as called through this <b>IDirect3DDevice9</b> interface.


### -field DeviceType

Type: <b><a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a> enumerated type. Denotes the amount of emulated functionality for this device. The value of this parameter mirrors the value passed to the <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">CreateDevice</a> call that created this device.


### -field hFocusWindow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Window handle to which focus belongs for this Direct3D device. The value of this parameter mirrors the value passed to the <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">CreateDevice</a> call that created this device.


### -field BehaviorFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A combination of one or more <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE</a> constants that control global behavior of the device. These constants mirror the constants passed to <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">CreateDevice</a> when the device was created.


## -see-also




<a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">CreateDevice</a>



<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/18889d40-a64f-41da-92dd-7b197749e685">GetCreationParameters</a>
 

 

