---
UID: NN:d3d9.IDirect3DQuery9
title: IDirect3DQuery9 (d3d9.h)
description: The IDirect3DQuery9 (d3d9.h) interface applications use the methods of the IDirect3DQuery9 interface to perform asynchronous queries on a driver.
helpviewer_keywords: ["6e601b3e-6b1d-4777-8fd2-a1c3ed1d5565","IDirect3DQuery9","IDirect3DQuery9 interface [Direct3D 9]","IDirect3DQuery9 interface [Direct3D 9]","described","d3d9helper/IDirect3DQuery9","direct3d9.idirect3dquery9"]
old-location: direct3d9\idirect3dquery9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dquery9.htm
ms.date: 08/11/2022
ms.keywords: 6e601b3e-6b1d-4777-8fd2-a1c3ed1d5565, IDirect3DQuery9, IDirect3DQuery9 interface [Direct3D 9], IDirect3DQuery9 interface [Direct3D 9],described, d3d9helper/IDirect3DQuery9, direct3d9.idirect3dquery9
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
 - IDirect3DQuery9
 - d3d9/IDirect3DQuery9
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
 - IDirect3DQuery9
---

# IDirect3DQuery9 interface


## -description

Applications use the methods of the IDirect3DQuery9 interface to perform asynchronous queries on a driver.

## -inheritance

The <b>IDirect3DQuery9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DQuery9</b> also has these types of members:

## -remarks

The LPDIRECT3DQUERY9 and PDIRECT3DQUERY9 types are defined as pointers to the <b>IDirect3DQuery9</b> interface.
    
            


```
typedef struct IDirect3DQuery9 *LPDIRECT3DQUERY9, *PDIRECT3DQUERY9;
```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>
