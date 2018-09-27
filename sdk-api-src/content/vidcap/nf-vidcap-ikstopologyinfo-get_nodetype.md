---
UID: NF:vidcap.IKsTopologyInfo.get_NodeType
title: IKsTopologyInfo::get_NodeType
author: windows-sdk-content
description: The get_NodeType method returns the node type for a given node.
old-location: dshow\ikstopologyinfo_get_nodetype.htm
tech.root: DirectShow
ms.assetid: 6606d563-6a35-4595-8bb2-6cf74f7af4e7
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IKsTopologyInfo interface [DirectShow],get_NodeType method, IKsTopologyInfo.get_NodeType, IKsTopologyInfo::get_NodeType, IKsTopologyInfoget_NodeType, dshow.ikstopologyinfo_get_nodetype, get_NodeType, get_NodeType method [DirectShow], get_NodeType method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_NodeType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsTopologyInfo.get_NodeType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKsTopologyInfo::get_NodeType


## -description


The <code>get_NodeType</code> method returns the node type for a given node.


## -parameters




### -param dwNodeId [in]

Index of the node. To find the number of nodes, call the <a href="https://msdn.microsoft.com/fdba99d5-fd44-4d4f-8575-867d98bf3339">IKsTopologyInfo::get_NumNodes</a> method.


### -param pNodeType [out]

Receives a GUID that defines the node type. For a list of node types, see <a href="https://msdn.microsoft.com/0e133ce3-8815-47d1-a5c3-577a98963912">KS Node Types</a>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/641a10fe-8e8c-4225-b05e-b09dfb5f2fee">IKsTopologyInfo Interface</a>
 

 

