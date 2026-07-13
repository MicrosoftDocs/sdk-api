---
UID: NF:d3d9helper.IDirect3DDevice9.GetClipStatus
title: IDirect3DDevice9::GetClipStatus (d3d9helper.h)
description: The IDirect3DDevice9::GetClipStatus method (d3d9.h) retrieves the clip status.
helpviewer_keywords: ["GetClipStatus","GetClipStatus method [Direct3D 9]","GetClipStatus method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetClipStatus method","IDirect3DDevice9.GetClipStatus","IDirect3DDevice9::GetClipStatus","d3d9helper/IDirect3DDevice9::GetClipStatus","df453492-e7c5-c7f3-db0d-498aa59e68b8","direct3d9.idirect3ddevice9__getclipstatus"]
old-location: direct3d9\idirect3ddevice9__getclipstatus.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getclipstatus.htm
ms.date: 08/11/2022
ms.keywords: GetClipStatus, GetClipStatus method [Direct3D 9], GetClipStatus method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetClipStatus method, IDirect3DDevice9.GetClipStatus, IDirect3DDevice9::GetClipStatus, d3d9helper/IDirect3DDevice9::GetClipStatus, df453492-e7c5-c7f3-db0d-498aa59e68b8, direct3d9.idirect3ddevice9__getclipstatus
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
 - IDirect3DDevice9::GetClipStatus
 - d3d9helper/IDirect3DDevice9::GetClipStatus
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
 - IDirect3DDevice9.GetClipStatus
---

# IDirect3DDevice9::GetClipStatus


## -description

Retrieves the clip status.

## -parameters

### -param pClipStatus [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dclipstatus9">D3DCLIPSTATUS9</a>*</b>

 Pointer to a <a href="/windows/desktop/direct3d9/d3dclipstatus9">D3DCLIPSTATUS9</a> structure that describes the clip status.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.


D3DERR_INVALIDCALL is returned if the argument is invalid.

## -remarks

When clipping is enabled during vertex processing (by <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-processvertices">IDirect3DDevice9::ProcessVertices</a>, <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive">IDirect3DDevice9::DrawPrimitive</a>, or other drawing functions), Direct3D computes a clip code for every vertex. The clip code is a combination of D3DCS_* bits. When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code. Direct3D maintains the clip status using <a href="/windows/desktop/direct3d9/d3dclipstatus9">D3DCLIPSTATUS9</a>, which has ClipUnion and ClipIntersection members. ClipUnion is a bitwise "OR" of all vertex clip codes and ClipIntersection is a bitwise "AND" of all vertex clip codes. Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection. When D3DRS_CLIPPING is set to <b>FALSE</b>, ClipUnion and ClipIntersection are set to zero. Direct3D updates the clip status during drawing calls. To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.

Clip status is not updated by <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawrectpatch">IDirect3DDevice9::DrawRectPatch</a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawtripatch">IDirect3DDevice9::DrawTriPatch</a> because there is no software emulation for them.

Clip status is used during software vertex processing. Therefore, this method is not supported on pure or nonpure hardware processing devices. For more information about pure devices, see <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipstatus">IDirect3DDevice9::SetClipStatus</a>
