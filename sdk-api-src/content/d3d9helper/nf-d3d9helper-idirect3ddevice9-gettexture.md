---
UID: NF:d3d9helper.IDirect3DDevice9.GetTexture
title: IDirect3DDevice9::GetTexture (d3d9helper.h)
description: The IDirect3DDevice9::GetTexture method (d3d9.h) retrieves a texture assigned to a stage for a device.
helpviewer_keywords: ["GetTexture","GetTexture method [Direct3D 9]","GetTexture method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetTexture method","IDirect3DDevice9.GetTexture","IDirect3DDevice9::GetTexture","b36b5e1a-bf59-6db1-b704-5002886b044f","d3d9helper/IDirect3DDevice9::GetTexture","direct3d9.idirect3ddevice9__gettexture"]
old-location: direct3d9\idirect3ddevice9__gettexture.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__gettexture.htm
ms.date: 08/11/2022
ms.keywords: GetTexture, GetTexture method [Direct3D 9], GetTexture method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetTexture method, IDirect3DDevice9.GetTexture, IDirect3DDevice9::GetTexture, b36b5e1a-bf59-6db1-b704-5002886b044f, d3d9helper/IDirect3DDevice9::GetTexture, direct3d9.idirect3ddevice9__gettexture
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
 - IDirect3DDevice9::GetTexture
 - d3d9helper/IDirect3DDevice9::GetTexture
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
 - IDirect3DDevice9.GetTexture
---

# IDirect3DDevice9::GetTexture


## -description

Retrieves a texture assigned to a stage for a device.

## -parameters

### -param Stage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Stage identifier of the texture to retrieve. Stage identifiers are zero-based.

### -param ppTexture [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a> interface, representing the returned texture.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

Typically, methods that return state will not work on a device that is created using D3DCREATE_PUREDEVICE. This method however, will work even on a pure device because it returns an interface.

Calling this method will increase the internal reference count on the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a> interface. Failure to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DTexture9</b> interface results in a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexturestagestate">IDirect3DDevice9::GetTextureStageState</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture">IDirect3DDevice9::SetTexture</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate">IDirect3DDevice9::SetTextureStageState</a>
