---
UID: NN:d3d10.ID3D10InputLayout
title: ID3D10InputLayout (d3d10.h)
description: An input-layout interface accesses the input data for the input-assembler stage.
helpviewer_keywords: ["763093e1-3009-8d0d-b2e2-1d58775e2b52","ID3D10InputLayout","ID3D10InputLayout interface [Direct3D 10]","ID3D10InputLayout interface [Direct3D 10]","described","d3d10/ID3D10InputLayout","direct3d10.id3d10inputlayout"]
old-location: direct3d10\id3d10inputlayout.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10inputlayout.htm
ms.date: 12/05/2018
ms.keywords: 763093e1-3009-8d0d-b2e2-1d58775e2b52, ID3D10InputLayout, ID3D10InputLayout interface [Direct3D 10], ID3D10InputLayout interface [Direct3D 10],described, d3d10/ID3D10InputLayout, direct3d10.id3d10inputlayout
req.header: d3d10.h
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
 - ID3D10InputLayout
 - d3d10/ID3D10InputLayout
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
 - ID3D10InputLayout
---

# ID3D10InputLayout interface


## -description

An input-layout interface accesses the input data for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.

## -remarks

This interface is created by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createinputlayout">ID3D10Device::CreateInputLayout</a>; use <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-iasetinputlayout">ID3D10Device::IASetInputLayout</a> to bind it to the graphics pipeline.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>