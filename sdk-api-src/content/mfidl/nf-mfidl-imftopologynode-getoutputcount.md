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

# IMFTopologyNode::GetOutputCount


## -description



Retrieves the number of output streams that currently exist on this node.




## -parameters




### -param pcOutputs [out]

Receives the number of output streams.


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
 




## -remarks



The output streams may or may not be connected to input streams on other nodes. To get the node that is connected to a specific output stream on this node, call <a href="https://msdn.microsoft.com/0d947d92-4669-4857-bd61-10fa8ebd2598">IMFTopologyNode::GetOutput</a>.

The <a href="https://msdn.microsoft.com/2340fd87-27ea-4f98-97e3-48b9506251a9">IMFTopologyNode::ConnectOutput</a> and <a href="https://msdn.microsoft.com/948fd64d-e3d8-45de-aaab-b052d9f0b9d8">IMFTopologyNode::SetOutputPrefType</a> methods add new input streams as needed.




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

