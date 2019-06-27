---
UID: NF:mfidl.IMFTopologyNode.GetOutputCount
title: IMFTopologyNode::GetOutputCount (mfidl.h)
author: windows-sdk-content
description: Retrieves the number of output streams that currently exist on this node.
old-location: mf\imftopologynode_getoutputcount.htm
tech.root: medfound
ms.assetid: dc964c38-9dac-491f-9d70-b1ba7b7001ad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetOutputCount, GetOutputCount method [Media Foundation], GetOutputCount method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetOutputCount method, IMFTopologyNode.GetOutputCount, IMFTopologyNode::GetOutputCount, dc964c38-9dac-491f-9d70-b1ba7b7001ad, mf.imftopologynode_getoutputcount, mfidl/IMFTopologyNode::GetOutputCount
ms.topic: method
f1_keywords: 
 - "mfidl/IMFTopologyNode.GetOutputCount"
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
 - IMFTopologyNode.GetOutputCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



The output streams may or may not be connected to input streams on other nodes. To get the node that is connected to a specific output stream on this node, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutput">IMFTopologyNode::GetOutput</a>.

The <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput">IMFTopologyNode::ConnectOutput</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setoutputpreftype">IMFTopologyNode::SetOutputPrefType</a> methods add new input streams as needed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topologies">Topologies</a>
 

 

