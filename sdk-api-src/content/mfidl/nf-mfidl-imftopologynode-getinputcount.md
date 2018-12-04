---
UID: NF:mfidl.IMFTopologyNode.GetInputCount
title: IMFTopologyNode::GetInputCount
author: windows-sdk-content
description: Retrieves the number of input streams that currently exist on this node.
old-location: mf\imftopologynode_getinputcount.htm
tech.root: medfound
ms.assetid: 84c079da-5de6-4c33-b0c7-5ffd017d5513
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: 84c079da-5de6-4c33-b0c7-5ffd017d5513, GetInputCount, GetInputCount method [Media Foundation], GetInputCount method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetInputCount method, IMFTopologyNode.GetInputCount, IMFTopologyNode::GetInputCount, mf.imftopologynode_getinputcount, mfidl/IMFTopologyNode::GetInputCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopologyNode.GetInputCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTopologyNode::GetInputCount


## -description



Retrieves the number of input streams that currently exist on this node.




## -parameters




### -param pcInputs [out]

Receives the number of input streams.


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



The input streams may or may not be connected to output streams on other nodes. To get the node that is connected to a specified input stream, call <a href="https://msdn.microsoft.com/49969e6d-c893-4f6f-8c1d-87d32405a65d">IMFTopologyNode::GetInput</a>.

The <a href="https://msdn.microsoft.com/2340fd87-27ea-4f98-97e3-48b9506251a9">IMFTopologyNode::ConnectOutput</a> and <a href="https://msdn.microsoft.com/348b3cba-8c8c-4df9-8cb9-b69cd140cffb">IMFTopologyNode::SetInputPrefType</a> methods add new input streams as needed.




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

