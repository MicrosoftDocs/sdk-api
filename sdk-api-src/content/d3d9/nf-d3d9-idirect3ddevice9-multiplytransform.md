---
UID: NF:d3d9.IDirect3DDevice9.MultiplyTransform
title: IDirect3DDevice9::MultiplyTransform (d3d9.h)
description: The IDirect3DDevice9::MultiplyTransform method (d3d9.h) multiplies a device's world, view, or projection matrices by a specified matrix.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","MultiplyTransform method","IDirect3DDevice9.MultiplyTransform","IDirect3DDevice9::MultiplyTransform","MultiplyTransform","MultiplyTransform method [Direct3D 9]","MultiplyTransform method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::MultiplyTransform","direct3d9.idirect3ddevice9__multiplytransform","fe383422-a888-e230-bf89-3ae4af8e8e7d"]
old-location: direct3d9\idirect3ddevice9__multiplytransform.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__multiplytransform.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],MultiplyTransform method, IDirect3DDevice9.MultiplyTransform, IDirect3DDevice9::MultiplyTransform, MultiplyTransform, MultiplyTransform method [Direct3D 9], MultiplyTransform method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::MultiplyTransform, direct3d9.idirect3ddevice9__multiplytransform, fe383422-a888-e230-bf89-3ae4af8e8e7d
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
 - IDirect3DDevice9::MultiplyTransform
 - d3d9/IDirect3DDevice9::MultiplyTransform
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
 - IDirect3DDevice9.MultiplyTransform
---

# IDirect3DDevice9::MultiplyTransform


## -description

Multiplies a device's world, view, or projection matrices by a specified matrix.

## -parameters

### -param unnamedParam1 [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dtransformstatetype">D3DTRANSFORMSTATETYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dtransformstatetype">D3DTRANSFORMSTATETYPE</a> enumerated type, or the <a href="/windows/desktop/direct3d9/d3dts-worldmatrix">D3DTS_WORLDMATRIX</a> macro that identifies which device matrix is to be modified. The most common setting, <b>D3DTS_WORLDMATRIX</b>(0), modifies the world matrix, but you can specify that the method modify the view or projection matrices, if needed.

### -param unnamedParam2 [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3dmatrix">D3DMATRIX</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dmatrix">D3DMATRIX</a> structure that modifies the current transformation.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if one of the arguments is invalid.

## -remarks

The multiplication order is pMatrix times State.

An application might use the <b>IDirect3DDevice9::MultiplyTransform</b> method to work with hierarchies of transformations. For example, the geometry and transformations describing an arm might be arranged in the following hierarchy.


```

    
    shoulder_transformation
    
    upper_arm geometry
    
    elbow transformation
    
    lower_arm geometry
    
    wrist transformation
    
    hand geometry

```


An application might use the following series of calls to render this hierarchy. Not all the parameters are shown in this pseudocode.
    
            


```

IDirect3DDevice9::SetTransform(D3DTS_WORLDMATRIX(0), 
                               shoulder_transform)
IDirect3DDevice9::DrawPrimitive(upper_arm)
IDirect3DDevice9::MultiplyTransform(D3DTS_WORLDMATRIX(0), 
                                    elbow_transform)
IDirect3DDevice9::DrawPrimitive(lower_arm)
IDirect3DDevice9::MultiplyTransform(D3DTS_WORLDMATRIX(0), 
                                    wrist_transform)
IDirect3DDevice9::DrawPrimitive(hand)
```

## -see-also

<a href="/windows/desktop/direct3d9/d3dts-world">D3DTS_WORLD</a>



<a href="/windows/desktop/direct3d9/d3dts-worldmatrix">D3DTS_WORLDMATRIX</a>



<a href="/windows/desktop/direct3d9/d3dts-worldn">D3DTS_WORLDn</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive">IDirect3DDevice9::DrawPrimitive</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform">IDirect3DDevice9::SetTransform</a>
