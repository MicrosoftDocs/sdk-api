---
UID: NE:d3d11_3.D3D11_CONTEXT_TYPE
title: D3D11_CONTEXT_TYPE (d3d11_3.h)
description: Specifies the context in which a query occurs.
helpviewer_keywords: ["D3D11_CONTEXT_TYPE","D3D11_CONTEXT_TYPE enumeration [Direct3D 11]","D3D11_CONTEXT_TYPE_3D","D3D11_CONTEXT_TYPE_ALL","D3D11_CONTEXT_TYPE_COMPUTE","D3D11_CONTEXT_TYPE_COPY","D3D11_CONTEXT_TYPE_VIDEO","d3d11_3/D3D11_CONTEXT_TYPE","d3d11_3/D3D11_CONTEXT_TYPE_3D","d3d11_3/D3D11_CONTEXT_TYPE_ALL","d3d11_3/D3D11_CONTEXT_TYPE_COMPUTE","d3d11_3/D3D11_CONTEXT_TYPE_COPY","d3d11_3/D3D11_CONTEXT_TYPE_VIDEO","direct3d11.d3d11_context_type"]
old-location: direct3d11\d3d11_context_type.htm
tech.root: direct3d11
ms.assetid: 5467F07C-E429-4324-B52E-FDC25B4DB9FE
ms.date: 12/05/2018
ms.keywords: D3D11_CONTEXT_TYPE, D3D11_CONTEXT_TYPE enumeration [Direct3D 11], D3D11_CONTEXT_TYPE_3D, D3D11_CONTEXT_TYPE_ALL, D3D11_CONTEXT_TYPE_COMPUTE, D3D11_CONTEXT_TYPE_COPY, D3D11_CONTEXT_TYPE_VIDEO, d3d11_3/D3D11_CONTEXT_TYPE, d3d11_3/D3D11_CONTEXT_TYPE_3D, d3d11_3/D3D11_CONTEXT_TYPE_ALL, d3d11_3/D3D11_CONTEXT_TYPE_COMPUTE, d3d11_3/D3D11_CONTEXT_TYPE_COPY, d3d11_3/D3D11_CONTEXT_TYPE_VIDEO, direct3d11.d3d11_context_type
req.header: d3d11_3.h
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
req.typenames: D3D11_CONTEXT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_CONTEXT_TYPE
 - d3d11_3/D3D11_CONTEXT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_3.h
api_name:
 - D3D11_CONTEXT_TYPE
---

# D3D11_CONTEXT_TYPE enumeration


## -description

Specifies the context in which a query occurs.

## -enum-fields

### -field D3D11_CONTEXT_TYPE_ALL:0

The query can occur in all contexts.

### -field D3D11_CONTEXT_TYPE_3D:1

The query occurs in the context of a 3D command queue.

### -field D3D11_CONTEXT_TYPE_COMPUTE:2

The query occurs in the context of a 3D compute queue.

### -field D3D11_CONTEXT_TYPE_COPY:3

The query occurs in the context of a 3D copy queue.

### -field D3D11_CONTEXT_TYPE_VIDEO:4

The query occurs in the context of video.

## -remarks

This enum is used by the following:
        

<ul>
<li>
<a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-cd3d11_query_desc1">D3D11_QUERY_DESC1</a> structure
          </li>
<li>A CD3D11_QUERY_DESC1 constructor.</li>
<li>
<a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11devicecontext3-flush1">ID3D11DeviceContext3::Flush1</a> method
          </li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>



<a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-cd3d11_query_desc1">D3D11_QUERY_DESC1</a>
