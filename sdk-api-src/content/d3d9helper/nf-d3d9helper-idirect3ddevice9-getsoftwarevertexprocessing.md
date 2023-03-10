---
UID: NF:d3d9helper.IDirect3DDevice9.GetSoftwareVertexProcessing
title: IDirect3DDevice9::GetSoftwareVertexProcessing (d3d9helper.h)
description: the IDirect3DDevice9::GetSoftwareVertexProcessing method (d3d9.h) gets the vertex hardware or software processing mode. 
helpviewer_keywords: ["17efcf07-7357-cfad-13db-c6391873f457","GetSoftwareVertexProcessing","GetSoftwareVertexProcessing method [Direct3D 9]","GetSoftwareVertexProcessing method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetSoftwareVertexProcessing method","IDirect3DDevice9.GetSoftwareVertexProcessing","IDirect3DDevice9::GetSoftwareVertexProcessing","d3d9helper/IDirect3DDevice9::GetSoftwareVertexProcessing","direct3d9.idirect3ddevice9__getsoftwarevertexprocessing"]
old-location: direct3d9\idirect3ddevice9__getsoftwarevertexprocessing.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getsoftwarevertexprocessing.htm
ms.date: 08/11/2022
ms.keywords: 17efcf07-7357-cfad-13db-c6391873f457, GetSoftwareVertexProcessing, GetSoftwareVertexProcessing method [Direct3D 9], GetSoftwareVertexProcessing method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetSoftwareVertexProcessing method, IDirect3DDevice9.GetSoftwareVertexProcessing, IDirect3DDevice9::GetSoftwareVertexProcessing, d3d9helper/IDirect3DDevice9::GetSoftwareVertexProcessing, direct3d9.idirect3ddevice9__getsoftwarevertexprocessing
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
 - IDirect3DDevice9::GetSoftwareVertexProcessing
 - d3d9helper/IDirect3DDevice9::GetSoftwareVertexProcessing
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
 - IDirect3DDevice9.GetSoftwareVertexProcessing
---

# IDirect3DDevice9::GetSoftwareVertexProcessing


## -description

Gets the vertex processing (hardware or software) mode.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if software vertex processing is set. Otherwise, it returns <b>FALSE</b>.

## -remarks

An application can create a mixed-mode device to use both the software vertex processing and the hardware vertex processing. To switch between the two vertex processing modes in DirectX 8.x, use <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate">IDirect3DDevice9::SetRenderState</a> with the render state D3DRS_SOFTWAREVERTEXPROCESSING and the appropriate BOOL argument. The drawback of the render state approach was the difficulty in defining the semantics for state blocks. Applications and the runtime had to do extra work and be careful while recording and playing back state blocks.

In Direct3D 9, use <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing">IDirect3DDevice9::SetSoftwareVertexProcessing</a> instead. This new API is not recorded by StateBlocks.

 Also refer to the notes for the <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a> constants.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
