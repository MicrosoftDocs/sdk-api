---
UID: NN:d3d9helper.IDirect3D9
title: IDirect3D9 (d3d9helper.h)
description: The IDirect3D9 interface (d3d9helper.h) provides methods that create Microsoft Direct3D objects and set up the environment.
helpviewer_keywords: ["IDirect3D9","IDirect3D9 interface [Direct3D 9]","IDirect3D9 interface [Direct3D 9]","described","d3d9helper/IDirect3D9","dc75d960-747a-5bea-1745-0255278bfcd1","direct3d9.idirect3d9"]
old-location: direct3d9\idirect3d9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9.htm
ms.date: 08/12/2022
ms.keywords: IDirect3D9, IDirect3D9 interface [Direct3D 9], IDirect3D9 interface [Direct3D 9],described, d3d9helper/IDirect3D9, dc75d960-747a-5bea-1745-0255278bfcd1, direct3d9.idirect3d9
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
 - IDirect3D9
 - d3d9helper/IDirect3D9
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
 - IDirect3D9
---

# IDirect3D9 interface


## -description

Applications use the methods of the IDirect3D9 interface to create Microsoft Direct3D objects and set up the environment. This interface includes methods for enumerating and retrieving capabilities of the device.

## -inheritance

The <b>IDirect3D9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3D9</b> also has these types of members:

## -remarks

The <b>IDirect3D9</b> interface is obtained by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-direct3dcreate9">Direct3DCreate9</a> function.

The LPDIRECT3D9 and PDIRECT3D9 types are defined as pointers to the <b>IDirect3D9</b> interface.
    
            


```
typedef struct IDirect3D9 *LPDIRECT3D9, *PDIRECT3D9;
```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>
