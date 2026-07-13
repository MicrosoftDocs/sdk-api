---
UID: NF:d3d9helper.IDirect3DDevice9.SetSamplerState
title: IDirect3DDevice9::SetSamplerState (d3d9helper.h)
description: The IDirect3DDevice9::SetSamplerState method (d3d9helper.h) sets the sampler state value.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetSamplerState method","IDirect3DDevice9.SetSamplerState","IDirect3DDevice9::SetSamplerState","SetSamplerState","SetSamplerState method [Direct3D 9]","SetSamplerState method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetSamplerState","direct3d9.idirect3ddevice9__setsamplerstate","ea91fb0c-0668-d552-ee6a-25d1288ffe7f"]
old-location: direct3d9\idirect3ddevice9__setsamplerstate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setsamplerstate.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetSamplerState method, IDirect3DDevice9.SetSamplerState, IDirect3DDevice9::SetSamplerState, SetSamplerState, SetSamplerState method [Direct3D 9], SetSamplerState method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetSamplerState, direct3d9.idirect3ddevice9__setsamplerstate, ea91fb0c-0668-d552-ee6a-25d1288ffe7f
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::SetSamplerState
 - d3d9helper/IDirect3DDevice9::SetSamplerState
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
 - IDirect3DDevice9.SetSamplerState
---

# IDirect3DDevice9::SetSamplerState


## -description

Sets the sampler state value.

## -parameters

### -param Sampler [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The sampler stage index. For more info about sampler stage, see <a href="/windows/desktop/direct3d9/vertex-textures-in-vs-3-0">Sampling Stage Registers in vs_3_0 (DirectX HLSL)</a>.

### -param Type [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dsamplerstatetype">D3DSAMPLERSTATETYPE</a></b>

This parameter can be any member of the <a href="/windows/desktop/direct3d9/d3dsamplerstatetype">D3DSAMPLERSTATETYPE</a> enumerated type.

### -param Value [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

State value to set. The meaning of this value is determined by the Type parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getsamplerstate">IDirect3DDevice9::GetSamplerState</a>
