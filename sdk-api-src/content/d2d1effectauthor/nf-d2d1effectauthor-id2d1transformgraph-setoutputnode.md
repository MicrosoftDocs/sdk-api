---
UID: NF:d2d1effectauthor.ID2D1TransformGraph.SetOutputNode
title: ID2D1TransformGraph::SetOutputNode
author: windows-sdk-content
description: Sets the output node for the transform graph.
old-location: direct2d\id2d1transformgraph_setoutputnode.htm
tech.root: direct2d
ms.assetid: 46C92F32-6D1B-49B8-B44A-F5415E670D9C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1TransformGraph interface [Direct2D],SetOutputNode method, ID2D1TransformGraph.SetOutputNode, ID2D1TransformGraph::SetOutputNode, SetOutputNode, SetOutputNode method [Direct2D], SetOutputNode method [Direct2D],ID2D1TransformGraph interface, d2d1effectauthor/ID2D1TransformGraph::SetOutputNode, direct2d.id2d1transformgraph_setoutputnode
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
 - ID2D1TransformGraph.SetOutputNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1TransformGraph::SetOutputNode


## -description


Sets the output node for the transform graph.


## -parameters




### -param node [in]

Type: <b><a href="https://msdn.microsoft.com/2ACF65DA-A812-4983-B044-71103A9AA450">ID2D1TransformNode</a>*</b>

The node that will be considered the output of the transform node.


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




## -see-also




<a href="https://msdn.microsoft.com/6CA29200-9834-4A5B-99E8-434CD6E9B243">ID2D1TransformGraph</a>
 

 

