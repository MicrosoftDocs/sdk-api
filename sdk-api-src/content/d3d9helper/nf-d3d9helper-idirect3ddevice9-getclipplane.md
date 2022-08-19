---
UID: NF:d3d9helper.IDirect3DDevice9.GetClipPlane
title: IDirect3DDevice9::GetClipPlane (d3d9helper.h)
description: The IDirect3DDevice9::GetClipPlane method (d3d9.h) retrieves the coefficients of a user-defined clipping plane for the device.
helpviewer_keywords: ["4ee4abff-6964-013c-ead5-e1d4da1fe84b","GetClipPlane","GetClipPlane method [Direct3D 9]","GetClipPlane method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetClipPlane method","IDirect3DDevice9.GetClipPlane","IDirect3DDevice9::GetClipPlane","d3d9helper/IDirect3DDevice9::GetClipPlane","direct3d9.idirect3ddevice9__getclipplane"]
old-location: direct3d9\idirect3ddevice9__getclipplane.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getclipplane.htm
ms.date: 08/11/2022
ms.keywords: 4ee4abff-6964-013c-ead5-e1d4da1fe84b, GetClipPlane, GetClipPlane method [Direct3D 9], GetClipPlane method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetClipPlane method, IDirect3DDevice9.GetClipPlane, IDirect3DDevice9::GetClipPlane, d3d9helper/IDirect3DDevice9::GetClipPlane, direct3d9.idirect3ddevice9__getclipplane
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
 - IDirect3DDevice9::GetClipPlane
 - d3d9helper/IDirect3DDevice9::GetClipPlane
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
 - IDirect3DDevice9.GetClipPlane
---

# IDirect3DDevice9::GetClipPlane


## -description

Retrieves the coefficients of a user-defined clipping plane for the device.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Index of the clipping plane for which the plane equation coefficients are retrieved.

### -param pPlane [out]

Type: <b>float*</b>

Pointer to a four-element array of values that represent the coefficients of the clipping plane in the form of the general plane equation. See Remarks.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value is D3DERR_INVALIDCALL. This error indicates that the value in Index exceeds the maximum clipping plane index supported by the device, or that the array at pPlane is not large enough to contain four floating-point values.

## -remarks

This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other values in <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>."
    


The coefficients that this method reports take the form of the general plane equation. If the values in the array at pPlane were labeled A, B, C, and D in the order that they appear in the array, they would fit into the general plane equation so that Ax + By + Cz + Dw = 0. A point with homogeneous coordinates (x, y, z, w) is visible in the half space of the plane if Ax + By + Cz + Dw &gt;= 0. Points that exist on or behind the clipping plane are clipped from the scene.

The plane equation used by this method exists in world space and is set by a previous call to the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane">IDirect3DDevice9::SetClipPlane</a> method.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane">IDirect3DDevice9::SetClipPlane</a>
