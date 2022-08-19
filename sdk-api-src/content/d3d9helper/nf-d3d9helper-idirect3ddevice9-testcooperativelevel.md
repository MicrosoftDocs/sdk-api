---
UID: NF:d3d9helper.IDirect3DDevice9.TestCooperativeLevel
title: IDirect3DDevice9::TestCooperativeLevel (d3d9helper.h)
description: The IDirect3DDevice9::TestCooperativeLevel method (d3d9helper.h) reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.
helpviewer_keywords: ["613a6a7b-3b6f-b565-1f3a-2b5322844deb","IDirect3DDevice9 interface [Direct3D 9]","TestCooperativeLevel method","IDirect3DDevice9.TestCooperativeLevel","IDirect3DDevice9::TestCooperativeLevel","TestCooperativeLevel","TestCooperativeLevel method [Direct3D 9]","TestCooperativeLevel method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::TestCooperativeLevel","direct3d9.idirect3ddevice9__testcooperativelevel"]
old-location: direct3d9\idirect3ddevice9__testcooperativelevel.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__testcooperativelevel.htm
ms.date: 08/11/2022
ms.keywords: 613a6a7b-3b6f-b565-1f3a-2b5322844deb, IDirect3DDevice9 interface [Direct3D 9],TestCooperativeLevel method, IDirect3DDevice9.TestCooperativeLevel, IDirect3DDevice9::TestCooperativeLevel, TestCooperativeLevel, TestCooperativeLevel method [Direct3D 9], TestCooperativeLevel method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::TestCooperativeLevel, direct3d9.idirect3ddevice9__testcooperativelevel
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
 - IDirect3DDevice9::TestCooperativeLevel
 - d3d9helper/IDirect3DDevice9::TestCooperativeLevel
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
 - IDirect3DDevice9.TestCooperativeLevel
---

# IDirect3DDevice9::TestCooperativeLevel


## -description

Reports the current cooperative-level status of the Direct3D device for a windowed or full-screen application.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK, indicating that the device is operational and the calling application can continue.
 If the method fails, the return value can be one of the following values: D3DERR_DEVICELOST, D3DERR_DEVICENOTRESET, D3DERR_DRIVERINTERNALERROR.

## -remarks

If the device is lost but cannot be restored at the current time, <b>IDirect3DDevice9::TestCooperativeLevel</b> returns the D3DERR_DEVICELOST return code. This would be the case, for example, when a full-screen device has lost focus. If an application detects a lost device, it should pause and periodically call <b>IDirect3DDevice9::TestCooperativeLevel</b> until it receives a return value of D3DERR_DEVICENOTRESET. The application may then attempt to reset the device by calling <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-reset">IDirect3DDevice9::Reset</a> and, if this succeeds, restore the necessary resources and resume normal operation. Note that <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">IDirect3DDevice9::Present</a> will return D3DERR_DEVICELOST if the device is either "lost" or "not reset".

A call to <b>IDirect3DDevice9::TestCooperativeLevel</b> will fail if called on a different thread than that used to create the device being reset.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
