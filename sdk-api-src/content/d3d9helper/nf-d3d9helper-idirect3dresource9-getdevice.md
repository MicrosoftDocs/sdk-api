---
UID: NF:d3d9helper.IDirect3DResource9.GetDevice
title: IDirect3DResource9::GetDevice (d3d9helper.h)
description: The IDirect3DResource9::GetDevice method (d3d9helper.h) retrieves the device associated with a resource.
helpviewer_keywords: ["3bf4048b-2238-43f9-bea2-116b8dc8df09","GetDevice","GetDevice method [Direct3D 9]","GetDevice method [Direct3D 9]","IDirect3DResource9 interface","IDirect3DResource9 interface [Direct3D 9]","GetDevice method","IDirect3DResource9.GetDevice","IDirect3DResource9::GetDevice","d3d9helper/IDirect3DResource9::GetDevice","direct3d9.idirect3dresource9__getdevice"]
old-location: direct3d9\idirect3dresource9__getdevice.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__getdevice.htm
ms.date: 08/11/2022
ms.keywords: 3bf4048b-2238-43f9-bea2-116b8dc8df09, GetDevice, GetDevice method [Direct3D 9], GetDevice method [Direct3D 9],IDirect3DResource9 interface, IDirect3DResource9 interface [Direct3D 9],GetDevice method, IDirect3DResource9.GetDevice, IDirect3DResource9::GetDevice, d3d9helper/IDirect3DResource9::GetDevice, direct3d9.idirect3dresource9__getdevice
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
 - IDirect3DResource9::GetDevice
 - d3d9helper/IDirect3DResource9::GetDevice
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
 - IDirect3DResource9.GetDevice
---

# IDirect3DResource9::GetDevice


## -description

Retrieves the device associated with a resource.

## -parameters

### -param ppDevice [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface to fill with the device pointer, if the query succeeds.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

This method allows navigation to the owning device object.

Calling this method will increase the internal reference count on the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface. Failure to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DDevice9</b> interface results in a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>
