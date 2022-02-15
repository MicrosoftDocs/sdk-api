---
UID: NN:d3d10_1.ID3D10BlendState1
title: ID3D10BlendState1 (d3d10_1.h)
description: This blend-state interface accesses blending state for a Direct3D 10.1 device for the output-merger stage.
helpviewer_keywords: ["50959f42-4209-b827-553e-862c94c85dfc","ID3D10BlendState1","ID3D10BlendState1 interface [Direct3D 10]","ID3D10BlendState1 interface [Direct3D 10]","described","d3d10_1/ID3D10BlendState1","direct3d10.id3d10blendstate1"]
old-location: direct3d10\id3d10blendstate1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10blendstate1.htm
ms.date: 12/05/2018
ms.keywords: 50959f42-4209-b827-553e-862c94c85dfc, ID3D10BlendState1, ID3D10BlendState1 interface [Direct3D 10], ID3D10BlendState1 interface [Direct3D 10],described, d3d10_1/ID3D10BlendState1, direct3d10.id3d10blendstate1
req.header: d3d10_1.h
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
 - ID3D10BlendState1
 - d3d10_1/ID3D10BlendState1
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
 - ID3D10BlendState1
---

# ID3D10BlendState1 interface


## -description

This blend-state interface accesses blending state for a Direct3D 10.1 device for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger</a> stage.

## -inheritance

The <b>ID3D10BlendState1</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10blendstate">ID3D10BlendState</a>. <b>ID3D10BlendState1</b> also has these types of members:

## -remarks

Blending combines two pixel values. You have control over how the pixels are blended by using a predefined set of blending operations, as well as preblending operations. The <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">Blending Block Diagram</a> shows conceptually how blending works.

To create a blend-state interface, call <a href="/windows/desktop/api/d3d10_1/nf-d3d10_1-id3d10device1-createblendstate1">ID3D10Device1::CreateBlendState1</a>. To initialize the blend state, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetblendstate">ID3D10Device::OMSetBlendState</a>.

This method requires Windows Vista Service Pack 1.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10blendstate">ID3D10BlendState</a>
