---
UID: NF:d3d9.IDirect3DDevice9.SetNPatchMode
title: IDirect3DDevice9::SetNPatchMode (d3d9.h)
description: The IDirect3DDevice9::SetNPatchMode method (d3d9.h) enables or disables N-patches.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetNPatchMode method","IDirect3DDevice9.SetNPatchMode","IDirect3DDevice9::SetNPatchMode","SetNPatchMode","SetNPatchMode method [Direct3D 9]","SetNPatchMode method [Direct3D 9]","IDirect3DDevice9 interface","a1559401-14f3-1ada-91cb-f26fd6d19851","d3d9helper/IDirect3DDevice9::SetNPatchMode","direct3d9.idirect3ddevice9__setnpatchmode"]
old-location: direct3d9\idirect3ddevice9__setnpatchmode.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setnpatchmode.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetNPatchMode method, IDirect3DDevice9.SetNPatchMode, IDirect3DDevice9::SetNPatchMode, SetNPatchMode, SetNPatchMode method [Direct3D 9], SetNPatchMode method [Direct3D 9],IDirect3DDevice9 interface, a1559401-14f3-1ada-91cb-f26fd6d19851, d3d9helper/IDirect3DDevice9::SetNPatchMode, direct3d9.idirect3ddevice9__setnpatchmode
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
 - IDirect3DDevice9::SetNPatchMode
 - d3d9/IDirect3DDevice9::SetNPatchMode
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
 - IDirect3DDevice9.SetNPatchMode
---

# IDirect3DDevice9::SetNPatchMode


## -description

Enable or disable N-patches.

## -parameters

### -param nSegments [in]

Type: <b>float</b>

Specifies the number of subdivision segments. If the number of segments is less than 1.0, N-patches are disabled. The default value is 0.0.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getnpatchmode">IDirect3DDevice9::GetNPatchMode</a>
