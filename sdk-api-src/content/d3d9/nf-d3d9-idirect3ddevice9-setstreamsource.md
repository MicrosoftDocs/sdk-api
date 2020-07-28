---
UID: NF:d3d9.IDirect3DDevice9.SetStreamSource
title: IDirect3DDevice9::SetStreamSource (d3d9.h)
description: Binds a vertex buffer to a device data stream. For more information, see Setting the Stream Source (Direct3D 9).
helpviewer_keywords: ["58d641c0-a959-cca3-67e2-7290e9426e8e","IDirect3DDevice9 interface [Direct3D 9]","SetStreamSource method","IDirect3DDevice9.SetStreamSource","IDirect3DDevice9::SetStreamSource","SetStreamSource","SetStreamSource method [Direct3D 9]","SetStreamSource method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetStreamSource","direct3d9.idirect3ddevice9__setstreamsource"]
old-location: direct3d9\idirect3ddevice9__setstreamsource.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setstreamsource.htm
ms.date: 12/05/2018
ms.keywords: 58d641c0-a959-cca3-67e2-7290e9426e8e, IDirect3DDevice9 interface [Direct3D 9],SetStreamSource method, IDirect3DDevice9.SetStreamSource, IDirect3DDevice9::SetStreamSource, SetStreamSource, SetStreamSource method [Direct3D 9], SetStreamSource method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetStreamSource, direct3d9.idirect3ddevice9__setstreamsource
f1_keywords:
- d3d9/IDirect3DDevice9.SetStreamSource
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
- IDirect3DDevice9.SetStreamSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9::SetStreamSource


## -description


Binds a vertex buffer to a device data stream. For more information, see <a href="https://docs.microsoft.com/windows/desktop/direct3d9/setting-the-stream-source">Setting the Stream Source (Direct3D 9)</a>.


## -parameters




### -param StreamNumber [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the data stream, in the range from 0 to the maximum number of streams -1.


### -param pStreamData [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a>*</b>

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a> interface, representing the vertex buffer to bind to the specified data stream. 


### -param OffsetInBytes [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset from the beginning of the stream to the beginning of the vertex data, in bytes. To find out if the device supports stream offsets, see the D3DDEVCAPS2_STREAMOFFSET constant in <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2</a>.


### -param Stride [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Stride of the component, in bytes. See Remarks.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



When a FVF vertex shader is used, the stride of the vertex stream must match the vertex size, computed from the FVF. When a declaration is used, the stride should be greater than or equal to the stream size computed from the declaration.

When calling SetStreamSource, the stride is normally required to be equal to the vertex size. However, there are times when you may want to draw multiple instances of the same or similar geometry (such as when using instancing to draw). For this case, use a zero stride to tell the runtime not to increment the vertex buffer offset (ie: use the same vertex data for all instances). For more information about instancing, see <a href="https://docs.microsoft.com/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitive">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitiveup">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitiveup">IDirect3DDevice9::DrawPrimitiveUP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getstreamsource">IDirect3DDevice9::GetStreamSource</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/vertex-buffers">Vertex Buffers (Direct3D 9)</a>
 

 

