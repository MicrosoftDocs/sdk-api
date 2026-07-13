---
UID: NF:d3d9.IDirect3D9.GetDeviceCaps
title: IDirect3D9::GetDeviceCaps (d3d9.h)
description: The IDirect3D9::GetDeviceCaps method (d3d9.h) retrieves device-specific information about a device.
helpviewer_keywords: ["87e98d3f-7bf9-d2ba-4731-1b08cb375732","GetDeviceCaps","GetDeviceCaps method [Direct3D 9]","GetDeviceCaps method [Direct3D 9]","IDirect3D9 interface","IDirect3D9 interface [Direct3D 9]","GetDeviceCaps method","IDirect3D9.GetDeviceCaps","IDirect3D9::GetDeviceCaps","d3d9helper/IDirect3D9::GetDeviceCaps","direct3d9.idirect3d9__getdevicecaps"]
old-location: direct3d9\idirect3d9__getdevicecaps.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__getdevicecaps.htm
ms.date: 08/10/2022
ms.keywords: 87e98d3f-7bf9-d2ba-4731-1b08cb375732, GetDeviceCaps, GetDeviceCaps method [Direct3D 9], GetDeviceCaps method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],GetDeviceCaps method, IDirect3D9.GetDeviceCaps, IDirect3D9::GetDeviceCaps, d3d9helper/IDirect3D9::GetDeviceCaps, direct3d9.idirect3d9__getdevicecaps
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
 - IDirect3D9::GetDeviceCaps
 - d3d9/IDirect3D9::GetDeviceCaps
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
 - IDirect3D9.GetDeviceCaps
---

# IDirect3D9::GetDeviceCaps


## -description

Retrieves device-specific information about a device.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number that denotes the display adapter. D3DADAPTER_DEFAULT is always the primary display adapter.

### -param DeviceType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a> enumerated type. Denotes the device type.

### -param pCaps [out]

Type: <b><a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure to be filled with information describing the capabilities of the device.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_INVALIDDEVICE, D3DERR_OUTOFVIDEOMEMORY, and D3DERR_NOTAVAILABLE.

## -remarks

The application should not assume the persistence of vertex processing capabilities across Direct3D device objects. The particular capabilities that a physical device exposes may depend on parameters supplied to <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">CreateDevice</a>. For example, the capabilities may yield different vertex processing capabilities before and after creating a Direct3D Device Object with hardware vertex processing enabled. For more information see the description of <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>
