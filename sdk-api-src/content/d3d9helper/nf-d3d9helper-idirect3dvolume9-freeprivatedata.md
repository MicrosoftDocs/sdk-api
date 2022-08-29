---
UID: NF:d3d9helper.IDirect3DVolume9.FreePrivateData
title: IDirect3DVolume9::FreePrivateData (d3d9helper.h)
description: The IDirect3DVolume9::FreePrivateData method (d3d9.h) frees the specified private data associated with this volume.
helpviewer_keywords: ["FreePrivateData","FreePrivateData method [Direct3D 9]","FreePrivateData method [Direct3D 9]","IDirect3DVolume9 interface","IDirect3DVolume9 interface [Direct3D 9]","FreePrivateData method","IDirect3DVolume9.FreePrivateData","IDirect3DVolume9::FreePrivateData","b68ae9e8-a0dd-1a8d-6653-dbbf3a1477d4","d3d9helper/IDirect3DVolume9::FreePrivateData","direct3d9.idirect3dvolume9__freeprivatedata"]
old-location: direct3d9\idirect3dvolume9__freeprivatedata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9__freeprivatedata.htm
ms.date: 08/12/2022
ms.keywords: FreePrivateData, FreePrivateData method [Direct3D 9], FreePrivateData method [Direct3D 9],IDirect3DVolume9 interface, IDirect3DVolume9 interface [Direct3D 9],FreePrivateData method, IDirect3DVolume9.FreePrivateData, IDirect3DVolume9::FreePrivateData, b68ae9e8-a0dd-1a8d-6653-dbbf3a1477d4, d3d9helper/IDirect3DVolume9::FreePrivateData, direct3d9.idirect3dvolume9__freeprivatedata
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
 - IDirect3DVolume9::FreePrivateData
 - d3d9helper/IDirect3DVolume9::FreePrivateData
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
 - IDirect3DVolume9.FreePrivateData
---

# IDirect3DVolume9::FreePrivateData


## -description

Frees the specified private data associated with this volume.

## -parameters

### -param refguid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Reference to the globally unique identifier that identifies the private data to free.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_NOTFOUND.

## -remarks

Direct3D calls this method automatically when a volume is released.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolume9">IDirect3DVolume9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getprivatedata">IDirect3DVolume9::GetPrivateData</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-setprivatedata">IDirect3DVolume9::SetPrivateData</a>
