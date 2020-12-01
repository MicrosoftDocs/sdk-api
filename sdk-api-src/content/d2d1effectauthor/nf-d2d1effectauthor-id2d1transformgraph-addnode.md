---
UID: NF:d2d1effectauthor.ID2D1TransformGraph.AddNode
title: ID2D1TransformGraph::AddNode (d2d1effectauthor.h)
description: Adds the provided node to the transform graph.
helpviewer_keywords: ["AddNode","AddNode method [Direct2D]","AddNode method [Direct2D]","ID2D1TransformGraph interface","ID2D1TransformGraph interface [Direct2D]","AddNode method","ID2D1TransformGraph.AddNode","ID2D1TransformGraph::AddNode","d2d1effectauthor/ID2D1TransformGraph::AddNode","direct2d.id2d1transformgraph_addnode"]
old-location: direct2d\id2d1transformgraph_addnode.htm
tech.root: Direct2D
ms.assetid: 1937BD5F-C26A-4E67-8E07-688A24DA201E
ms.date: 12/05/2018
ms.keywords: AddNode, AddNode method [Direct2D], AddNode method [Direct2D],ID2D1TransformGraph interface, ID2D1TransformGraph interface [Direct2D],AddNode method, ID2D1TransformGraph.AddNode, ID2D1TransformGraph::AddNode, d2d1effectauthor/ID2D1TransformGraph::AddNode, direct2d.id2d1transformgraph_addnode
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
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1TransformGraph::AddNode
 - d2d1effectauthor/ID2D1TransformGraph::AddNode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1TransformGraph.AddNode
---

# ID2D1TransformGraph::AddNode


## -description

Adds the provided node to the transform graph.

## -parameters

### -param node [in]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>*</b>

The node that will be added to the transform graph.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
</table>

## -remarks

This adds a transform node to the transform graph. A node must be added to the transform graph before it can be interconnected in any way.


A transform graph cannot be directly added to another transform graph. 
Only interfaces derived from <a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a> can be added to the transform graph.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph">ID2D1TransformGraph</a>