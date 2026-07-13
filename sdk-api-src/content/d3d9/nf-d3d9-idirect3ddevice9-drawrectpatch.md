---
UID: NF:d3d9.IDirect3DDevice9.DrawRectPatch
title: IDirect3DDevice9::DrawRectPatch (d3d9.h)
description: The IDirect3DDevice9::DrawRectPatch method (d3d9.h) draws a rectangular patch using the currently set streams.
helpviewer_keywords: ["9f04b48b-012e-3487-432e-10ce6b33782a","DrawRectPatch","DrawRectPatch method [Direct3D 9]","DrawRectPatch method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","DrawRectPatch method","IDirect3DDevice9.DrawRectPatch","IDirect3DDevice9::DrawRectPatch","d3d9helper/IDirect3DDevice9::DrawRectPatch","direct3d9.idirect3ddevice9__drawrectpatch"]
old-location: direct3d9\idirect3ddevice9__drawrectpatch.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawrectpatch.htm
ms.date: 08/10/2022
ms.keywords: 9f04b48b-012e-3487-432e-10ce6b33782a, DrawRectPatch, DrawRectPatch method [Direct3D 9], DrawRectPatch method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawRectPatch method, IDirect3DDevice9.DrawRectPatch, IDirect3DDevice9::DrawRectPatch, d3d9helper/IDirect3DDevice9::DrawRectPatch, direct3d9.idirect3ddevice9__drawrectpatch
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
 - IDirect3DDevice9::DrawRectPatch
 - d3d9/IDirect3DDevice9::DrawRectPatch
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
 - IDirect3DDevice9.DrawRectPatch
---

# IDirect3DDevice9::DrawRectPatch


## -description

Draws a rectangular patch using the currently set streams.

## -parameters

### -param Handle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Handle to the rectangular patch to draw.

### -param pNumSegs [in]

Type: <b>const float*</b>

Pointer to an array of four floating-point values that identify the number of segments each edge of the rectangle patch should be divided into when tessellated. See <a href="/windows/desktop/direct3d9/d3drectpatch-info">D3DRECTPATCH_INFO</a>.

### -param pRectPatchInfo [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3drectpatch-info">D3DRECTPATCH_INFO</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3drectpatch-info">D3DRECTPATCH_INFO</a> structure, describing the rectangular patch to draw.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be 
     D3DERR_INVALIDCALL.

## -remarks

For static patches: Set the vertex shader, set the appropriate streams, supply patch information in the pRectPatchInfo parameter, and specify a handle so that Direct3D can capture and cache information. Call <b>IDirect3DDevice9::DrawRectPatch</b> subsequently with pRectPatchInfo set to <b>NULL</b> to efficiently draw the patch. When drawing a cached patch, the currently set streams are ignored. Override the cached pNumSegs by specifying a new value for pNumSegs. When rendering a cached patch, you must set the same vertex shader that was set when it was captured.

Calling <b>IDirect3DDevice9::DrawRectPatch</b> with a handle invalidates the same handle cached by a previous <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawtripatch">IDirect3DDevice9::DrawTriPatch</a> call.

For dynamic patches, the patch data changes for every rendering of the patch, so it is not efficient to cache information. The application can convey this to Direct3D by setting Handle to 0. In this case, Direct3D draws the patch using the currently set streams and the pNumSegs values, and does not cache any information. It is not valid to simultaneously set Handle to 0 and pRectPatchInfo to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-deletepatch">IDirect3DDevice9::DeletePatch</a>



<a href="/windows/desktop/direct3d9/using-higher-order-primitives">Using Higher-Order Primitives (Direct3D 9)</a>
