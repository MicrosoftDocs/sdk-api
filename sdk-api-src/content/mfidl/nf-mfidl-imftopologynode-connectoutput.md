---
UID: NF:mfidl.IMFTopologyNode.ConnectOutput
title: IMFTopologyNode::ConnectOutput
author: windows-sdk-content
description: Connects an output stream from this node to the input stream of another node.
old-location: mf\imftopologynode_connectoutput.htm
old-project: medfound
ms.assetid: 2340fd87-27ea-4f98-97e3-48b9506251a9
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 2340fd87-27ea-4f98-97e3-48b9506251a9, ConnectOutput, ConnectOutput method [Media Foundation], ConnectOutput method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],ConnectOutput method, IMFTopologyNode.ConnectOutput, IMFTopologyNode::ConnectOutput, mf.imftopologynode_connectoutput, mfidl/IMFTopologyNode::ConnectOutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTopologyNode.ConnectOutput
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopologyNode::ConnectOutput


## -description



Connects an output stream from this node to the input stream of another node.




## -parameters




### -param dwOutputIndex [in]

Zero-based index of the output stream on this node.


### -param pDownstreamNode [in]

Pointer to the <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface of the node to connect to.


### -param dwInputIndexOnDownstreamNode [in]

Zero-based index of the input stream on the other node.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter.

</td>
</tr>
</table>
 




## -remarks



Node connections represent data flow from one node to the next. The streams are logical, and are specified by index.

If the node is already connected at the specified output, the method breaks the existing connection. If <i>dwOutputIndex</i> or <i>dwInputIndexOnDownstreamNode</i> specify streams that do not exist yet, the method adds as many streams as needed.

This method checks for certain invalid conditions:

<ul>
<li>
An output node cannot have any output connections. If you call this method on an output node, the method returns E_FAIL.

</li>
<li>
A node cannot be connected to itself. If <i>pDownstreamNode</i> specifies the same node as the method call, the method returns E_INVALIDARG.

</li>
</ul>
However, if the method succeeds, it does not guarantee that the node connection is valid. It is possible to create a partial topology that the topology loader cannot resolve. If so, the <a href="https://msdn.microsoft.com/02ce47db-54a1-456a-a763-c62039aea2c9">IMFTopoLoader::Load</a> method will fail.

To break an existing node connection, call <a href="https://msdn.microsoft.com/77b91797-d9a7-40da-827d-6e2a347112dc">IMFTopologyNode::DisconnectOutput</a>.




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

