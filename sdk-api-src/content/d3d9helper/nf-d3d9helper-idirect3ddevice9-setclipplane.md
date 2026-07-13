---
UID: NF:d3d9helper.IDirect3DDevice9.SetClipPlane
title: IDirect3DDevice9::SetClipPlane (d3d9helper.h)
description: The IDirect3DDevice9::SetClipPlane method (d3d9.h) sets the coefficients of a user-defined clipping plane for the device.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetClipPlane method","IDirect3DDevice9.SetClipPlane","IDirect3DDevice9::SetClipPlane","SetClipPlane","SetClipPlane method [Direct3D 9]","SetClipPlane method [Direct3D 9]","IDirect3DDevice9 interface","b1eeda9e-38a1-4dea-dab6-04754538861d","d3d9helper/IDirect3DDevice9::SetClipPlane","direct3d9.idirect3ddevice9__setclipplane"]
old-location: direct3d9\idirect3ddevice9__setclipplane.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setclipplane.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetClipPlane method, IDirect3DDevice9.SetClipPlane, IDirect3DDevice9::SetClipPlane, SetClipPlane, SetClipPlane method [Direct3D 9], SetClipPlane method [Direct3D 9],IDirect3DDevice9 interface, b1eeda9e-38a1-4dea-dab6-04754538861d, d3d9helper/IDirect3DDevice9::SetClipPlane, direct3d9.idirect3ddevice9__setclipplane
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
 - IDirect3DDevice9::SetClipPlane
 - d3d9helper/IDirect3DDevice9::SetClipPlane
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
 - IDirect3DDevice9.SetClipPlane
---

# IDirect3DDevice9::SetClipPlane


## -description

Sets the coefficients of a user-defined clipping plane for the device.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Index of the clipping plane for which the plane equation coefficients are to be set.

### -param pPlane [in]

Type: <b>const float*</b>

Pointer to an address of a four-element array of values that represent the clipping plane coefficients to be set, in the form of the general plane equation. See Remarks.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value is D3DERR_INVALIDCALL. This error indicates that the value in Index exceeds the maximum clipping plane index supported by the device or that the array at pPlane is not large enough to contain four floating-point values.

## -remarks

The coefficients that this method sets take the form of the general plane equation. If the values in the array at pPlane were labeled A, B, C, and D in the order that they appear in the array, they would fit into the general plane equation so that Ax + By + Cz + Dw = 0. A point with homogeneous coordinates (x, y, z, w) is visible in the half space of the plane if Ax + By + Cz + Dw &gt;= 0. Points that exist behind the clipping plane are clipped from the scene.

When the fixed function pipeline is used the plane equations are assumed to be in world space. When the programmable pipeline is used the plane equations are assumed to be in the clipping space (the same space as output vertices).

This method does not enable the clipping plane equation being set. To enable a clipping plane, set the corresponding bit in the DWORD value applied to the D3DRS_CLIPPLANEENABLE render state.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane">IDirect3DDevice9::GetClipPlane</a>
