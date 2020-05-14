---
UID: NF:d3d9.IDirect3DDevice9.SetScissorRect
title: IDirect3DDevice9::SetScissorRect (d3d9.h)
description: Sets the scissor rectangle.helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetScissorRect method","IDirect3DDevice9.SetScissorRect","IDirect3DDevice9::SetScissorRect","SetScissorRect","SetScissorRect method [Direct3D 9]","SetScissorRect method [Direct3D 9]","IDirect3DDevice9 interface","c088567d-a486-1e7d-7863-886a85f0ecbb","d3d9helper/IDirect3DDevice9::SetScissorRect","direct3d9.idirect3ddevice9__setscissorrect"]
old-location: direct3d9\idirect3ddevice9__setscissorrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setscissorrect.htm
ms.date: 12/05/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetScissorRect method, IDirect3DDevice9.SetScissorRect, IDirect3DDevice9::SetScissorRect, SetScissorRect, SetScissorRect method [Direct3D 9], SetScissorRect method [Direct3D 9],IDirect3DDevice9 interface, c088567d-a486-1e7d-7863-886a85f0ecbb, d3d9helper/IDirect3DDevice9::SetScissorRect, direct3d9.idirect3ddevice9__setscissorrect
f1_keywords:
- d3d9/IDirect3DDevice9.SetScissorRect
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D9.lib
- D3D9.dll
api_name:
- IDirect3DDevice9.SetScissorRect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9::SetScissorRect


## -description


Sets the scissor rectangle.


## -parameters




### -param pRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that defines the rendering area within the render target if scissor test is enabled. This parameter may not be <b>NULL</b>.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -remarks



The scissor rectangle is used as a rectangular clipping region.

See <a href="https://docs.microsoft.com/windows/desktop/direct3d9/rectangles">Rectangles (Direct3D 9)</a> for further information on the use of rectangles in DirectX.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
 

 

