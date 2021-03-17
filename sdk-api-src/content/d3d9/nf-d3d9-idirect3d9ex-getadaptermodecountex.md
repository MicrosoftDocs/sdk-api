---
UID: NF:d3d9.IDirect3D9Ex.GetAdapterModeCountEx
title: IDirect3D9Ex::GetAdapterModeCountEx (d3d9.h)
description: Returns the number of display modes available.
helpviewer_keywords: ["GetAdapterModeCountEx","GetAdapterModeCountEx method [Direct3D 9]","GetAdapterModeCountEx method [Direct3D 9]","IDirect3D9Ex interface","IDirect3D9Ex interface [Direct3D 9]","GetAdapterModeCountEx method","IDirect3D9Ex.GetAdapterModeCountEx","IDirect3D9Ex::GetAdapterModeCountEx","b588ce9d-6d83-1841-d193-8ee55c13af53","d3d9/IDirect3D9Ex::GetAdapterModeCountEx","direct3d9.idirect3d9ex_getadaptermodecountex"]
old-location: direct3d9\idirect3d9ex_getadaptermodecountex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_getadaptermodecountex.htm
ms.date: 12/05/2018
ms.keywords: GetAdapterModeCountEx, GetAdapterModeCountEx method [Direct3D 9], GetAdapterModeCountEx method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],GetAdapterModeCountEx method, IDirect3D9Ex.GetAdapterModeCountEx, IDirect3D9Ex::GetAdapterModeCountEx, b588ce9d-6d83-1841-d193-8ee55c13af53, d3d9/IDirect3D9Ex::GetAdapterModeCountEx, direct3d9.idirect3d9ex_getadaptermodecountex
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
 - IDirect3D9Ex::GetAdapterModeCountEx
 - d3d9/IDirect3D9Ex::GetAdapterModeCountEx
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
 - IDirect3D9Ex.GetAdapterModeCountEx
---

# IDirect3D9Ex::GetAdapterModeCountEx


## -description

Returns the number of display modes available.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number denoting the display adapter from which to retrieve the display mode count.

### -param pFilter [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3ddisplaymodefilter">D3DDISPLAYMODEFILTER</a>*</b>

Specifies the characteristics of the desired display mode. See <a href="/windows/desktop/direct3d9/d3ddisplaymodefilter">D3DDISPLAYMODEFILTER</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of display modes available. A return of value zero from this method is an indication that no such display mode is supported or simply this monitor is no longer available.

## -remarks

Events such as display mode changes on other heads of the same hardware, monitor change or its connection status change, and desktop extension/unextension could all affect the number of display mode available.

To fullscreen applications, S_PRESENT_MODE_CHANGED returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex">PresentEx</a> or <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate">CheckDeviceState</a> is the indication of display mode setting failure due to those events.

To increase the chance of setting a currently available display mode successfully, fullscreen applications should try to requery the available display mode list upon receiving S_PRESENT_MODE_CHANGED.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a>