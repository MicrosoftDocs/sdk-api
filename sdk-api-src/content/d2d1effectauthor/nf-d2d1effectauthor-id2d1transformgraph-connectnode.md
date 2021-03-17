---
UID: NF:d2d1effectauthor.ID2D1TransformGraph.ConnectNode
title: ID2D1TransformGraph::ConnectNode (d2d1effectauthor.h)
description: Connects two nodes inside the transform graph.
helpviewer_keywords: ["ConnectNode","ConnectNode method [Direct2D]","ConnectNode method [Direct2D]","ID2D1TransformGraph interface","ID2D1TransformGraph interface [Direct2D]","ConnectNode method","ID2D1TransformGraph.ConnectNode","ID2D1TransformGraph::ConnectNode","d2d1effectauthor/ID2D1TransformGraph::ConnectNode","direct2d.id2d1transformgraph_connectnode"]
old-location: direct2d\id2d1transformgraph_connectnode.htm
tech.root: Direct2D
ms.assetid: 59C7A366-804F-4CB3-A8CB-8617F226CE6B
ms.date: 12/05/2018
ms.keywords: ConnectNode, ConnectNode method [Direct2D], ConnectNode method [Direct2D],ID2D1TransformGraph interface, ID2D1TransformGraph interface [Direct2D],ConnectNode method, ID2D1TransformGraph.ConnectNode, ID2D1TransformGraph::ConnectNode, d2d1effectauthor/ID2D1TransformGraph::ConnectNode, direct2d.id2d1transformgraph_connectnode
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
 - ID2D1TransformGraph::ConnectNode
 - d2d1effectauthor/ID2D1TransformGraph::ConnectNode
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
 - ID2D1TransformGraph.ConnectNode
---

# ID2D1TransformGraph::ConnectNode


## -description

Connects two nodes inside the transform graph.

## -parameters

### -param fromNode [in]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>*</b>

The node from which the connection will be made.

### -param toNode [in]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformnode">ID2D1TransformNode</a>*</b>

The node to which the connection will be made.

### -param toNodeInputIndex

Type: <b>UINT32</b>

The node input that will be connected.

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
<td>D2DERR_NOT_FOUND = (HRESULT_FROM_WIN32(ERROR_NOT_FOUND))</td>
<td>Direct2D could not locate the specified node.</td>
</tr>
</table>

## -remarks

Both nodes must already exist in the graph; otherwise, the call fails with <b>D2DERR_NOT_FOUND</b>.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph">ID2D1TransformGraph</a>