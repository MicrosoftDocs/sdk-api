---
UID: NF:d3d9helper.IDirect3DDevice9.GetStreamSourceFreq
title: IDirect3DDevice9::GetStreamSourceFreq (d3d9helper.h)
description: The IDirect3DDevice9::GetStreamSourceFreq method (d3d9.h) gets the stream source frequency divider value.
helpviewer_keywords: ["5a7d1b69-c1ef-f38d-2536-b01c718bd9b6","GetStreamSourceFreq","GetStreamSourceFreq method [Direct3D 9]","GetStreamSourceFreq method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetStreamSourceFreq method","IDirect3DDevice9.GetStreamSourceFreq","IDirect3DDevice9::GetStreamSourceFreq","d3d9helper/IDirect3DDevice9::GetStreamSourceFreq","direct3d9.idirect3ddevice9__getstreamsourcefreq"]
old-location: direct3d9\idirect3ddevice9__getstreamsourcefreq.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getstreamsourcefreq.htm
ms.date: 08/11/2022
ms.keywords: 5a7d1b69-c1ef-f38d-2536-b01c718bd9b6, GetStreamSourceFreq, GetStreamSourceFreq method [Direct3D 9], GetStreamSourceFreq method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetStreamSourceFreq method, IDirect3DDevice9.GetStreamSourceFreq, IDirect3DDevice9::GetStreamSourceFreq, d3d9helper/IDirect3DDevice9::GetStreamSourceFreq, direct3d9.idirect3ddevice9__getstreamsourcefreq
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
 - IDirect3DDevice9::GetStreamSourceFreq
 - d3d9helper/IDirect3DDevice9::GetStreamSourceFreq
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
 - IDirect3DDevice9.GetStreamSourceFreq
---

## -description

Gets the stream source frequency divider value.

## -parameters

### -param StreamNumber

Type: [in] <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Stream source number.

### -param Divider

Type: [out] <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Returns the frequency divider value.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

Vertex shaders can now be invoked more than once per vertex. See <a href="/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry">Drawing Non-Indexed Geometry</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>

<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq">IDirect3DDevice9::SetStreamSourceFreq</a>
