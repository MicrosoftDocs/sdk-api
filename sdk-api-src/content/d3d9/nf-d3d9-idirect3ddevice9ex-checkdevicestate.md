---
UID: NF:d3d9.IDirect3DDevice9Ex.CheckDeviceState
title: IDirect3DDevice9Ex::CheckDeviceState (d3d9.h)
description: Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application. (IDirect3DDevice9Ex.CheckDeviceState)
helpviewer_keywords: ["7c555cdc-567a-be2d-d677-3b3df3746e0b","CheckDeviceState","CheckDeviceState method [Direct3D 9]","CheckDeviceState method [Direct3D 9]","IDirect3DDevice9Ex interface","IDirect3DDevice9Ex interface [Direct3D 9]","CheckDeviceState method","IDirect3DDevice9Ex.CheckDeviceState","IDirect3DDevice9Ex::CheckDeviceState","d3d9/IDirect3DDevice9Ex::CheckDeviceState","direct3d9.idirect3ddevice9ex_checkdevicestate"]
old-location: direct3d9\idirect3ddevice9ex_checkdevicestate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_checkdevicestate.htm
ms.date: 12/05/2018
ms.keywords: 7c555cdc-567a-be2d-d677-3b3df3746e0b, CheckDeviceState, CheckDeviceState method [Direct3D 9], CheckDeviceState method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],CheckDeviceState method, IDirect3DDevice9Ex.CheckDeviceState, IDirect3DDevice9Ex::CheckDeviceState, d3d9/IDirect3DDevice9Ex::CheckDeviceState, direct3d9.idirect3ddevice9ex_checkdevicestate
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
 - IDirect3DDevice9Ex::CheckDeviceState
 - d3d9/IDirect3DDevice9Ex::CheckDeviceState
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
 - IDirect3DDevice9Ex.CheckDeviceState
---

# IDirect3DDevice9Ex::CheckDeviceState


## -description

Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.

## -parameters

### -param hDestinationWindow [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The destination window handle to check for occlusion. When this parameter is <b>NULL</b>, S_PRESENT_OCCLUDED is returned when another device has fullscreen ownership. When the window handle is not <b>NULL</b>, window's client area is checked for occlusion. A window is occluded if any part of it is obscured by another application.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Possible return values include: D3D_OK, D3DERR_DEVICELOST, D3DERR_DEVICEHUNG, D3DERR_DEVICEREMOVED, or D3DERR_OUTOFVIDEOMEMORY (see <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a>), or S_PRESENT_MODE_CHANGED, or S_PRESENT_OCCLUDED (see <a href="/windows/desktop/direct3d9/device-state-return-codes">S_PRESENT</a>).

## -remarks

This method replaces <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel">IDirect3DDevice9::TestCooperativeLevel</a>, which always returns S_OK in Direct3D 9Ex applications.

We recommend not to call <b>CheckDeviceState</b> every frame. Instead, call <b>CheckDeviceState</b> only if the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex">IDirect3DDevice9Ex::PresentEx</a> method returns a failure code.

See <a href="/windows/desktop/direct3d9/dx9lh">Lost Device Behavior Changes</a> for more information about lost, hung, and removed devices.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>
