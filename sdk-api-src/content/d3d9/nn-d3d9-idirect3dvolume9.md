---
UID: NN:d3d9.IDirect3DVolume9
title: IDirect3DVolume9 (d3d9.h)
description: The IDirect3DVolume9 (d3d9.h) interface is used by applications to manipulate volume resources.
helpviewer_keywords: ["3502e743-9dc5-6b50-07d2-5a1e110c1543","IDirect3DVolume9","IDirect3DVolume9 interface [Direct3D 9]","IDirect3DVolume9 interface [Direct3D 9]","described","d3d9helper/IDirect3DVolume9","direct3d9.idirect3dvolume9"]
old-location: direct3d9\idirect3dvolume9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9.htm
ms.date: 08/11/2022
ms.keywords: 3502e743-9dc5-6b50-07d2-5a1e110c1543, IDirect3DVolume9, IDirect3DVolume9 interface [Direct3D 9], IDirect3DVolume9 interface [Direct3D 9],described, d3d9helper/IDirect3DVolume9, direct3d9.idirect3dvolume9
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DVolume9
 - d3d9/IDirect3DVolume9
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3DVolume9
---

# IDirect3DVolume9 interface


## -description

Applications use the methods of the <b>IDirect3DVolume9</b> interface to manipulate volume resources.

## -inheritance

The <b>IDirect3DVolume9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DVolume9</b> also has these types of members:

## -remarks

The <b>IDirect3DVolume9</b> interface is obtained by calling the <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getvolumelevel">IDirect3DVolumeTexture9::GetVolumeLevel</a> method.

This interface, like all COM interfaces, inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DVOLUME9 and PDIRECT3DVOLUME9 types are defined as pointers to the <b>IDirect3DVolume9</b> interface.
    

    


```

typedef struct IDirect3DVolume9 *LPDIRECT3DVOLUME9, *PDIRECT3DVOLUME9;

```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>
