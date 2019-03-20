---
UID: NF:mfidl.IMFTopologyNode.GetOutput
title: IMFTopologyNode::GetOutput (mfidl.h)
author: windows-sdk-content
description: Retrieves the node that is connected to a specified output stream on this node.
old-location: mf\imftopologynode_getoutput.htm
tech.root: medfound
ms.assetid: 0d947d92-4669-4857-bd61-10fa8ebd2598
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 0d947d92-4669-4857-bd61-10fa8ebd2598, GetOutput, GetOutput method [Media Foundation], GetOutput method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetOutput method, IMFTopologyNode.GetOutput, IMFTopologyNode::GetOutput, mf.imftopologynode_getoutput, mfidl/IMFTopologyNode::GetOutput
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
 - IMFTopologyNode.GetOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTopologyNode::GetOutput


## -description



Retrieves the node that is connected to a specified output stream on this node.




## -parameters




### -param dwOutputIndex [in]

Zero-based index of an output stream on this node.


### -param ppDownstreamNode [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface of the node that is connected to the specified output stream. The caller must release the interface.


### -param pdwInputIndexOnDownstreamNode [out]

Receives the index of the input stream that is connected to this node's output stream.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified input stream is not connected to another node.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

