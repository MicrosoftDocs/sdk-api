---
UID: NF:d3d9helper.IDirect3DDevice9.SetSoftwareVertexProcessing
title: IDirect3DDevice9::SetSoftwareVertexProcessing (d3d9helper.h)
description: The IDirect3DDevice9::SetSoftwareVertexProcessing method (d3d9helper.h) switches between software and hardware vertex processing.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetSoftwareVertexProcessing method","IDirect3DDevice9.SetSoftwareVertexProcessing","IDirect3DDevice9::SetSoftwareVertexProcessing","SetSoftwareVertexProcessing","SetSoftwareVertexProcessing method [Direct3D 9]","SetSoftwareVertexProcessing method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetSoftwareVertexProcessing","direct3d9.idirect3ddevice9__setsoftwarevertexprocessing","f140124d-0bf1-92be-8e64-ee7d8f661302"]
old-location: direct3d9\idirect3ddevice9__setsoftwarevertexprocessing.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setsoftwarevertexprocessing.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetSoftwareVertexProcessing method, IDirect3DDevice9.SetSoftwareVertexProcessing, IDirect3DDevice9::SetSoftwareVertexProcessing, SetSoftwareVertexProcessing, SetSoftwareVertexProcessing method [Direct3D 9], SetSoftwareVertexProcessing method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetSoftwareVertexProcessing, direct3d9.idirect3ddevice9__setsoftwarevertexprocessing, f140124d-0bf1-92be-8e64-ee7d8f661302
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
 - IDirect3DDevice9::SetSoftwareVertexProcessing
 - d3d9helper/IDirect3DDevice9::SetSoftwareVertexProcessing
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
 - IDirect3DDevice9.SetSoftwareVertexProcessing
---

# IDirect3DDevice9::SetSoftwareVertexProcessing


## -description

Use this method to switch between software and hardware vertex processing.

## -parameters

### -param bSoftware [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to specify software vertex processing; <b>FALSE</b> to specify hardware vertex processing.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

The restrictions for changing modes are as follows (also refer to the notes on the <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a> constants):

<ul>
<li>If a device is created with D3DCREATE_SOFTWARE_VERTEXPROCESSING, the vertex processing will be done in software and cannot be changed.</li>
<li>If a device is created with D3DCREATE_HARDWARE_VERTEXPROCESSING, the vertex processing will be done in hardware and cannot be changed.</li>
<li>If a device is created with D3DCREATE_MIXED_VERTEXPROCESSING, the vertex processing will be done in hardware by default. The processing can be switched to software (or back to hardware) using <b>IDirect3DDevice9::SetSoftwareVertexProcessing</b>.</li>
</ul>
An application can create a mixed-mode device to use both the software vertex processing and the hardware vertex processing. To switch between the two vertex processing modes in DirectX 8.x, use IDirect3DDevice8::SetRenderState with the render state D3DRS_SOFTWAREVERTEXPROCESSING and the appropriate DWORD argument. The drawback of the render state approach was the difficulty in defining the semantics for state blocks. Applications and the runtime had to do extra work and be careful while recording and playing back state blocks.

In Direct3D 9, use <b>SetSoftwareVertexProcessing</b> instead. This new API is not recorded by StateBlocks.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getsoftwarevertexprocessing">IDirect3DDevice9::GetSoftwareVertexProcessing</a>
