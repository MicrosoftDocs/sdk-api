---
UID: NF:d3d9helper.IDirect3DDevice9.GetTextureStageState
title: IDirect3DDevice9::GetTextureStageState
author: windows-sdk-content
description: Retrieves a state value for an assigned texture.
old-location: direct3d9\idirect3ddevice9__gettexturestagestate.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__gettexturestagestate.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 8b57c261-2c3b-959e-ad7c-dc12c2854d73, GetTextureStageState, GetTextureStageState method [Direct3D 9], GetTextureStageState method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetTextureStageState method, IDirect3DDevice9.GetTextureStageState, IDirect3DDevice9::GetTextureStageState, d3d9helper/IDirect3DDevice9::GetTextureStageState, direct3d9.idirect3ddevice9__gettexturestagestate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.GetTextureStageState
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetTextureStageState


## -description


Retrieves a state value for an assigned texture.


## -parameters




### -param Stage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Stage identifier of the texture for which the state is retrieved. Stage identifiers are zero-based. Devices can have up to eight set textures, so the maximum value allowed for Stage is 7. 


### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/87a5a1bb-e748-4c72-8320-ea82250dcc0e">D3DTEXTURESTAGESTATETYPE</a></b>

Texture state to retrieve. This parameter can be any member of the <a href="https://msdn.microsoft.com/87a5a1bb-e748-4c72-8320-ea82250dcc0e">D3DTEXTURESTAGESTATETYPE</a> enumerated type. 


### -param pValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer a variable to fill with the retrieved state value. The meaning of the retrieved value is determined by the Type parameter. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other flag values in <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE</a>."
    





## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/f472de6f-6c46-4424-95e5-62164afaf026">IDirect3DDevice9::GetTexture</a>



<a href="https://msdn.microsoft.com/ec62aeee-037f-4c33-b242-e0483872016c">IDirect3DDevice9::SetTexture</a>



<a href="https://msdn.microsoft.com/303f7a80-edaf-4106-a4ce-8fb7a7d30a5a">IDirect3DDevice9::SetTextureStageState</a>
 

 

