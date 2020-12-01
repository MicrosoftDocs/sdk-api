---
UID: NF:mfidl.IMFTopology.AddNode
title: IMFTopology::AddNode (mfidl.h)
description: Adds a node to the topology.
helpviewer_keywords: ["5e519524-f5c5-4d4d-922f-166f9e616631","AddNode","AddNode method [Media Foundation]","AddNode method [Media Foundation]","IMFTopology interface","IMFTopology interface [Media Foundation]","AddNode method","IMFTopology.AddNode","IMFTopology::AddNode","mf.imftopology_addnode","mfidl/IMFTopology::AddNode"]
old-location: mf\imftopology_addnode.htm
tech.root: mf
ms.assetid: 5e519524-f5c5-4d4d-922f-166f9e616631
ms.date: 12/05/2018
ms.keywords: 5e519524-f5c5-4d4d-922f-166f9e616631, AddNode, AddNode method [Media Foundation], AddNode method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],AddNode method, IMFTopology.AddNode, IMFTopology::AddNode, mf.imftopology_addnode, mfidl/IMFTopology::AddNode
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
 - IMFTopology::AddNode
 - mfidl/IMFTopology::AddNode
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
 - IMFTopology.AddNode
---

# IMFTopology::AddNode


## -description

Adds a node to the topology.

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
<i>pNode</i> is invalid, possibly because the node already exists in the topology.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>