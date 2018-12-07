---
UID: NF:d3d9.IDirect3DDevice9.GetSamplerState
title: IDirect3DDevice9::GetSamplerState
author: windows-sdk-content
description: Gets the sampler state value.
old-location: direct3d9\idirect3ddevice9__getsamplerstate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getsamplerstate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 2f2d9d2b-67e2-1c0d-8bc2-e3824a20ab32, GetSamplerState, GetSamplerState method [Direct3D 9], GetSamplerState method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetSamplerState method, IDirect3DDevice9.GetSamplerState, IDirect3DDevice9::GetSamplerState, d3d9helper/IDirect3DDevice9::GetSamplerState, direct3d9.idirect3ddevice9__getsamplerstate
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
 - IDirect3DDevice9.GetSamplerState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetSamplerState


## -description


Gets the sampler state value.


## -parameters




### -param Sampler [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The sampler stage index.


### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172602(v=VS.85).aspx">D3DSAMPLERSTATETYPE</a></b>

This parameter can be any member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172602(v=VS.85).aspx">D3DSAMPLERSTATETYPE</a> enumerated type. 


### -param pValue [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

State value to get. The meaning of this value is determined by the Type parameter. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other values in <a href="https://msdn.microsoft.com/en-us/library/Bb172527(v=VS.85).aspx">D3DCREATE</a>."
    





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174456(v=VS.85).aspx">IDirect3DDevice9::SetSamplerState</a>
 

 

