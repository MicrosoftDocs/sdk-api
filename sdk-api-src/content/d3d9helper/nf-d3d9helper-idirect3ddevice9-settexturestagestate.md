---
UID: NF:d3d9helper.IDirect3DDevice9.SetTextureStageState
title: IDirect3DDevice9::SetTextureStageState
author: windows-sdk-content
description: Sets the state value for the currently assigned texture.
old-location: direct3d9\idirect3ddevice9__settexturestagestate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__settexturestagestate.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetTextureStageState method, IDirect3DDevice9.SetTextureStageState, IDirect3DDevice9::SetTextureStageState, SetTextureStageState, SetTextureStageState method [Direct3D 9], SetTextureStageState method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetTextureStageState, d527a1a7-ab83-8b59-b7eb-084188448dc6, direct3d9.idirect3ddevice9__settexturestagestate
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirect3DDevice9.SetTextureStageState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetTextureStageState


## -description


Sets the state value for the currently assigned texture.


## -parameters




### -param Stage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Stage identifier of the texture for which the state value is set. Stage identifiers are zero-based. Devices can have up to eight set textures, so the maximum value allowed for Stage is 7. 


### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/87a5a1bb-e748-4c72-8320-ea82250dcc0e">D3DTEXTURESTAGESTATETYPE</a></b>

Texture state to set. This parameter can be any member of the <a href="https://msdn.microsoft.com/87a5a1bb-e748-4c72-8320-ea82250dcc0e">D3DTEXTURESTAGESTATETYPE</a> enumerated type. 


### -param Value [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

State value to set. The meaning of this value is determined by the Type parameter. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/f472de6f-6c46-4424-95e5-62164afaf026">IDirect3DDevice9::GetTexture</a>



<a href="https://msdn.microsoft.com/8ecc2019-16f9-4c32-9ecb-33c2b85108dc">IDirect3DDevice9::GetTextureStageState</a>



<a href="https://msdn.microsoft.com/ec62aeee-037f-4c33-b242-e0483872016c">IDirect3DDevice9::SetTexture</a>
 

 

