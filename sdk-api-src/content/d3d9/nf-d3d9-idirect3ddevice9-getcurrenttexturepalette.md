---
UID: NF:d3d9.IDirect3DDevice9.GetCurrentTexturePalette
title: IDirect3DDevice9::GetCurrentTexturePalette (d3d9.h)
description: The IDirect3DDevice9::GetCurrentTexturePalette method (d3d9.h) retrieves the current texture palette.
helpviewer_keywords: ["GetCurrentTexturePalette","GetCurrentTexturePalette method [Direct3D 9]","GetCurrentTexturePalette method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetCurrentTexturePalette method","IDirect3DDevice9.GetCurrentTexturePalette","IDirect3DDevice9::GetCurrentTexturePalette","d3d9helper/IDirect3DDevice9::GetCurrentTexturePalette","direct3d9.idirect3ddevice9__getcurrenttexturepalette","e2c8a5f6-1d2a-0371-2db7-743fbfb6531b"]
old-location: direct3d9\idirect3ddevice9__getcurrenttexturepalette.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getcurrenttexturepalette.htm
ms.date: 08/10/2022
ms.keywords: GetCurrentTexturePalette, GetCurrentTexturePalette method [Direct3D 9], GetCurrentTexturePalette method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetCurrentTexturePalette method, IDirect3DDevice9.GetCurrentTexturePalette, IDirect3DDevice9::GetCurrentTexturePalette, d3d9helper/IDirect3DDevice9::GetCurrentTexturePalette, direct3d9.idirect3ddevice9__getcurrenttexturepalette, e2c8a5f6-1d2a-0371-2db7-743fbfb6531b
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
 - IDirect3DDevice9::GetCurrentTexturePalette
 - d3d9/IDirect3DDevice9::GetCurrentTexturePalette
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
 - IDirect3DDevice9.GetCurrentTexturePalette
---

# IDirect3DDevice9::GetCurrentTexturePalette


## -description

Retrieves the current texture palette.

## -parameters

### -param PaletteNumber [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to a returned value that identifies the current texture palette.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setcurrenttexturepalette">IDirect3DDevice9::SetCurrentTexturePalette</a>



<a href="/windows/desktop/direct3d9/texture-palettes">Texture Palettes (Direct3D 9)</a>
