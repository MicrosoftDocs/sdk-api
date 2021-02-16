---
UID: NF:d2d1effectauthor.ID2D1TransformGraph.SetPassthroughGraph
title: ID2D1TransformGraph::SetPassthroughGraph (d2d1effectauthor.h)
description: Uses the specified input as the effect output.
helpviewer_keywords: ["ID2D1TransformGraph interface [Direct2D]","SetPassthroughGraph method","ID2D1TransformGraph.SetPassthroughGraph","ID2D1TransformGraph::SetPassthroughGraph","SetPassthroughGraph","SetPassthroughGraph method [Direct2D]","SetPassthroughGraph method [Direct2D]","ID2D1TransformGraph interface","d2d1effectauthor/ID2D1TransformGraph::SetPassthroughGraph","direct2d.id2d1transformgraph_setpassthroughgraph"]
old-location: direct2d\id2d1transformgraph_setpassthroughgraph.htm
tech.root: Direct2D
ms.assetid: 719F7C82-31D7-40A0-BD5C-59F97F0002F9
ms.date: 12/05/2018
ms.keywords: ID2D1TransformGraph interface [Direct2D],SetPassthroughGraph method, ID2D1TransformGraph.SetPassthroughGraph, ID2D1TransformGraph::SetPassthroughGraph, SetPassthroughGraph, SetPassthroughGraph method [Direct2D], SetPassthroughGraph method [Direct2D],ID2D1TransformGraph interface, d2d1effectauthor/ID2D1TransformGraph::SetPassthroughGraph, direct2d.id2d1transformgraph_setpassthroughgraph
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
 - ID2D1TransformGraph::SetPassthroughGraph
 - d2d1effectauthor/ID2D1TransformGraph::SetPassthroughGraph
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
 - ID2D1TransformGraph.SetPassthroughGraph
---

# ID2D1TransformGraph::SetPassthroughGraph


## -description

Uses the specified input as the effect output.

## -parameters

### -param effectInputIndex

The index of the input to the effect.

## -returns

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

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph">ID2D1TransformGraph</a>