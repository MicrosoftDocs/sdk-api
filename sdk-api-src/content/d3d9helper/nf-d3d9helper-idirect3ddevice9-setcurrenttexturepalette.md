---
UID: NF:d3d9helper.IDirect3DDevice9.SetCurrentTexturePalette
title: IDirect3DDevice9::SetCurrentTexturePalette (d3d9helper.h)
description: The IDirect3DDevice9::SetCurrentTexturePalette method (d3d9.h) sets the current texture palette.
helpviewer_keywords: ["94925c3c-1326-79c0-a0f6-53b8d6877539","IDirect3DDevice9 interface [Direct3D 9]","SetCurrentTexturePalette method","IDirect3DDevice9.SetCurrentTexturePalette","IDirect3DDevice9::SetCurrentTexturePalette","SetCurrentTexturePalette","SetCurrentTexturePalette method [Direct3D 9]","SetCurrentTexturePalette method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetCurrentTexturePalette","direct3d9.idirect3ddevice9__setcurrenttexturepalette"]
old-location: direct3d9\idirect3ddevice9__setcurrenttexturepalette.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setcurrenttexturepalette.htm
ms.date: 08/11/2022
ms.keywords: 94925c3c-1326-79c0-a0f6-53b8d6877539, IDirect3DDevice9 interface [Direct3D 9],SetCurrentTexturePalette method, IDirect3DDevice9.SetCurrentTexturePalette, IDirect3DDevice9::SetCurrentTexturePalette, SetCurrentTexturePalette, SetCurrentTexturePalette method [Direct3D 9], SetCurrentTexturePalette method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetCurrentTexturePalette, direct3d9.idirect3ddevice9__setcurrenttexturepalette
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
 - IDirect3DDevice9::SetCurrentTexturePalette
 - d3d9helper/IDirect3DDevice9::SetCurrentTexturePalette
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
 - IDirect3DDevice9.SetCurrentTexturePalette
---

# IDirect3DDevice9::SetCurrentTexturePalette


## -description

Sets the current texture palette.

## -parameters

### -param PaletteNumber [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Value that specifies the texture palette to set as the current texture palette.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

A single logical palette is associated with the device, and is shared by all texture stages.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getcurrenttexturepalette">IDirect3DDevice9::GetCurrentTexturePalette</a>



<a href="/windows/desktop/direct3d9/texture-palettes">Texture Palettes (Direct3D 9)</a>
