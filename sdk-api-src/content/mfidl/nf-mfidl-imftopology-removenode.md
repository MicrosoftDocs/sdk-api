---
UID: NF:mfidl.IMFTopology.RemoveNode
title: IMFTopology::RemoveNode (mfidl.h)
description: Removes a node from the topology.
helpviewer_keywords: ["0dbafd3f-315b-4135-aecd-ad46f2c19886","IMFTopology interface [Media Foundation]","RemoveNode method","IMFTopology.RemoveNode","IMFTopology::RemoveNode","RemoveNode","RemoveNode method [Media Foundation]","RemoveNode method [Media Foundation]","IMFTopology interface","mf.imftopology_removenode","mfidl/IMFTopology::RemoveNode"]
old-location: mf\imftopology_removenode.htm
tech.root: mf
ms.assetid: 0dbafd3f-315b-4135-aecd-ad46f2c19886
ms.date: 12/05/2018
ms.keywords: 0dbafd3f-315b-4135-aecd-ad46f2c19886, IMFTopology interface [Media Foundation],RemoveNode method, IMFTopology.RemoveNode, IMFTopology::RemoveNode, RemoveNode, RemoveNode method [Media Foundation], RemoveNode method [Media Foundation],IMFTopology interface, mf.imftopology_removenode, mfidl/IMFTopology::RemoveNode
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
 - IMFTopology::RemoveNode
 - mfidl/IMFTopology::RemoveNode
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
 - IMFTopology.RemoveNode
---

# IMFTopology::RemoveNode


## -description

Removes a node from the topology.

## -parameters

### -param pNode [in]

Pointer to the node's <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface.

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
The specified node is not a member of this topology.

</td>
</tr>
</table>

## -remarks

This method does not destroy the node, so the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> pointer is still valid after the method returns.

The method breaks any connections between the specified node and other nodes.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>