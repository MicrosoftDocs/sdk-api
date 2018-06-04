---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MFGetTopoNodeCurrentType function


## -description


Gets the media type for a stream associated with a topology node.


## -parameters




### -param pNode

A pointer to the <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface.


### -param dwStreamIndex

The identifier of the stream to query. This parameter is interpreted as follows:

<ul>
<li>Transform nodes: The value is the zero-based index of the input or output stream.</li>
<li>All other node types: The value must be zero.</li>
</ul>

### -param fOutput

<b>If TRUE</b>, the function gets an output type<b>. If FALSE</b>, the function gets an input type. This parameter is interpreted as follows:

<ul>
<li>Output nodes: The value must be <b>TRUE</b>.</li>
<li>Source nodes: The value must be <b>FALSE</b>.</li>
<li>Tee nodes: The value is ignored.</li>
<li>Transform nodes: If the value is <b>TRUE</b>, the <i>dwStreamIndex</i> parameter is the index for an output stream. Otherwise, <i>dwStreamIndex</i> is the index for an input stream.</li>
</ul>

### -param ppType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The stream index is invalid.

</td>
</tr>
</table>
 




## -remarks



This function gets the actual media type from the object that is associated with the topology node. The <i>pNode</i> parameter should specify a node that belongs to a fully resolved topology.  If the node belongs to a partial topology, the function will probably fail. 

Tee nodes do not have an associated object to query. For tee nodes, the function gets the node's input type, if available. Otherwise, if no input type is available, the function gets the media type of the node's primary output stream. The primary output stream is identified by the <a href="https://msdn.microsoft.com/f7d98837-75da-48cc-8307-091be2d95392">MF_TOPONODE_PRIMARYOUTPUT</a>  attribute.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

