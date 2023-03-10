---
UID: NF:d3d9.IDirect3DDevice9.GetPaletteEntries
title: IDirect3DDevice9::GetPaletteEntries (d3d9.h)
description: The IDirect3DDevice9::GetPaletteEntries method (d3d9.h) retrieves palette entries.
helpviewer_keywords: ["GetPaletteEntries","GetPaletteEntries method [Direct3D 9]","GetPaletteEntries method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetPaletteEntries method","IDirect3DDevice9.GetPaletteEntries","IDirect3DDevice9::GetPaletteEntries","c99163c4-eea0-1af6-c7fd-c8d1cfd3d969","d3d9helper/IDirect3DDevice9::GetPaletteEntries","direct3d9.idirect3ddevice9__getpaletteentries"]
old-location: direct3d9\idirect3ddevice9__getpaletteentries.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getpaletteentries.htm
ms.date: 08/10/2022
ms.keywords: GetPaletteEntries, GetPaletteEntries method [Direct3D 9], GetPaletteEntries method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetPaletteEntries method, IDirect3DDevice9.GetPaletteEntries, IDirect3DDevice9::GetPaletteEntries, c99163c4-eea0-1af6-c7fd-c8d1cfd3d969, d3d9helper/IDirect3DDevice9::GetPaletteEntries, direct3d9.idirect3ddevice9__getpaletteentries
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
 - IDirect3DDevice9::GetPaletteEntries
 - d3d9/IDirect3DDevice9::GetPaletteEntries
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
 - IDirect3DDevice9.GetPaletteEntries
---

# IDirect3DDevice9::GetPaletteEntries


## -description

Retrieves palette entries.

## -parameters

### -param PaletteNumber [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An ordinal value identifying the particular palette to retrieve.

### -param pEntries [in, out]

Type: <b><a href="/windows/desktop/api/wingdi/ns-wingdi-paletteentry">PALETTEENTRY</a>*</b>

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-paletteentry">PALETTEENTRY</a> structure, representing the returned palette entries.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

For more information about <a href="/windows/desktop/api/wingdi/ns-wingdi-paletteentry">PALETTEENTRY</a>, see the Platform SDK.

<div class="alert"><b>Note</b>  As of Direct3D 9, the peFlags member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-paletteentry">PALETTEENTRY</a> structure does not work the way it is documented in the Platform SDK. The peFlags member is now the alpha channel for 8-bit palettized formats.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getcurrenttexturepalette">IDirect3DDevice9::GetCurrentTexturePalette</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setcurrenttexturepalette">IDirect3DDevice9::SetCurrentTexturePalette</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpaletteentries">IDirect3DDevice9::SetPaletteEntries</a>



<a href="/windows/desktop/direct3d9/texture-palettes">Texture Palettes (Direct3D 9)</a>
