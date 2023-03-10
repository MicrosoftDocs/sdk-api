---
UID: NF:d3d9.IDirect3DVolumeTexture9.LockBox
title: IDirect3DVolumeTexture9::LockBox (d3d9.h)
description: The IDirect3DVolumeTexture9::LockBox (d3d9.h) method locks a box on a volume texture resource.
helpviewer_keywords: ["9be8529a-2a7d-01f2-cddd-e44589e88cfe","IDirect3DVolumeTexture9 interface [Direct3D 9]","LockBox method","IDirect3DVolumeTexture9.LockBox","IDirect3DVolumeTexture9::LockBox","LockBox","LockBox method [Direct3D 9]","LockBox method [Direct3D 9]","IDirect3DVolumeTexture9 interface","d3d9helper/IDirect3DVolumeTexture9::LockBox","direct3d9.idirect3dvolumetexture9__lockbox"]
old-location: direct3d9\idirect3dvolumetexture9__lockbox.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9__lockbox.htm
ms.date: 08/11/2022
ms.keywords: 9be8529a-2a7d-01f2-cddd-e44589e88cfe, IDirect3DVolumeTexture9 interface [Direct3D 9],LockBox method, IDirect3DVolumeTexture9.LockBox, IDirect3DVolumeTexture9::LockBox, LockBox, LockBox method [Direct3D 9], LockBox method [Direct3D 9],IDirect3DVolumeTexture9 interface, d3d9helper/IDirect3DVolumeTexture9::LockBox, direct3d9.idirect3dvolumetexture9__lockbox
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
 - IDirect3DVolumeTexture9::LockBox
 - d3d9/IDirect3DVolumeTexture9::LockBox
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
 - IDirect3DVolumeTexture9.LockBox
---

# IDirect3DVolumeTexture9::LockBox


## -description

Locks a box on a volume texture resource.

## -parameters

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the level of the volume texture resource to lock.

### -param pLockedVolume [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dlocked-box">D3DLOCKED_BOX</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dlocked-box">D3DLOCKED_BOX</a> structure, describing the locked region.

### -param pBox [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3dbox">D3DBOX</a>*</b>

Pointer to the volume to lock. This parameter is specified by a pointer to a <a href="/windows/desktop/direct3d9/d3dbox">D3DBOX</a> structure. Specifying <b>NULL</b> for this parameter locks the entire volume level.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Combination of zero or more locking flags that describe the type of lock to perform. For this method, the valid flags are: 
    


<ul>
<li>D3DLOCK_DISCARD</li>
<li>D3DLOCK_NO_DIRTY_UPDATE</li>
<li>D3DLOCK_NOSYSLOCK</li>
<li>D3DLOCK_READONLY</li>
</ul>
For a description of the flags, see <a href="/windows/desktop/direct3d9/d3dlock">D3DLOCK</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

For performance reasons, dirty regions are only recorded for level zero of a texture. Dirty regions are automatically recorded when <b>LockBox</b> is called without D3DLOCK_NO_DIRTY_UPDATE or D3DLOCK_READONLY. For more information, see <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture">UpdateTexture</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9">IDirect3DVolumeTexture9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-unlockbox">UnlockBox</a>
