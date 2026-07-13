---
UID: NF:d3d9helper.IDirect3DDevice9.SetViewport
title: IDirect3DDevice9::SetViewport (d3d9helper.h)
description: The IDirect3DDevice9::SetViewport method (d3d9helper.h) sets the viewport parameters for the device.
helpviewer_keywords: ["69ed7b86-4dee-fd8c-4647-7e95842d559a","IDirect3DDevice9 interface [Direct3D 9]","SetViewport method","IDirect3DDevice9.SetViewport","IDirect3DDevice9::SetViewport","SetViewport","SetViewport method [Direct3D 9]","SetViewport method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetViewport","direct3d9.idirect3ddevice9__setviewport"]
old-location: direct3d9\idirect3ddevice9__setviewport.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setviewport.htm
ms.date: 08/11/2022
ms.keywords: 69ed7b86-4dee-fd8c-4647-7e95842d559a, IDirect3DDevice9 interface [Direct3D 9],SetViewport method, IDirect3DDevice9.SetViewport, IDirect3DDevice9::SetViewport, SetViewport, SetViewport method [Direct3D 9], SetViewport method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetViewport, direct3d9.idirect3ddevice9__setviewport
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
 - IDirect3DDevice9::SetViewport
 - d3d9helper/IDirect3DDevice9::SetViewport
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
 - IDirect3DDevice9.SetViewport
---

# IDirect3DDevice9::SetViewport


## -description

Sets the viewport parameters for the device.

## -parameters

### -param pViewport [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3dviewport9">D3DVIEWPORT9</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dviewport9">D3DVIEWPORT9</a> structure, specifying the viewport parameters to set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, it will return D3DERR_INVALIDCALL. This will happen if pViewport is invalid, or if pViewport describes a region that cannot exist within the render target surface.

## -remarks

Direct3D sets the following default values for the viewport.




```

D3DVIEWPORT9 vp;
vp.X      = 0;
vp.Y      = 0;
vp.Width  = RenderTarget.Width;
vp.Height = RenderTarget.Height;
vp.MinZ   = 0.0f;
vp.MaxZ   = 1.0f;

```


<b>IDirect3DDevice9::SetViewport</b> can be used to draw on part of the screen. Make sure to call it before any geometry is drawn so the viewport settings will take effect.

To draw multiple views within a scene, repeat the <b>IDirect3DDevice9::SetViewport</b> and draw geometry sequence for each view.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getviewport">IDirect3DDevice9::GetViewport</a>
