---
UID: NF:d2d1.ID2D1TessellationSink.AddTriangles
title: ID2D1TessellationSink::AddTriangles (d2d1.h)
description: Copies the specified triangles to the sink.
helpviewer_keywords: ["AddTriangles","AddTriangles method [Direct2D]","AddTriangles method [Direct2D]","ID2D1TessellationSink interface","ID2D1TessellationSink interface [Direct2D]","AddTriangles method","ID2D1TessellationSink.AddTriangles","ID2D1TessellationSink::AddTriangles","d2d1/ID2D1TessellationSink::AddTriangles","direct2d.ID2D1TessellationSink_AddTriangles"]
old-location: direct2d\ID2D1TessellationSink_AddTriangles.htm
tech.root: Direct2D
ms.assetid: 45084e57-d022-4bdb-9001-83e4e88c9c55
ms.date: 12/05/2018
ms.keywords: AddTriangles, AddTriangles method [Direct2D], AddTriangles method [Direct2D],ID2D1TessellationSink interface, ID2D1TessellationSink interface [Direct2D],AddTriangles method, ID2D1TessellationSink.AddTriangles, ID2D1TessellationSink::AddTriangles, d2d1/ID2D1TessellationSink::AddTriangles, direct2d.ID2D1TessellationSink_AddTriangles
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1TessellationSink::AddTriangles
 - d2d1/ID2D1TessellationSink::AddTriangles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1TessellationSink.AddTriangles
---

# ID2D1TessellationSink::AddTriangles


## -description

Copies the specified triangles to the sink.

## -parameters

### -param triangles [in]

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_triangle">D2D1_TRIANGLE</a>*</b>

An array of <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_triangle">D2D1_TRIANGLE</a> structures that describe the triangles to add to the sink.

### -param trianglesCount

Type: <b>UINT</b>

The number of triangles to copy from the <i>triangles</i> array.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink">ID2D1TessellationSink</a>

