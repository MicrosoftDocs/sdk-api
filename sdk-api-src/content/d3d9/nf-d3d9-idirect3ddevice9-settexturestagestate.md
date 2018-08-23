---
UID: NF:d3d9.IDirect3DDevice9.SetTextureStageState
title: IDirect3DDevice9::SetTextureStageState
author: windows-sdk-content
description: Sets the state value for the currently assigned texture.
old-location: direct3d9\idirect3ddevice9__settexturestagestate.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__settexturestagestate.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetTextureStageState method, IDirect3DDevice9.SetTextureStageState, IDirect3DDevice9::SetTextureStageState, SetTextureStageState, SetTextureStageState method [Direct3D 9], SetTextureStageState method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetTextureStageState, d527a1a7-ab83-8b59-b7eb-084188448dc6, direct3d9.idirect3ddevice9__settexturestagestate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
req.redist: 
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.SetTextureStageState
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetTextureStageState


## -description


Sets the state value for the currently assigned texture.


## -parameters




### -param Stage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Stage identifier of the texture for which the state value is set. Stage identifiers are zero-based. Devices can have up to eight set textures, so the maximum value allowed for Stage is 7. 


### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172617(v=VS.85).aspx">D3DTEXTURESTAGESTATETYPE</a></b>

Texture state to set. This parameter can be any member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172617(v=VS.85).aspx">D3DTEXTURESTAGESTATETYPE</a> enumerated type. 


### -param Value [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

State value to set. The meaning of this value is determined by the Type parameter. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174412(v=VS.85).aspx">IDirect3DDevice9::GetTexture</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174413(v=VS.85).aspx">IDirect3DDevice9::GetTextureStageState</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174461(v=VS.85).aspx">IDirect3DDevice9::SetTexture</a>
 

 

