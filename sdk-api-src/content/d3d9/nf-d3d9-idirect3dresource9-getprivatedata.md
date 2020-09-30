---
UID: NF:d3d9.IDirect3DResource9.GetPrivateData
title: IDirect3DResource9::GetPrivateData (d3d9.h)
description: Copies the private data associated with the resource to a provided buffer.
helpviewer_keywords: ["GetPrivateData","GetPrivateData method [Direct3D 9]","GetPrivateData method [Direct3D 9]","IDirect3DResource9 interface","IDirect3DResource9 interface [Direct3D 9]","GetPrivateData method","IDirect3DResource9.GetPrivateData","IDirect3DResource9::GetPrivateData","a3ce4b5e-f58e-cf26-2ef5-896eaf4a5613","d3d9helper/IDirect3DResource9::GetPrivateData","direct3d9.idirect3dresource9__getprivatedata"]
old-location: direct3d9\idirect3dresource9__getprivatedata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__getprivatedata.htm
ms.date: 12/05/2018
ms.keywords: GetPrivateData, GetPrivateData method [Direct3D 9], GetPrivateData method [Direct3D 9],IDirect3DResource9 interface, IDirect3DResource9 interface [Direct3D 9],GetPrivateData method, IDirect3DResource9.GetPrivateData, IDirect3DResource9::GetPrivateData, a3ce4b5e-f58e-cf26-2ef5-896eaf4a5613, d3d9helper/IDirect3DResource9::GetPrivateData, direct3d9.idirect3dresource9__getprivatedata
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
 - IDirect3DResource9::GetPrivateData
 - d3d9/IDirect3DResource9::GetPrivateData
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
 - IDirect3DResource9.GetPrivateData
---

# IDirect3DResource9::GetPrivateData


## -description

Copies the private data associated with the resource to a provided buffer.

## -parameters

### -param refguid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

The globally unique identifier that identifies the private data to retrieve.

### -param pData [in, out]

Type: <b>void*</b>

Pointer to a previously allocated buffer to fill with the requested private data if the call succeeds. The application calling this method is responsible for allocating and releasing this buffer. If this parameter is <b>NULL</b>, this method will return the buffer size in pSizeOfData.

### -param pSizeOfData [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Pointer to the size of the buffer at 
    pData, in bytes. If this value is less than the actual size of the private data (such as 0), the method sets this parameter to the required buffer size and the method returns D3DERR_MOREDATA.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_MOREDATA, D3DERR_NOTFOUND.

## -remarks

This method is inherited by the following interfaces: 
    
    <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>, 
    
    <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>,
    
    <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a>, 
    
    <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a>, 
    
    <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9">IDirect3DVolumeTexture9</a>,
    
    <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a>, 
    
    <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>