---
UID: NF:d3d11.ID3D11DeviceContext.IAGetPrimitiveTopology
title: ID3D11DeviceContext::IAGetPrimitiveTopology (d3d11.h)
description: Get information about the primitive type, and data order that describes input data for the input assembler stage. (ID3D11DeviceContext.IAGetPrimitiveTopology)
helpviewer_keywords: ["83077387-5c62-f840-c94a-b5edcab58593","IAGetPrimitiveTopology","IAGetPrimitiveTopology method [Direct3D 11]","IAGetPrimitiveTopology method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","IAGetPrimitiveTopology method","ID3D11DeviceContext.IAGetPrimitiveTopology","ID3D11DeviceContext::IAGetPrimitiveTopology","d3d11/ID3D11DeviceContext::IAGetPrimitiveTopology","direct3d11.id3d11devicecontext_iagetprimitivetopology"]
old-location: direct3d11\id3d11devicecontext_iagetprimitivetopology.htm
tech.root: direct3d11
ms.assetid: 99f82993-72c2-47b5-a2fe-16bb1e7bd2e3
ms.date: 12/05/2018
ms.keywords: 83077387-5c62-f840-c94a-b5edcab58593, IAGetPrimitiveTopology, IAGetPrimitiveTopology method [Direct3D 11], IAGetPrimitiveTopology method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IAGetPrimitiveTopology method, ID3D11DeviceContext.IAGetPrimitiveTopology, ID3D11DeviceContext::IAGetPrimitiveTopology, d3d11/ID3D11DeviceContext::IAGetPrimitiveTopology, direct3d11.id3d11devicecontext_iagetprimitivetopology
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::IAGetPrimitiveTopology
 - d3d11/ID3D11DeviceContext::IAGetPrimitiveTopology
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
 - ID3D11DeviceContext.IAGetPrimitiveTopology
---

# ID3D11DeviceContext::IAGetPrimitiveTopology


## -description

Get information about the primitive type, and data order that describes input data for the input assembler stage.

## -parameters

### -param pTopology [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)">D3D11_PRIMITIVE_TOPOLOGY</a>*</b>

A pointer to the type of primitive, and ordering of the primitive data (see <a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)">D3D11_PRIMITIVE_TOPOLOGY</a>).

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
