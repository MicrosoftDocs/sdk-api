---
UID: NF:d3d9.IDirect3DDevice9.GetTextureStageState
title: IDirect3DDevice9::GetTextureStageState (d3d9.h)
description: The IDirect3DDevice9::GetTextureStageState method (d3d9.h) retrieves a state value for an assigned texture.
helpviewer_keywords: ["8b57c261-2c3b-959e-ad7c-dc12c2854d73","GetTextureStageState","GetTextureStageState method [Direct3D 9]","GetTextureStageState method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetTextureStageState method","IDirect3DDevice9.GetTextureStageState","IDirect3DDevice9::GetTextureStageState","d3d9helper/IDirect3DDevice9::GetTextureStageState","direct3d9.idirect3ddevice9__gettexturestagestate"]
old-location: direct3d9\idirect3ddevice9__gettexturestagestate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__gettexturestagestate.htm
ms.date: 08/11/2022
ms.keywords: 8b57c261-2c3b-959e-ad7c-dc12c2854d73, GetTextureStageState, GetTextureStageState method [Direct3D 9], GetTextureStageState method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetTextureStageState method, IDirect3DDevice9.GetTextureStageState, IDirect3DDevice9::GetTextureStageState, d3d9helper/IDirect3DDevice9::GetTextureStageState, direct3d9.idirect3ddevice9__gettexturestagestate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::GetTextureStageState
 - d3d9/IDirect3DDevice9::GetTextureStageState
dev_langs:
 - c++
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
---

# IDirect3DDevice9::GetTextureStageState


## -description

Retrieves a state value for an assigned texture.

## -parameters

### -param Stage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Stage identifier of the texture for which the state is retrieved. Stage identifiers are zero-based. Devices can have up to eight set textures, so the maximum value allowed for Stage is 7.

### -param Type [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dtexturestagestatetype">D3DTEXTURESTAGESTATETYPE</a></b>

Texture state to retrieve. This parameter can be any member of the <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype">D3DTEXTURESTAGESTATETYPE</a> enumerated type.

### -param pValue [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Pointer a variable to fill with the retrieved state value. The meaning of the retrieved value is determined by the Type parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other flag values in <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>."

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexture">IDirect3DDevice9::GetTexture</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture">IDirect3DDevice9::SetTexture</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate">IDirect3DDevice9::SetTextureStageState</a>
