---
UID: NN:d3d10effect.ID3D10Effect
title: ID3D10Effect (d3d10effect.h)
description: An ID3D10Effect interface manages a set of state objects, resources, and shaders for implementing a rendering effect.
helpviewer_keywords: ["8f18434d-7574-2504-c371-767566771aca","ID3D10Effect","ID3D10Effect interface [Direct3D 10]","ID3D10Effect interface [Direct3D 10]","described","d3d10effect/ID3D10Effect","direct3d10.id3d10effect"]
old-location: direct3d10\id3d10effect.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect.htm
ms.date: 12/05/2018
ms.keywords: 8f18434d-7574-2504-c371-767566771aca, ID3D10Effect, ID3D10Effect interface [Direct3D 10], ID3D10Effect interface [Direct3D 10],described, d3d10effect/ID3D10Effect, direct3d10.id3d10effect
req.header: d3d10effect.h
req.include-header: 
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Effect
 - d3d10effect/ID3D10Effect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Effect
---

# ID3D10Effect interface


## -description

An <b>ID3D10Effect</b> interface manages a set of state objects, resources, and shaders for implementing a rendering effect.

## -inheritance

The <b>ID3D10Effect</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10Effect</b> also has these types of members:

## -remarks

An effect is created by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-d3d10createeffectfrommemory">D3D10CreateEffectFromMemory</a>.

The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders. For more information, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-effects">Effects (Direct3D 10)</a>.

<div class="alert"><b>Note</b>  <p class="note">If you call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on an <b>ID3D10Effect</b> object to retrieve the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface, <b>QueryInterface</b> returns E_NOINTERFACE. To work around this issue, use the following code:


```
IUnknown* pIUnknown = (IUnknown*)pEffect;
    pIUnknown->AddRef();

```


</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-interfaces">Effect Interfaces (Direct3D 10)</a>
