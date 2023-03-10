---
UID: NN:d3d11.ID3D11InputLayout
title: ID3D11InputLayout (d3d11.h)
description: An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the input-assembler stage of the graphics pipeline.
helpviewer_keywords: ["ID3D11InputLayout","ID3D11InputLayout interface [Direct3D 11]","ID3D11InputLayout interface [Direct3D 11]","described","b8a9a875-1563-0aed-8b68-020a489fb28a","d3d11/ID3D11InputLayout","direct3d11.id3d11inputlayout"]
old-location: direct3d11\id3d11inputlayout.htm
tech.root: direct3d11
ms.assetid: df83fcdc-ff1b-4901-9f1f-15eb2fe5241c
ms.date: 12/05/2018
ms.keywords: ID3D11InputLayout, ID3D11InputLayout interface [Direct3D 11], ID3D11InputLayout interface [Direct3D 11],described, b8a9a875-1563-0aed-8b68-020a489fb28a, d3d11/ID3D11InputLayout, direct3d11.id3d11inputlayout
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11InputLayout
 - d3d11/ID3D11InputLayout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InputLayout
---

# ID3D11InputLayout interface


## -description

An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a> of the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline">graphics pipeline</a>.

## -remarks

To create an input-layout object, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout">ID3D11Device::CreateInputLayout</a>. To bind the input-layout object to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-iasetinputlayout">ID3D11DeviceContext::IASetInputLayout</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>