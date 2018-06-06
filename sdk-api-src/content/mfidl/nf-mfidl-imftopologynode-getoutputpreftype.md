---
UID: NF:mfidl.IMFTopologyNode.GetOutputPrefType
title: IMFTopologyNode::GetOutputPrefType
author: windows-sdk-content
description: Retrieves the preferred media type for an output stream on this node.
old-location: mf\imftopologynode_getoutputpreftype.htm
old-project: medfound
ms.assetid: 972052ca-1d87-4fa4-abeb-6e74ba6c9368
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 972052ca-1d87-4fa4-abeb-6e74ba6c9368, GetOutputPrefType, GetOutputPrefType method [Media Foundation], GetOutputPrefType method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetOutputPrefType method, IMFTopologyNode.GetOutputPrefType, IMFTopologyNode::GetOutputPrefType, mf.imftopologynode_getoutputpreftype, mfidl/IMFTopologyNode::GetOutputPrefType
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopologyNode.GetOutputPrefType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopologyNode::GetOutputPrefType


## -description



Retrieves the preferred media type for an output stream on this node.




## -parameters




### -param dwOutputIndex [in]

Zero-based index of the output stream.


### -param ppType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type. The caller must release the interface.


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
This node does not have a preferred output type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This node is an output node.

</td>
</tr>
</table>
 




## -remarks



Output nodes cannot have outputs. If this method is called on an output node, it returns E_NOTIMPL.

The preferred output type provides a hint to the topology loader. In a fully resolved topology, there is no guarantee that every topology node will have a preferred output type. To get the actual media type for a node, you must get a pointer to the node's underlying object. (For more information, see <a href="https://msdn.microsoft.com/73ea1f48-0d86-4104-860c-83a4f9189920">MF_TOPOLOGY_TYPE</a> enumeration.)




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

