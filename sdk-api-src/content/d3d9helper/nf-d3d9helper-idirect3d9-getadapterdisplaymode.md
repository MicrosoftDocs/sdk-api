---
UID: NF:d3d9helper.IDirect3D9.GetAdapterDisplayMode
title: IDirect3D9::GetAdapterDisplayMode (d3d9helper.h)
description: The IDirect3D9::GetAdapterDisplayMode (d3d9helper.h) method retrieves the current display mode of the adapter.
helpviewer_keywords: ["GetAdapterDisplayMode","GetAdapterDisplayMode method [Direct3D 9]","GetAdapterDisplayMode method [Direct3D 9]","IDirect3D9 interface","IDirect3D9 interface [Direct3D 9]","GetAdapterDisplayMode method","IDirect3D9.GetAdapterDisplayMode","IDirect3D9::GetAdapterDisplayMode","a03b5255-0046-403d-b90f-e76191710598","d3d9helper/IDirect3D9::GetAdapterDisplayMode","direct3d9.idirect3d9__getadapterdisplaymode"]
old-location: direct3d9\idirect3d9__getadapterdisplaymode.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__getadapterdisplaymode.htm
ms.date: 08/11/2022
ms.keywords: GetAdapterDisplayMode, GetAdapterDisplayMode method [Direct3D 9], GetAdapterDisplayMode method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],GetAdapterDisplayMode method, IDirect3D9.GetAdapterDisplayMode, IDirect3D9::GetAdapterDisplayMode, a03b5255-0046-403d-b90f-e76191710598, d3d9helper/IDirect3D9::GetAdapterDisplayMode, direct3d9.idirect3d9__getadapterdisplaymode
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
 - IDirect3D9::GetAdapterDisplayMode
 - d3d9helper/IDirect3D9::GetAdapterDisplayMode
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
 - IDirect3D9.GetAdapterDisplayMode
---

# IDirect3D9::GetAdapterDisplayMode


## -description

Retrieves the current display mode of the adapter.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number that denotes the display adapter to query. D3DADAPTER_DEFAULT is always the primary display adapter.

### -param pMode [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3ddisplaymode">D3DDISPLAYMODE</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3ddisplaymode">D3DDISPLAYMODE</a> structure, to be filled with information describing the current adapter's mode.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. 



If Adapter is out of range or pMode is invalid, this method returns D3DERR_INVALIDCALL.

## -remarks

<b>GetAdapterDisplayMode</b> will not return the correct format when the display is in an extended format, such as 2:10:10:10. Instead, it returns the format X8R8G8B8.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>
