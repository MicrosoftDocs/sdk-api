---
UID: NF:d3d9.IDirect3D9Ex.EnumAdapterModesEx
title: IDirect3D9Ex::EnumAdapterModesEx (d3d9.h)
description: This method returns the actual display mode info based on the given mode index.
helpviewer_keywords: ["4bc3b89a-9f5a-0632-2b67-102fd92c5053","EnumAdapterModesEx","EnumAdapterModesEx method [Direct3D 9]","EnumAdapterModesEx method [Direct3D 9]","IDirect3D9Ex interface","IDirect3D9Ex interface [Direct3D 9]","EnumAdapterModesEx method","IDirect3D9Ex.EnumAdapterModesEx","IDirect3D9Ex::EnumAdapterModesEx","d3d9/IDirect3D9Ex::EnumAdapterModesEx","direct3d9.idirect3d9ex_enumadaptermodesex"]
old-location: direct3d9\idirect3d9ex_enumadaptermodesex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_enumadaptermodesex.htm
ms.date: 12/05/2018
ms.keywords: 4bc3b89a-9f5a-0632-2b67-102fd92c5053, EnumAdapterModesEx, EnumAdapterModesEx method [Direct3D 9], EnumAdapterModesEx method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],EnumAdapterModesEx method, IDirect3D9Ex.EnumAdapterModesEx, IDirect3D9Ex::EnumAdapterModesEx, d3d9/IDirect3D9Ex::EnumAdapterModesEx, direct3d9.idirect3d9ex_enumadaptermodesex
req.header: d3d9.h
req.include-header: 
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
 - IDirect3D9Ex::EnumAdapterModesEx
 - d3d9/IDirect3D9Ex::EnumAdapterModesEx
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
 - IDirect3D9Ex.EnumAdapterModesEx
---

# IDirect3D9Ex::EnumAdapterModesEx


## -description

This method returns the actual display mode info based on the given mode index.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number denoting the display adapter to enumerate. D3DADAPTER_DEFAULT is always the primary display adapter. This method returns D3DERR_INVALIDCALL when this value equals or exceeds the number of display adapters in the system.

### -param pFilter [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3ddisplaymodefilter">D3DDISPLAYMODEFILTER</a>*</b>

See <a href="/windows/desktop/direct3d9/d3ddisplaymodefilter">D3DDISPLAYMODEFILTER</a>.

### -param Mode [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Represents the display-mode index which is an unsigned integer between zero and the value returned by GetAdapterModeCount minus one.

### -param pMode [out, retval]

Type: <b><a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a>*</b>

A pointer to the available display mode of type <a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

<ul>
<li>If the device can be used on this adapter, D3D_OK is returned.</li>
<li>If the Adapter equals or exceeds the number of display adapters in the system, D3DERR_INVALIDCALL is returned.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a>