---
UID: NF:d3d9.IDirect3DDevice9.SetTextureStageState
title: IDirect3DDevice9::SetTextureStageState (d3d9.h)
description: The IDirect3DDevice9::SetTextureStageState method (d3d9helper.h) sets the state value for the currently assigned texture. 
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetTextureStageState method","IDirect3DDevice9.SetTextureStageState","IDirect3DDevice9::SetTextureStageState","SetTextureStageState","SetTextureStageState method [Direct3D 9]","SetTextureStageState method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetTextureStageState","d527a1a7-ab83-8b59-b7eb-084188448dc6","direct3d9.idirect3ddevice9__settexturestagestate"]
old-location: direct3d9\idirect3ddevice9__settexturestagestate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__settexturestagestate.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetTextureStageState method, IDirect3DDevice9.SetTextureStageState, IDirect3DDevice9::SetTextureStageState, SetTextureStageState, SetTextureStageState method [Direct3D 9], SetTextureStageState method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetTextureStageState, d527a1a7-ab83-8b59-b7eb-084188448dc6, direct3d9.idirect3ddevice9__settexturestagestate
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
 - IDirect3DDevice9::SetTextureStageState
 - d3d9/IDirect3DDevice9::SetTextureStageState
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
 - IDirect3DDevice9.SetTextureStageState
---

# IDirect3DDevice9::SetTextureStageState


## -description

Sets the state value for the currently assigned texture.

## -parameters

### -param Stage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Stage identifier of the texture for which the state value is set. Stage identifiers are zero-based. Devices can have up to eight set textures, so the maximum value allowed for Stage is 7.

### -param Type [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dtexturestagestatetype">D3DTEXTURESTAGESTATETYPE</a></b>

Texture state to set. This parameter can be any member of the <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype">D3DTEXTURESTAGESTATETYPE</a> enumerated type.

### -param Value [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

State value to set. The meaning of this value is determined by the Type parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexture">IDirect3DDevice9::GetTexture</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexturestagestate">IDirect3DDevice9::GetTextureStageState</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture">IDirect3DDevice9::SetTexture</a>
