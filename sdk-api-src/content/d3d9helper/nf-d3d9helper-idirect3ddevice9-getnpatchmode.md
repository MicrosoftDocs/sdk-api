---
UID: NF:d3d9helper.IDirect3DDevice9.GetNPatchMode
title: IDirect3DDevice9::GetNPatchMode (d3d9helper.h)
description: The IDirect3DDevice9::GetNPatchMode method (d3d9.h) gets the N-patch mode segments.
helpviewer_keywords: ["GetNPatchMode","GetNPatchMode method [Direct3D 9]","GetNPatchMode method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetNPatchMode method","IDirect3DDevice9.GetNPatchMode","IDirect3DDevice9::GetNPatchMode","a14b100f-853a-c4a3-4c40-bb1bf093d57c","d3d9helper/IDirect3DDevice9::GetNPatchMode","direct3d9.idirect3ddevice9__getnpatchmode"]
old-location: direct3d9\idirect3ddevice9__getnpatchmode.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getnpatchmode.htm
ms.date: 08/11/2022
ms.keywords: GetNPatchMode, GetNPatchMode method [Direct3D 9], GetNPatchMode method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetNPatchMode method, IDirect3DDevice9.GetNPatchMode, IDirect3DDevice9::GetNPatchMode, a14b100f-853a-c4a3-4c40-bb1bf093d57c, d3d9helper/IDirect3DDevice9::GetNPatchMode, direct3d9.idirect3ddevice9__getnpatchmode
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
 - IDirect3DDevice9::GetNPatchMode
 - d3d9helper/IDirect3DDevice9::GetNPatchMode
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
 - IDirect3DDevice9.GetNPatchMode
---

# IDirect3DDevice9::GetNPatchMode


## -description

Gets the N-patch mode segments.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Specifies the number of subdivision segments. If the number of segments is less than 1.0, N-patches are disabled. The default value is 0.0.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode">IDirect3DDevice9::SetNPatchMode</a>
