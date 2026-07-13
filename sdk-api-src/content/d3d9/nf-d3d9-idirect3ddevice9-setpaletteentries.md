---
UID: NF:d3d9.IDirect3DDevice9.SetPaletteEntries
title: IDirect3DDevice9::SetPaletteEntries (d3d9.h)
description: The IDirect3DDevice9::SetPaletteEntries method (d3d9.h) sets palette entries.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetPaletteEntries method","IDirect3DDevice9.SetPaletteEntries","IDirect3DDevice9::SetPaletteEntries","SetPaletteEntries","SetPaletteEntries method [Direct3D 9]","SetPaletteEntries method [Direct3D 9]","IDirect3DDevice9 interface","bc7747ff-8f30-7495-fd87-8a6cb44c173c","d3d9helper/IDirect3DDevice9::SetPaletteEntries","direct3d9.idirect3ddevice9__setpaletteentries"]
old-location: direct3d9\idirect3ddevice9__setpaletteentries.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setpaletteentries.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetPaletteEntries method, IDirect3DDevice9.SetPaletteEntries, IDirect3DDevice9::SetPaletteEntries, SetPaletteEntries, SetPaletteEntries method [Direct3D 9], SetPaletteEntries method [Direct3D 9],IDirect3DDevice9 interface, bc7747ff-8f30-7495-fd87-8a6cb44c173c, d3d9helper/IDirect3DDevice9::SetPaletteEntries, direct3d9.idirect3ddevice9__setpaletteentries
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
 - IDirect3DDevice9::SetPaletteEntries
 - d3d9/IDirect3DDevice9::SetPaletteEntries
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
 - IDirect3DDevice9.SetPaletteEntries
---

# IDirect3DDevice9::SetPaletteEntries


## -description

Sets palette entries.

## -parameters

### -param PaletteNumber [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An ordinal value identifying the particular palette upon which the operation is to be performed.

### -param pEntries [in]

Type: <b>const <a href="/windows/desktop/api/wingdi/ns-wingdi-paletteentry">PALETTEENTRY</a>*</b>

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-paletteentry">PALETTEENTRY</a> structure, representing the palette entries to set. The number of <b>PALETTEENTRY</b> structures pointed to by pEntries is assumed to be 256. See Remarks.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

For Direct3D 9 applications, any palette sent to this method must conform to the D3DPTEXTURECAPS_ALPHAPALETTE capability bit of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure. If D3DPTEXTURECAPS_ALPHAPALETTE is not set, every entry in the palette must have alpha set to 1.0 or this method will fail with D3DERR_INVALIDCALL. If D3DPTEXTURECAPS_ALPHAPALETTE is set, then any set of alpha values are allowed. Note that the debug runtime will print a warning message if all palette entries have alpha set to 0. 

A single logical palette is associated with the device, and is shared by all texture stages.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getcurrenttexturepalette">IDirect3DDevice9::GetCurrentTexturePalette</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpaletteentries">IDirect3DDevice9::GetPaletteEntries</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setcurrenttexturepalette">IDirect3DDevice9::SetCurrentTexturePalette</a>



<a href="/windows/desktop/direct3d9/texture-palettes">Texture Palettes (Direct3D 9)</a>
