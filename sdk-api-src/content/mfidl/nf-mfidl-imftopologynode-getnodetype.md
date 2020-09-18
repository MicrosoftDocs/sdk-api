---
UID: NF:mfidl.IMFTopologyNode.GetNodeType
title: IMFTopologyNode::GetNodeType (mfidl.h)
description: Retrieves the node type.
helpviewer_keywords: ["64b2d2b4-1f00-412d-8188-fa361dc317a1","GetNodeType","GetNodeType method [Media Foundation]","GetNodeType method [Media Foundation]","IMFTopologyNode interface","IMFTopologyNode interface [Media Foundation]","GetNodeType method","IMFTopologyNode.GetNodeType","IMFTopologyNode::GetNodeType","mf.imftopologynode_getnodetype","mfidl/IMFTopologyNode::GetNodeType"]
old-location: mf\imftopologynode_getnodetype.htm
tech.root: mf
ms.assetid: 64b2d2b4-1f00-412d-8188-fa361dc317a1
ms.date: 12/05/2018
ms.keywords: 64b2d2b4-1f00-412d-8188-fa361dc317a1, GetNodeType, GetNodeType method [Media Foundation], GetNodeType method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetNodeType method, IMFTopologyNode.GetNodeType, IMFTopologyNode::GetNodeType, mf.imftopologynode_getnodetype, mfidl/IMFTopologyNode::GetNodeType
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTopologyNode::GetNodeType
 - mfidl/IMFTopologyNode::GetNodeType
dev_langs:
 - c++
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
---

# IMFTopologyNode::GetNodeType


## -description

Retrieves the node type.

## -parameters

### -param pType [out]

Receives the node type, specified as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_topology_type">MF_TOPOLOGY_TYPE</a> enumeration.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>