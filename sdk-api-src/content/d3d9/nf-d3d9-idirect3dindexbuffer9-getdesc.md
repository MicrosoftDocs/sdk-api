---
UID: NF:d3d9.IDirect3DIndexBuffer9.GetDesc
title: IDirect3DIndexBuffer9::GetDesc (d3d9.h)
description: The IDirect3DIndexBuffer9::GetDesc method (d3d9helper.h) retrieves a description of the index buffer resource.
helpviewer_keywords: ["GetDesc","GetDesc method [Direct3D 9]","GetDesc method [Direct3D 9]","IDirect3DIndexBuffer9 interface","IDirect3DIndexBuffer9 interface [Direct3D 9]","GetDesc method","IDirect3DIndexBuffer9.GetDesc","IDirect3DIndexBuffer9::GetDesc","d3d9helper/IDirect3DIndexBuffer9::GetDesc","direct3d9.idirect3dindexbuffer9__getdesc","f6d3661c-7957-0918-0367-c148e854bf9f"]
old-location: direct3d9\idirect3dindexbuffer9__getdesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dindexbuffer9__getdesc.htm
ms.date: 08/11/2022
ms.keywords: GetDesc, GetDesc method [Direct3D 9], GetDesc method [Direct3D 9],IDirect3DIndexBuffer9 interface, IDirect3DIndexBuffer9 interface [Direct3D 9],GetDesc method, IDirect3DIndexBuffer9.GetDesc, IDirect3DIndexBuffer9::GetDesc, d3d9helper/IDirect3DIndexBuffer9::GetDesc, direct3d9.idirect3dindexbuffer9__getdesc, f6d3661c-7957-0918-0367-c148e854bf9f
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
 - IDirect3DIndexBuffer9::GetDesc
 - d3d9/IDirect3DIndexBuffer9::GetDesc
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
 - IDirect3DIndexBuffer9.GetDesc
---

# IDirect3DIndexBuffer9::GetDesc


## -description

Retrieves a description of the index buffer resource.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dindexbuffer-desc">D3DINDEXBUFFER_DESC</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dindexbuffer-desc">D3DINDEXBUFFER_DESC</a> structure, describing the returned index buffer.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a>



<a href="/windows/desktop/direct3d9/index-buffers">Index Buffers (Direct3D 9)</a>
