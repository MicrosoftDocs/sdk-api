---
UID: NF:d3d9.IDirect3DDevice9.SetSamplerState
title: IDirect3DDevice9::SetSamplerState
author: windows-sdk-content
description: Sets the sampler state value.
old-location: direct3d9\idirect3ddevice9__setsamplerstate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setsamplerstate.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetSamplerState method, IDirect3DDevice9.SetSamplerState, IDirect3DDevice9::SetSamplerState, SetSamplerState, SetSamplerState method [Direct3D 9], SetSamplerState method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetSamplerState, direct3d9.idirect3ddevice9__setsamplerstate, ea91fb0c-0668-d552-ee6a-25d1288ffe7f
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
 - IDirect3DDevice9.SetSamplerState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetSamplerState


## -description


Sets the sampler state value.


## -parameters




### -param Sampler [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The sampler stage index. For more info about sampler stage, see <a href="https://msdn.microsoft.com/en-us/library/Bb206339(v=VS.85).aspx">Sampling Stage Registers in vs_3_0 (DirectX HLSL)</a>.


### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172602(v=VS.85).aspx">D3DSAMPLERSTATETYPE</a></b>

This parameter can be any member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172602(v=VS.85).aspx">D3DSAMPLERSTATETYPE</a> enumerated type. 


### -param Value [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

State value to set. The meaning of this value is determined by the Type parameter. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174406(v=VS.85).aspx">IDirect3DDevice9::GetSamplerState</a>
 

 

