---
UID: NS:d2d1effectauthor.D2D1_VERTEX_RANGE
title: D2D1_VERTEX_RANGE (d2d1effectauthor.h)
description: Defines a range of vertices that are used when rendering less than the full contents of a vertex buffer.
helpviewer_keywords: ["D2D1_VERTEX_RANGE","D2D1_VERTEX_RANGE structure [Direct2D]","d2d1effectauthor/D2D1_VERTEX_RANGE","direct2d.d2d1_vertex_range"]
old-location: direct2d\d2d1_vertex_range.htm
tech.root: Direct2D
ms.assetid: a5c93541-86dd-48d3-b731-50e9f66f401d
ms.date: 12/05/2018
ms.keywords: D2D1_VERTEX_RANGE, D2D1_VERTEX_RANGE structure [Direct2D], d2d1effectauthor/D2D1_VERTEX_RANGE, direct2d.d2d1_vertex_range
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_VERTEX_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_VERTEX_RANGE
 - d2d1effectauthor/D2D1_VERTEX_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_VERTEX_RANGE
---

# D2D1_VERTEX_RANGE structure


## -description

Defines a range of vertices that are used when rendering less than the full contents of a vertex buffer.

## -struct-fields

### -field startVertex

The first vertex in the range to process.

### -field vertexCount

The number of vertices to use.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing">ID2D1DrawInfo::SetVertexProcessing</a>