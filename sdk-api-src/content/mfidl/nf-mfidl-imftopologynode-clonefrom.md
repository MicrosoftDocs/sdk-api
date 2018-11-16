---
UID: NF:mfidl.IMFTopologyNode.CloneFrom
title: IMFTopologyNode::CloneFrom
author: windows-sdk-content
description: Copies the data from another topology node into this node.
old-location: mf\imftopologynode_clonefrom.htm
tech.root: medfound
ms.assetid: 90322fbc-e3de-4801-b10b-63ce538fc83f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 90322fbc-e3de-4801-b10b-63ce538fc83f, CloneFrom, CloneFrom method [Media Foundation], CloneFrom method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],CloneFrom method, IMFTopologyNode.CloneFrom, IMFTopologyNode::CloneFrom, mf.imftopologynode_clonefrom, mfidl/IMFTopologyNode::CloneFrom
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
 - IMFTopologyNode.CloneFrom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFTopologyNode.CloneFrom
: 
---

# IMFTopologyNode::CloneFrom


## -description


Copies the data from another topology node into this node.


## -parameters




### -param pNode [in]

A pointer to the <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface of the node to copy.
          


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The node types do not match.
              

</td>
</tr>
</table>
 




## -remarks



The two nodes must have the same node type. To get the node type, call <a href="https://msdn.microsoft.com/64b2d2b4-1f00-412d-8188-fa361dc317a1">IMFTopologyNode::GetNodeType</a>.
      

This method copies the object pointer, preferred types, and attributes from <i>pNode</i> to this node. It also copies the <a href="https://msdn.microsoft.com/a6d9246a-0cc6-4dbd-affa-e7d0bbddb008">TOPOID</a> that uniquely identifies each node in a topology. It does not duplicate any of the connections from <i>pNode</i> to other nodes.
      

The purpose of this method is to copy nodes from one topology to another. Do not use duplicate nodes within the same topology.
      




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

