---
UID: NF:d2d1effectauthor.ID2D1TransformGraph.ConnectNode
title: ID2D1TransformGraph::ConnectNode
author: windows-sdk-content
description: Connects two nodes inside the transform graph.
old-location: direct2d\id2d1transformgraph_connectnode.htm
tech.root: direct2d
ms.assetid: 59C7A366-804F-4CB3-A8CB-8617F226CE6B
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ConnectNode, ConnectNode method [Direct2D], ConnectNode method [Direct2D],ID2D1TransformGraph interface, ID2D1TransformGraph interface [Direct2D],ConnectNode method, ID2D1TransformGraph.ConnectNode, ID2D1TransformGraph::ConnectNode, d2d1effectauthor/ID2D1TransformGraph::ConnectNode, direct2d.id2d1transformgraph_connectnode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1TransformGraph::ConnectNode


## -description


Connects two nodes inside the transform graph.


## -parameters




### -param fromNode [in]

Type: <b><a href="https://msdn.microsoft.com/2ACF65DA-A812-4983-B044-71103A9AA450">ID2D1TransformNode</a>*</b>

The node from which the connection will be made.


### -param toNode [in]

Type: <b><a href="https://msdn.microsoft.com/2ACF65DA-A812-4983-B044-71103A9AA450">ID2D1TransformNode</a>*</b>

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




<a href="https://msdn.microsoft.com/6CA29200-9834-4A5B-99E8-434CD6E9B243">ID2D1TransformGraph</a>
 

 

