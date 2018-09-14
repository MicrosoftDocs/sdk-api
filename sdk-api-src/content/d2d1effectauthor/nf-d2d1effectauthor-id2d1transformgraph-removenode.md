---
UID: NF:d2d1effectauthor.ID2D1TransformGraph.RemoveNode
title: ID2D1TransformGraph::RemoveNode
author: windows-sdk-content
description: Removes the provided node from the transform graph.
old-location: direct2d\id2d1transformgraph_removenode.htm
tech.root: Direct2D
ms.assetid: 075D43D7-0299-45E9-8C43-3EA37F0477CB
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID2D1TransformGraph interface [Direct2D],RemoveNode method, ID2D1TransformGraph.RemoveNode, ID2D1TransformGraph::RemoveNode, RemoveNode, RemoveNode method [Direct2D], RemoveNode method [Direct2D],ID2D1TransformGraph interface, d2d1effectauthor/ID2D1TransformGraph::RemoveNode, direct2d.id2d1transformgraph_removenode
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
 - ID2D1TransformGraph.RemoveNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1TransformGraph::RemoveNode


## -description


Removes the provided node from the transform graph.


## -parameters




### -param node [in]

Type: <b><a href="https://msdn.microsoft.com/2ACF65DA-A812-4983-B044-71103A9AA450">ID2D1TransformNode</a>*</b>

The node that will be removed from the transform graph.


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



The node must already exist in the graph; otherwise, the call fails with <b>D2DERR_NOT_FOUND</b>.

Any connections to this node will be removed when the node is removed.

After the node is removed, it cannot be used by the interface until it has been added to the graph by <a href="https://msdn.microsoft.com/1937BD5F-C26A-4E67-8E07-688A24DA201E">AddNode</a>.




## -see-also




<a href="https://msdn.microsoft.com/6CA29200-9834-4A5B-99E8-434CD6E9B243">ID2D1TransformGraph</a>
 

 

