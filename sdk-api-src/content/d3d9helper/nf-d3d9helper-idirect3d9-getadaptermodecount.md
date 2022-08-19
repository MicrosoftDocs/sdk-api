---
UID: NF:d3d9helper.IDirect3D9.GetAdapterModeCount
title: IDirect3D9::GetAdapterModeCount (d3d9helper.h)
description: The IDirect3D9::GetAdapterModeCount (d3d9helper.h) method returns the number of display modes available on this adapter.
helpviewer_keywords: ["8c15b401-a18e-3d6f-8b01-fd6833879d87","GetAdapterModeCount","GetAdapterModeCount method [Direct3D 9]","GetAdapterModeCount method [Direct3D 9]","IDirect3D9 interface","IDirect3D9 interface [Direct3D 9]","GetAdapterModeCount method","IDirect3D9.GetAdapterModeCount","IDirect3D9::GetAdapterModeCount","d3d9helper/IDirect3D9::GetAdapterModeCount","direct3d9.idirect3d9__getadaptermodecount"]
old-location: direct3d9\idirect3d9__getadaptermodecount.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__getadaptermodecount.htm
ms.date: 08/11/2022
ms.keywords: 8c15b401-a18e-3d6f-8b01-fd6833879d87, GetAdapterModeCount, GetAdapterModeCount method [Direct3D 9], GetAdapterModeCount method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],GetAdapterModeCount method, IDirect3D9.GetAdapterModeCount, IDirect3D9::GetAdapterModeCount, d3d9helper/IDirect3D9::GetAdapterModeCount, direct3d9.idirect3d9__getadaptermodecount
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
 - IDirect3D9::GetAdapterModeCount
 - d3d9helper/IDirect3D9::GetAdapterModeCount
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
 - IDirect3D9.GetAdapterModeCount
---

# IDirect3D9::GetAdapterModeCount


## -description

Returns the number of display modes available on this adapter.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number that denotes the display adapter. D3DADAPTER_DEFAULT is always the primary display adapter.

### -param Format [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Identifies the format of the surface type using <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>. Use <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes">EnumAdapterModes</a> to see the valid formats.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

This method returns the number of display modes on this adapter or zero if Adapter is greater than or equal to the number of adapters on the system.

## -see-also

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes">EnumAdapterModes</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>
