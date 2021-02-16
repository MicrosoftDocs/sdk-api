---
UID: NF:d2d1effectauthor.ID2D1TransformGraph.ConnectToEffectInput
title: ID2D1TransformGraph::ConnectToEffectInput (d2d1effectauthor.h)
description: Connects a transform node inside the graph to the corresponding effect input of the encapsulating effect.
helpviewer_keywords: ["ConnectToEffectInput","ConnectToEffectInput method [Direct2D]","ConnectToEffectInput method [Direct2D]","ID2D1TransformGraph interface","ID2D1TransformGraph interface [Direct2D]","ConnectToEffectInput method","ID2D1TransformGraph.ConnectToEffectInput","ID2D1TransformGraph::ConnectToEffectInput","d2d1effectauthor/ID2D1TransformGraph::ConnectToEffectInput","direct2d.id2d1transformgraph_connecttoeffectinput"]
old-location: direct2d\id2d1transformgraph_connecttoeffectinput.htm
tech.root: Direct2D
ms.assetid: 5190B887-4F3C-4304-A582-77585B438317
ms.date: 12/05/2018
ms.keywords: ConnectToEffectInput, ConnectToEffectInput method [Direct2D], ConnectToEffectInput method [Direct2D],ID2D1TransformGraph interface, ID2D1TransformGraph interface [Direct2D],ConnectToEffectInput method, ID2D1TransformGraph.ConnectToEffectInput, ID2D1TransformGraph::ConnectToEffectInput, d2d1effectauthor/ID2D1TransformGraph::ConnectToEffectInput, direct2d.id2d1transformgraph_connecttoeffectinput
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
 - ID2D1TransformGraph::ConnectToEffectInput
 - d2d1effectauthor/ID2D1TransformGraph::ConnectToEffectInput
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
 - ID2D1TransformGraph.ConnectToEffectInput
---

# ID2D1TransformGraph::ConnectToEffectInput


## -description

Connects a transform node inside the graph to the corresponding effect input of the encapsulating effect.

## -parameters

### -param toEffectInputIndex

Type: <b>UINT32</b>

The effect input to which the transform node will be bound.

### -param node [in]

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

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph">ID2D1TransformGraph</a>