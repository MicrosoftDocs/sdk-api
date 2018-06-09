---
UID: NF:mfidl.IMFTopologyNode.GetNodeType
title: IMFTopologyNode::GetNodeType
author: windows-sdk-content
description: Retrieves the node type.
old-location: mf\imftopologynode_getnodetype.htm
old-project: medfound
ms.assetid: 64b2d2b4-1f00-412d-8188-fa361dc317a1
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 64b2d2b4-1f00-412d-8188-fa361dc317a1, GetNodeType, GetNodeType method [Media Foundation], GetNodeType method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetNodeType method, IMFTopologyNode.GetNodeType, IMFTopologyNode::GetNodeType, mf.imftopologynode_getnodetype, mfidl/IMFTopologyNode::GetNodeType
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
 - IMFTopologyNode.GetNodeType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopologyNode::GetNodeType


## -description



Retrieves the node type.




## -parameters




### -param pType [out]

Receives the node type, specified as a member of the <a href="https://msdn.microsoft.com/73ea1f48-0d86-4104-860c-83a4f9189920">MF_TOPOLOGY_TYPE</a> enumeration.


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




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

