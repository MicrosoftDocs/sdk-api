---
UID: NF:d3d9helper.IDirect3DVolumeTexture9.GetVolumeLevel
title: IDirect3DVolumeTexture9::GetVolumeLevel (d3d9helper.h)
description: The IDirect3DVolumeTexture9::GetVolumeLevel method (d3d9helper.h) retrieves the specified volume texture level.
helpviewer_keywords: ["6b38df70-e8ab-b3ca-2c91-45641b4a2e90","GetVolumeLevel","GetVolumeLevel method [Direct3D 9]","GetVolumeLevel method [Direct3D 9]","IDirect3DVolumeTexture9 interface","IDirect3DVolumeTexture9 interface [Direct3D 9]","GetVolumeLevel method","IDirect3DVolumeTexture9.GetVolumeLevel","IDirect3DVolumeTexture9::GetVolumeLevel","d3d9helper/IDirect3DVolumeTexture9::GetVolumeLevel","direct3d9.idirect3dvolumetexture9__getvolumelevel"]
old-location: direct3d9\idirect3dvolumetexture9__getvolumelevel.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9__getvolumelevel.htm
ms.date: 08/12/2022
ms.keywords: 6b38df70-e8ab-b3ca-2c91-45641b4a2e90, GetVolumeLevel, GetVolumeLevel method [Direct3D 9], GetVolumeLevel method [Direct3D 9],IDirect3DVolumeTexture9 interface, IDirect3DVolumeTexture9 interface [Direct3D 9],GetVolumeLevel method, IDirect3DVolumeTexture9.GetVolumeLevel, IDirect3DVolumeTexture9::GetVolumeLevel, d3d9helper/IDirect3DVolumeTexture9::GetVolumeLevel, direct3d9.idirect3dvolumetexture9__getvolumelevel
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
 - IDirect3DVolumeTexture9::GetVolumeLevel
 - d3d9helper/IDirect3DVolumeTexture9::GetVolumeLevel
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
 - IDirect3DVolumeTexture9.GetVolumeLevel
---

# IDirect3DVolumeTexture9::GetVolumeLevel


## -description

Retrieves the specified volume texture level.

## -parameters

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Identifies a level of the volume texture resource. This method returns a volume for the level specified by this parameter.

### -param ppVolumeLevel [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolume9">IDirect3DVolume9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolume9">IDirect3DVolume9</a> interface, representing the returned volume level.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

Calling this method will increase the internal reference count on the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolume9">IDirect3DVolume9</a> interface. Failure to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DVolume9</b> interface results in a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9">IDirect3DVolumeTexture9</a>
