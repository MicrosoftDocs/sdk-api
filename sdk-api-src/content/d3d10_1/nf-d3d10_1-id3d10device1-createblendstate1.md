---
UID: NF:d3d10_1.ID3D10Device1.CreateBlendState1
title: ID3D10Device1::CreateBlendState1 (d3d10_1.h)
description: Create a blend-state object that encapsulates blend state for the output-merger stage. (ID3D10Device1.CreateBlendState1)
helpviewer_keywords: ["CreateBlendState1","CreateBlendState1 method [Direct3D 10]","CreateBlendState1 method [Direct3D 10]","ID3D10Device1 interface","ID3D10Device1 interface [Direct3D 10]","CreateBlendState1 method","ID3D10Device1.CreateBlendState1","ID3D10Device1::CreateBlendState1","b8ad390b-12a5-cfce-2558-a74e808c9358","d3d10_1/ID3D10Device1::CreateBlendState1","direct3d10.id3d10device1_createblendstate1"]
old-location: direct3d10\id3d10device1_createblendstate1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device1_createblendstate1.htm
ms.date: 12/05/2018
ms.keywords: CreateBlendState1, CreateBlendState1 method [Direct3D 10], CreateBlendState1 method [Direct3D 10],ID3D10Device1 interface, ID3D10Device1 interface [Direct3D 10],CreateBlendState1 method, ID3D10Device1.CreateBlendState1, ID3D10Device1::CreateBlendState1, b8ad390b-12a5-cfce-2558-a74e808c9358, d3d10_1/ID3D10Device1::CreateBlendState1, direct3d10.id3d10device1_createblendstate1
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device1::CreateBlendState1
 - d3d10_1/ID3D10Device1::CreateBlendState1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10_1.h
api_name:
 - ID3D10Device1.CreateBlendState1
---

# ID3D10Device1::CreateBlendState1


## -description

Create a blend-state object that encapsulates blend state for the output-merger stage.

## -parameters

### -param pBlendStateDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_blend_desc1">D3D10_BLEND_DESC1</a>*</b>

Pointer to a blend-state description (see <a href="/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_blend_desc1">D3D10_BLEND_DESC1</a>).

### -param ppBlendState [out]

Type: <b><a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10blendstate1">ID3D10BlendState1</a>**</b>

Address of a pointer to the blend-state object created (see <a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10blendstate1">ID3D10BlendState1 Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

An application can create up to 4096 unique blend-state objects. For each object created, the runtime checks to see if a previous object has the same state. If such a previous object exists, the runtime will return a pointer to previous instance instead of creating a duplicate object.

This method requires Windows Vista Service Pack 1.

## -see-also

<a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1">ID3D10Device1 Interface</a>
