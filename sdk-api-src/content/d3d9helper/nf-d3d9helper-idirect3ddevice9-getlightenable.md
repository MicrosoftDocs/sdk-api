---
UID: NF:d3d9helper.IDirect3DDevice9.GetLightEnable
title: IDirect3DDevice9::GetLightEnable
author: windows-sdk-content
description: Retrieves the activity status - enabled or disabled - for a set of lighting parameters within a device.
old-location: direct3d9\idirect3ddevice9__getlightenable.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getlightenable.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 2d73c9f9-8cdd-b499-9dc6-930ac19d6977, GetLightEnable, GetLightEnable method [Direct3D 9], GetLightEnable method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetLightEnable method, IDirect3DDevice9.GetLightEnable, IDirect3DDevice9::GetLightEnable, d3d9helper/IDirect3DDevice9::GetLightEnable, direct3d9.idirect3ddevice9__getlightenable
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9.GetLightEnable
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetLightEnable


## -description


Retrieves the activity status - enabled or disabled - for a set of lighting parameters within a device.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Zero-based index of the set of lighting parameters that are the target of this method. 


### -param pEnable [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Pointer to a variable to fill with the status of the specified lighting parameters. After the call, a nonzero value at this address indicates that the specified lighting parameters are enabled; a value of 0 indicates that they are disabled. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other values in <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE</a>.
    





## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/1e52be8e-7e24-400d-89c5-93dd316534bc">IDirect3DDevice9::GetLight</a>



<a href="https://msdn.microsoft.com/3a23a10b-ded5-4dfc-ac17-ebe199f9a788">IDirect3DDevice9::LightEnable</a>



<a href="https://msdn.microsoft.com/e1f07ba6-8a9f-4bac-8dad-16160559fa4c">IDirect3DDevice9::SetLight</a>
 

 

