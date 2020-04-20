---
UID: NF:d3d9helper.IDirect3DDevice9.GetIndices
title: IDirect3DDevice9::GetIndices (d3d9helper.h)
description: Retrieves index data.helpviewer_keywords: ["137303d6-63b8-2f24-bcef-26fdda3c4a15","GetIndices","GetIndices method [Direct3D 9]","GetIndices method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetIndices method","IDirect3DDevice9.GetIndices","IDirect3DDevice9::GetIndices","d3d9helper/IDirect3DDevice9::GetIndices","direct3d9.idirect3ddevice9__getindices"]
old-location: direct3d9\idirect3ddevice9__getindices.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getindices.htm
ms.date: 12/05/2018
ms.keywords: 137303d6-63b8-2f24-bcef-26fdda3c4a15, GetIndices, GetIndices method [Direct3D 9], GetIndices method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetIndices method, IDirect3DDevice9.GetIndices, IDirect3DDevice9::GetIndices, d3d9helper/IDirect3DDevice9::GetIndices, direct3d9.idirect3ddevice9__getindices
f1_keywords:
- d3d9helper/IDirect3DDevice9.GetIndices
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D9.lib
- D3D9.dll
api_name:
- IDirect3DDevice9.GetIndices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9::GetIndices


## -description


Retrieves index data.


## -parameters




### -param ppIndexData [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a>**</b>

Address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a> interface, representing the returned index data. 


#### - pBaseVertexIndex [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to a UINT value, holding the returned base value for vertex indices. This value is added to all indices prior to referencing vertex data, defining a starting position in the vertex streams. 


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



 Calling this method will increase the internal reference count on the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a> interface. Failure to call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DIndexBuffer9</b> interface results in a memory leak.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitive">IDirect3DDevice9::DrawIndexedPrimitive</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitiveup">IDirect3DDevice9::DrawIndexedPrimitiveUP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitiveup">IDirect3DDevice9::DrawPrimitiveUP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setindices">IDirect3DDevice9::SetIndices</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/index-buffers">Index Buffers (Direct3D 9)</a>
 

 

