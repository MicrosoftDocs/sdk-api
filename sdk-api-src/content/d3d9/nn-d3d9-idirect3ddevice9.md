---
UID: NN:d3d9.IDirect3DDevice9
title: IDirect3DDevice9 (d3d9.h)
description: The IDirect3DDevice9 (d3d9.h) applications use the methods of the IDirect3DDevice9 interface to perform DrawPrimitive-based rendering and create resources.
helpviewer_keywords: ["28be25f8-38cf-f9e4-3aac-15cad98cac63","IDirect3DDevice9","IDirect3DDevice9 interface [Direct3D 9]","IDirect3DDevice9 interface [Direct3D 9]","described","d3d9helper/IDirect3DDevice9","direct3d9.idirect3ddevice9"]
old-location: direct3d9\idirect3ddevice9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9.htm
ms.date: 08/11/2022
ms.keywords: 28be25f8-38cf-f9e4-3aac-15cad98cac63, IDirect3DDevice9, IDirect3DDevice9 interface [Direct3D 9], IDirect3DDevice9 interface [Direct3D 9],described, d3d9helper/IDirect3DDevice9, direct3d9.idirect3ddevice9
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
 - IDirect3DDevice9
 - d3d9/IDirect3DDevice9
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
 - IDirect3DDevice9
---

# IDirect3DDevice9 interface


## -description

Applications use the methods of the IDirect3DDevice9 interface to perform DrawPrimitive-based rendering, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.

## -inheritance

The <b>IDirect3DDevice9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DDevice9</b> also has these types of members:

## -remarks

The <b>IDirect3DDevice9</b> interface is obtained by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a> method.

This interface, like all COM interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods.

The LPDIRECT3DDEVICE9 and PDIRECT3DDEVICE9 types are defined as pointers to the <b>IDirect3DDevice9</b> interface.


```

typedef struct IDirect3DDevice9 *LPDIRECT3DDEVICE9, *PDIRECT3DDEVICE9;

```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a>
