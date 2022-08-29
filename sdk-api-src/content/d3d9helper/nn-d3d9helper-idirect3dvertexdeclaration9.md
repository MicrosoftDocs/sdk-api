---
UID: NN:d3d9helper.IDirect3DVertexDeclaration9
title: IDirect3DVertexDeclaration9 (d3d9helper.h)
description: The IDirect3DVertexDeclaration9 interface (d3d9helper.h) provides methods that encapsulate the vertex shader declaration.
helpviewer_keywords: ["IDirect3DVertexDeclaration9","IDirect3DVertexDeclaration9 interface [Direct3D 9]","IDirect3DVertexDeclaration9 interface [Direct3D 9]","described","d3d9helper/IDirect3DVertexDeclaration9","direct3d9.idirect3dvertexdeclaration9","f42aaa68-f7f3-0eec-ac4e-7d8617f131ae"]
old-location: direct3d9\idirect3dvertexdeclaration9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexdeclaration9.htm
ms.date: 08/12/2022
ms.keywords: IDirect3DVertexDeclaration9, IDirect3DVertexDeclaration9 interface [Direct3D 9], IDirect3DVertexDeclaration9 interface [Direct3D 9],described, d3d9helper/IDirect3DVertexDeclaration9, direct3d9.idirect3dvertexdeclaration9, f42aaa68-f7f3-0eec-ac4e-7d8617f131ae
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
 - IDirect3DVertexDeclaration9
 - d3d9helper/IDirect3DVertexDeclaration9
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
 - IDirect3DVertexDeclaration9
---

# IDirect3DVertexDeclaration9 interface


## -description

Applications use the methods of the IDirect3DVertexDeclaration9 interface to encapsulate the vertex shader declaration.

## -inheritance

The <b>IDirect3DVertexDeclaration9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DVertexDeclaration9</b> also has these types of members:

## -remarks

A vertex shader declaration is made up of an array of vertex elements.

The LPDIRECT3DVERTEXDECLARATION9 and PDIRECT3DVERTEXDECLARATION9 types are defined as pointers to the <b>IDirect3DVertexDeclaration9</b> interface.
    
            


```
typedef struct IDirect3DVertexDeclaration9 *LPDIRECT3DVERTEXDECLARATION9, *PDIRECT3DVERTEXDECLARATION9;
```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>
