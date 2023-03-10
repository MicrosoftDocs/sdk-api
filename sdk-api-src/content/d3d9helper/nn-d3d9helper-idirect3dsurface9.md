---
UID: NN:d3d9helper.IDirect3DSurface9
title: IDirect3DSurface9 (d3d9helper.h)
description: The IDirect3DSurface9 interface (d3d9helper.h) provides methods to query and prepare surfaces.
helpviewer_keywords: ["7eb0f571-de02-55a6-f6eb-fc92e63fbb48","IDirect3DSurface9","IDirect3DSurface9 interface [Direct3D 9]","IDirect3DSurface9 interface [Direct3D 9]","described","d3d9helper/IDirect3DSurface9","direct3d9.idirect3dsurface9"]
old-location: direct3d9\idirect3dsurface9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9.htm
ms.date: 08/12/2022
ms.keywords: 7eb0f571-de02-55a6-f6eb-fc92e63fbb48, IDirect3DSurface9, IDirect3DSurface9 interface [Direct3D 9], IDirect3DSurface9 interface [Direct3D 9],described, d3d9helper/IDirect3DSurface9, direct3d9.idirect3dsurface9
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DSurface9
 - d3d9helper/IDirect3DSurface9
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
 - IDirect3DSurface9
---

# IDirect3DSurface9 interface


## -description

Applications use the methods of the IDirect3DSurface9 interface to query and prepare surfaces.

## -inheritance

The <b>IDirect3DSurface9</b> interface inherits from <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>. <b>IDirect3DSurface9</b> also has these types of members:

## -remarks

The LPDIRECT3DSURFACE9 and PDIRECT3DSURFACE9 types are defined as pointers to the <b>IDirect3DSurface9</b> interface.
    

    


```

typedef struct IDirect3DSurface9 *LPDIRECT3DSURFACE9, *PDIRECT3DSURFACE9;

```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>
