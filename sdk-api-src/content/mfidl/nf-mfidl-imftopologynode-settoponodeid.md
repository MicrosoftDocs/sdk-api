---
UID: NF:mfidl.IMFTopologyNode.SetTopoNodeID
title: IMFTopologyNode::SetTopoNodeID (mfidl.h)
description: Sets the identifier for the node.
helpviewer_keywords: ["80efa004-d739-4f9a-9ea3-8bf7d97f0a7d","IMFTopologyNode interface [Media Foundation]","SetTopoNodeID method","IMFTopologyNode.SetTopoNodeID","IMFTopologyNode::SetTopoNodeID","SetTopoNodeID","SetTopoNodeID method [Media Foundation]","SetTopoNodeID method [Media Foundation]","IMFTopologyNode interface","mf.imftopologynode_settoponodeid","mfidl/IMFTopologyNode::SetTopoNodeID"]
old-location: mf\imftopologynode_settoponodeid.htm
tech.root: mf
ms.assetid: 80efa004-d739-4f9a-9ea3-8bf7d97f0a7d
ms.date: 12/05/2018
ms.keywords: 80efa004-d739-4f9a-9ea3-8bf7d97f0a7d, IMFTopologyNode interface [Media Foundation],SetTopoNodeID method, IMFTopologyNode.SetTopoNodeID, IMFTopologyNode::SetTopoNodeID, SetTopoNodeID, SetTopoNodeID method [Media Foundation], SetTopoNodeID method [Media Foundation],IMFTopologyNode interface, mf.imftopologynode_settoponodeid, mfidl/IMFTopologyNode::SetTopoNodeID
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
 - IMFTopologyNode::SetTopoNodeID
 - mfidl/IMFTopologyNode::SetTopoNodeID
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
 - IMFTopologyNode.SetTopoNodeID
---

# IMFTopologyNode::SetTopoNodeID


## -description

Sets the identifier for the node.

## -parameters

### -param ullTopoID [in]

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
The <a href="/windows/desktop/medfound/topoid">TOPOID</a> has already been set for this object.
              

</td>
</tr>
</table>

## -remarks

When a node is first created, it is assigned an identifier. Typically there is no reason for an application to override the identifier. Within a topology, each node identifier should be unique.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topoid">TOPOID</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>