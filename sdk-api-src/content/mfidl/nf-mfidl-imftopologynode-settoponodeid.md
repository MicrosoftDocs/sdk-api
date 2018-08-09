---
UID: NF:mfidl.IMFTopologyNode.SetTopoNodeID
title: IMFTopologyNode::SetTopoNodeID
author: windows-sdk-content
description: Sets the identifier for the node.
old-location: mf\imftopologynode_settoponodeid.htm
old-project: medfound
ms.assetid: 80efa004-d739-4f9a-9ea3-8bf7d97f0a7d
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 80efa004-d739-4f9a-9ea3-8bf7d97f0a7d, IMFTopologyNode interface [Media Foundation],SetTopoNodeID method, IMFTopologyNode.SetTopoNodeID, IMFTopologyNode::SetTopoNodeID, SetTopoNodeID, SetTopoNodeID method [Media Foundation], SetTopoNodeID method [Media Foundation],IMFTopologyNode interface, mf.imftopologynode_settoponodeid, mfidl/IMFTopologyNode::SetTopoNodeID
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
 - IMFTopologyNode.SetTopoNodeID
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopologyNode::SetTopoNodeID


## -description


Sets the identifier for the node.


## -parameters




### -param ullTopoID






#### - llTopoID [in]

The identifier for the node.
          


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
The <a href="https://msdn.microsoft.com/a6d9246a-0cc6-4dbd-affa-e7d0bbddb008">TOPOID</a> has already been set for this object.
              

</td>
</tr>
</table>
 




## -remarks



When a node is first created, it is assigned an identifier. Typically there is no reason for an application to override the identifier. Within a topology, each node identifier should be unique.
      




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/a6d9246a-0cc6-4dbd-affa-e7d0bbddb008">TOPOID</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

