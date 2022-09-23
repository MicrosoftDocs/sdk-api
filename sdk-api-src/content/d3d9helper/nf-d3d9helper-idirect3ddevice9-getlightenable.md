---
UID: NF:d3d9helper.IDirect3DDevice9.GetLightEnable
title: IDirect3DDevice9::GetLightEnable (d3d9helper.h)
description: The IDirect3DDevice9::GetLightEnable method (d3d9.h) retrieves the activity status of enabled or disabled, for a set of lighting parameters within a device.
helpviewer_keywords: ["2d73c9f9-8cdd-b499-9dc6-930ac19d6977","GetLightEnable","GetLightEnable method [Direct3D 9]","GetLightEnable method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetLightEnable method","IDirect3DDevice9.GetLightEnable","IDirect3DDevice9::GetLightEnable","d3d9helper/IDirect3DDevice9::GetLightEnable","direct3d9.idirect3ddevice9__getlightenable"]
old-location: direct3d9\idirect3ddevice9__getlightenable.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getlightenable.htm
ms.date: 08/11/2022
ms.keywords: 2d73c9f9-8cdd-b499-9dc6-930ac19d6977, GetLightEnable, GetLightEnable method [Direct3D 9], GetLightEnable method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetLightEnable method, IDirect3DDevice9.GetLightEnable, IDirect3DDevice9::GetLightEnable, d3d9helper/IDirect3DDevice9::GetLightEnable, direct3d9.idirect3ddevice9__getlightenable
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
 - IDirect3DDevice9::GetLightEnable
 - d3d9helper/IDirect3DDevice9::GetLightEnable
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
 - IDirect3DDevice9.GetLightEnable
---

# IDirect3DDevice9::GetLightEnable


## -description

Retrieves the activity status - enabled or disabled - for a set of lighting parameters within a device.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Zero-based index of the set of lighting parameters that are the target of this method.

### -param pEnable [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Pointer to a variable to fill with the status of the specified lighting parameters. After the call, a nonzero value at this address indicates that the specified lighting parameters are enabled; a value of 0 indicates that they are disabled.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other values in <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlight">IDirect3DDevice9::GetLight</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-lightenable">IDirect3DDevice9::LightEnable</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight">IDirect3DDevice9::SetLight</a>
