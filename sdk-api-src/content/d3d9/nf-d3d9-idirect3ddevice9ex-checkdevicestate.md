---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirect3DDevice9Ex::CheckDeviceState


## -description


Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.


## -parameters




### -param hDestinationWindow






#### - hWindow [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The destination window handle to check for occlusion. When this parameter is <b>NULL</b>, S_PRESENT_OCCLUDED is returned when another device has fullscreen ownership. When the window handle is not <b>NULL</b>, window's client area is checked for occlusion. A window is occluded if any part of it is obscured by another application.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Possible return values include: D3D_OK, D3DERR_DEVICELOST, D3DERR_DEVICEHUNG, D3DERR_DEVICEREMOVED, or D3DERR_OUTOFVIDEOMEMORY (see <a href="https://msdn.microsoft.com/4a9daa05-74f3-4173-b63d-53767feea7e2">D3DERR</a>), or S_PRESENT_MODE_CHANGED, or S_PRESENT_OCCLUDED (see <a href="https://msdn.microsoft.com/391b56a1-d0aa-4d35-8dba-cf7de66513d8">S_PRESENT</a>).




## -remarks



This method replaces <a href="https://msdn.microsoft.com/da2ac8dd-0df8-4661-995f-9c3e6ccb62d2">IDirect3DDevice9::TestCooperativeLevel</a>, which always returns S_OK in Direct3D 9Ex applications.

We recommend not to call <b>CheckDeviceState</b> every frame. Instead, call <b>CheckDeviceState</b> only if the <a href="https://msdn.microsoft.com/845c72ff-669d-44bf-8065-cff456418e8c">IDirect3DDevice9Ex::PresentEx</a> method returns a failure code.

See <a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">Lost Device Behavior Changes</a> for more information about lost, hung, and removed devices.




## -see-also




<a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>
 

 

