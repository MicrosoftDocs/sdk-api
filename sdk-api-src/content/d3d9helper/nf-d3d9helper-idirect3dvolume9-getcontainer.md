---
UID: NF:d3d9helper.IDirect3DVolume9.GetContainer
title: IDirect3DVolume9::GetContainer (d3d9helper.h)
description: The IDirect3DVolume9::GetContainer method (d3d9.h) provides access to the parent volume texture object, if the surface is a child level of a volume texture.
helpviewer_keywords: ["0941591e-d47b-5e74-736a-768203a929fd","GetContainer","GetContainer method [Direct3D 9]","GetContainer method [Direct3D 9]","IDirect3DVolume9 interface","IDirect3DVolume9 interface [Direct3D 9]","GetContainer method","IDirect3DVolume9.GetContainer","IDirect3DVolume9::GetContainer","d3d9helper/IDirect3DVolume9::GetContainer","direct3d9.idirect3dvolume9__getcontainer"]
old-location: direct3d9\idirect3dvolume9__getcontainer.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9__getcontainer.htm
ms.date: 08/12/2022
ms.keywords: 0941591e-d47b-5e74-736a-768203a929fd, GetContainer, GetContainer method [Direct3D 9], GetContainer method [Direct3D 9],IDirect3DVolume9 interface, IDirect3DVolume9 interface [Direct3D 9],GetContainer method, IDirect3DVolume9.GetContainer, IDirect3DVolume9::GetContainer, d3d9helper/IDirect3DVolume9::GetContainer, direct3d9.idirect3dvolume9__getcontainer
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
 - IDirect3DVolume9::GetContainer
 - d3d9helper/IDirect3DVolume9::GetContainer
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
 - IDirect3DVolume9.GetContainer
---

# IDirect3DVolume9::GetContainer


## -description

Provides access to the parent volume texture object, if this surface is a child level of a volume texture.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

Reference identifier of the volume being requested.

### -param ppContainer [out, retval]

Type: <b>void**</b>

Address of a pointer to fill with the container pointer, if the query succeeds.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

If the call succeeds, the reference count of the container is increased by one.

Here's an example getting the parent volume texture of a volume texture.


```

// Assumes pSurface is a valid IDirect3DVolume9 pointer
void *pContainer = NULL;
IDirect3DVolumeTexture9 *pVolumeTexture = NULL;
HRESULT hr = pVolume->GetContainer(IID_IDirect3DVolumeTexture9, &pContainer);
if (SUCCEEDED(hr) && pContainer)
{
    pVolumeTexture = (IDirect3DVolumeTexture9 *)pContainer;

```

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolume9">IDirect3DVolume9</a>
