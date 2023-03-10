---
UID: NN:d3d9helper.IDirect3DStateBlock9
title: IDirect3DStateBlock9 (d3d9helper.h)
description: The IDirect3DStateBlock9 interface (d3d9helper.h) provides methods that encapsulate render states.
helpviewer_keywords: ["4d36b0db-f60c-4be1-3a29-4484c05de1bb","IDirect3DStateBlock9","IDirect3DStateBlock9 interface [Direct3D 9]","IDirect3DStateBlock9 interface [Direct3D 9]","described","d3d9helper/IDirect3DStateBlock9","direct3d9.idirect3dstateblock9"]
old-location: direct3d9\idirect3dstateblock9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dstateblock9.htm
ms.date: 08/12/2022
ms.keywords: 4d36b0db-f60c-4be1-3a29-4484c05de1bb, IDirect3DStateBlock9, IDirect3DStateBlock9 interface [Direct3D 9], IDirect3DStateBlock9 interface [Direct3D 9],described, d3d9helper/IDirect3DStateBlock9, direct3d9.idirect3dstateblock9
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
 - IDirect3DStateBlock9
 - d3d9helper/IDirect3DStateBlock9
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
 - IDirect3DStateBlock9
---

# IDirect3DStateBlock9 interface


## -description

Applications use the methods of the IDirect3DStateBlock9 interface to encapsulate render states.

## -inheritance

The <b>IDirect3DStateBlock9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DStateBlock9</b> also has these types of members:

## -remarks

This interface can be used to save and restore pipeline state. It can also be used to capture the current state.

The LPDIRECT3DSTATEBLOCK9 and PDIRECT3DSTATEBLOCK9 types are defined as pointers to the <b>IDirect3DStateBlock9</b> interface.
    
            


```
typedef struct IDirect3DStateBlock9 *LPDIRECT3DSTATEBLOCK9, *PDIRECT3DSTATEBLOCK9;
```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>
