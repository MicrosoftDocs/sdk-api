---
UID: NF:d3d9.IDirect3DCubeTexture9.GetLevelDesc
title: IDirect3DCubeTexture9::GetLevelDesc (d3d9.h)
description: The IDirect3DCubeTexture9::GetLevelDesc method (d3d9.h) retrieves a description of one face of the specified cube texture level.
helpviewer_keywords: ["GetLevelDesc","GetLevelDesc method [Direct3D 9]","GetLevelDesc method [Direct3D 9]","IDirect3DCubeTexture9 interface","IDirect3DCubeTexture9 interface [Direct3D 9]","GetLevelDesc method","IDirect3DCubeTexture9.GetLevelDesc","IDirect3DCubeTexture9::GetLevelDesc","d3d9helper/IDirect3DCubeTexture9::GetLevelDesc","direct3d9.idirect3dcubetexture9__getleveldesc","f3b033c9-6f8e-47a9-8c20-08c7e254bd9c"]
old-location: direct3d9\idirect3dcubetexture9__getleveldesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__getleveldesc.htm
ms.date: 08/10/2022
ms.keywords: GetLevelDesc, GetLevelDesc method [Direct3D 9], GetLevelDesc method [Direct3D 9],IDirect3DCubeTexture9 interface, IDirect3DCubeTexture9 interface [Direct3D 9],GetLevelDesc method, IDirect3DCubeTexture9.GetLevelDesc, IDirect3DCubeTexture9::GetLevelDesc, d3d9helper/IDirect3DCubeTexture9::GetLevelDesc, direct3d9.idirect3dcubetexture9__getleveldesc, f3b033c9-6f8e-47a9-8c20-08c7e254bd9c
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
 - IDirect3DCubeTexture9::GetLevelDesc
 - d3d9/IDirect3DCubeTexture9::GetLevelDesc
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
 - IDirect3DCubeTexture9.GetLevelDesc
---

# IDirect3DCubeTexture9::GetLevelDesc


## -description

Retrieves a description of one face of the specified cube texture level.

## -parameters

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies a level of a mipmapped cube texture.

### -param pDesc [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dsurface-desc">D3DSURFACE_DESC</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dsurface-desc">D3DSURFACE_DESC</a> structure, describing one face of the specified cube texture level.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.

## -remarks

The <a href="/windows/desktop/direct3d9/d3dsurface-desc">D3DSURFACE_DESC</a> structure contains Width and Height members, which describe the size of one face in the cube. To get the size of the entire cube, multiply six (the number of cube faces) by the product of Width and Height.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-adddirtyrect">IDirect3DCubeTexture9::AddDirtyRect</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-lockrect">IDirect3DCubeTexture9::LockRect</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-unlockrect">IDirect3DCubeTexture9::UnlockRect</a>
