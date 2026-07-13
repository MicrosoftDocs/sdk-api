---
UID: NF:d3d9.IDirect3DDevice9.GetRenderState
title: IDirect3DDevice9::GetRenderState (d3d9.h)
description: The IDirect3DDevice9::GetRenderState method (d3d9.h) retrieves a render-state value for a device.
helpviewer_keywords: ["2d20be3d-5ba4-bf91-6270-0a3b1c346d9d","GetRenderState","GetRenderState method [Direct3D 9]","GetRenderState method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetRenderState method","IDirect3DDevice9.GetRenderState","IDirect3DDevice9::GetRenderState","d3d9helper/IDirect3DDevice9::GetRenderState","direct3d9.idirect3ddevice9__getrenderstate"]
old-location: direct3d9\idirect3ddevice9__getrenderstate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getrenderstate.htm
ms.date: 08/10/2022
ms.keywords: 2d20be3d-5ba4-bf91-6270-0a3b1c346d9d, GetRenderState, GetRenderState method [Direct3D 9], GetRenderState method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetRenderState method, IDirect3DDevice9.GetRenderState, IDirect3DDevice9::GetRenderState, d3d9helper/IDirect3DDevice9::GetRenderState, direct3d9.idirect3ddevice9__getrenderstate
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
 - IDirect3DDevice9::GetRenderState
 - d3d9/IDirect3DDevice9::GetRenderState
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
 - IDirect3DDevice9.GetRenderState
---

# IDirect3DDevice9::GetRenderState


## -description

Retrieves a render-state value for a device.

## -parameters

### -param State [in]

Type: <b><a href="/windows/desktop/direct3d9/d3drenderstatetype">D3DRENDERSTATETYPE</a></b>

Device state variable that is being queried. This parameter can be any member of the <a href="/windows/desktop/direct3d9/d3drenderstatetype">D3DRENDERSTATETYPE</a> enumerated type.

### -param pValue [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Pointer to a variable that receives the value of the queried render state variable when the method returns.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if one of the arguments is invalid.

## -remarks

This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other values in <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>."

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate">IDirect3DDevice9::SetRenderState</a>
