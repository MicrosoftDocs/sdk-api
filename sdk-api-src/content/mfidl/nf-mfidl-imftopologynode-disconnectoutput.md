---
UID: NF:mfidl.IMFTopologyNode.DisconnectOutput
title: IMFTopologyNode::DisconnectOutput
author: windows-driver-content
description: Disconnects an output stream on this node.
old-location: mf\imftopologynode_disconnectoutput.htm
old-project: medfound
ms.assetid: 77b91797-d9a7-40da-827d-6e2a347112dc
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 77b91797-d9a7-40da-827d-6e2a347112dc, DisconnectOutput, DisconnectOutput method [Media Foundation], DisconnectOutput method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],DisconnectOutput method, IMFTopologyNode.DisconnectOutput, IMFTopologyNode::DisconnectOutput, mf.imftopologynode_disconnectoutput, mfidl/IMFTopologyNode::DisconnectOutput
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTopologyNode.DisconnectOutput
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopologyNode::DisconnectOutput


## -description



Disconnects an output stream on this node.




## -parameters




### -param dwOutputIndex [in]

Zero-based index of the output stream to disconnect.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwOutputIndex</i> parameter is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified output stream is not connected to another node.

</td>
</tr>
</table>
 




## -remarks



If the specified output stream is connected to another node, this method breaks the connection.




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

