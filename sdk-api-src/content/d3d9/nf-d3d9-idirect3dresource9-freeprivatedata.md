---
UID: NF:d3d9.IDirect3DResource9.FreePrivateData
title: IDirect3DResource9::FreePrivateData (d3d9.h)
description: The IDirect3DResource9::FreePrivateData (d3d9.h) method frees the specified private data associated with this resource.
helpviewer_keywords: ["FreePrivateData","FreePrivateData method [Direct3D 9]","FreePrivateData method [Direct3D 9]","IDirect3DResource9 interface","IDirect3DResource9 interface [Direct3D 9]","FreePrivateData method","IDirect3DResource9.FreePrivateData","IDirect3DResource9::FreePrivateData","d3d9helper/IDirect3DResource9::FreePrivateData","direct3d9.idirect3dresource9__freeprivatedata","e283eb7c-b7c9-110d-2b8b-1966dc1dc914"]
old-location: direct3d9\idirect3dresource9__freeprivatedata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__freeprivatedata.htm
ms.date: 08/11/2022
ms.keywords: FreePrivateData, FreePrivateData method [Direct3D 9], FreePrivateData method [Direct3D 9],IDirect3DResource9 interface, IDirect3DResource9 interface [Direct3D 9],FreePrivateData method, IDirect3DResource9.FreePrivateData, IDirect3DResource9::FreePrivateData, d3d9helper/IDirect3DResource9::FreePrivateData, direct3d9.idirect3dresource9__freeprivatedata, e283eb7c-b7c9-110d-2b8b-1966dc1dc914
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
 - IDirect3DResource9::FreePrivateData
 - d3d9/IDirect3DResource9::FreePrivateData
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
 - IDirect3DResource9.FreePrivateData
---

# IDirect3DResource9::FreePrivateData


## -description

Frees the specified private data associated with this resource.

## -parameters

### -param refguid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Reference to the globally unique identifier that identifies the private data to free.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_NOTFOUND.

## -remarks

Direct3D calls this method automatically when a resource is released.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>
