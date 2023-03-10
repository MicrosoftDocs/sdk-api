---
UID: NF:mfidl.IMFTopology.GetNodeByID
title: IMFTopology::GetNodeByID (mfidl.h)
description: Gets a node in the topology, specified by node identifier.
helpviewer_keywords: ["34c8326f-bd34-4bf6-9171-a1ed3191b85e","GetNodeByID","GetNodeByID method [Media Foundation]","GetNodeByID method [Media Foundation]","IMFTopology interface","IMFTopology interface [Media Foundation]","GetNodeByID method","IMFTopology.GetNodeByID","IMFTopology::GetNodeByID","mf.imftopology_getnodebyid","mfidl/IMFTopology::GetNodeByID"]
old-location: mf\imftopology_getnodebyid.htm
tech.root: mf
ms.assetid: 34c8326f-bd34-4bf6-9171-a1ed3191b85e
ms.date: 12/05/2018
ms.keywords: 34c8326f-bd34-4bf6-9171-a1ed3191b85e, GetNodeByID, GetNodeByID method [Media Foundation], GetNodeByID method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],GetNodeByID method, IMFTopology.GetNodeByID, IMFTopology::GetNodeByID, mf.imftopology_getnodebyid, mfidl/IMFTopology::GetNodeByID
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
 - IMFTopology::GetNodeByID
 - mfidl/IMFTopology::GetNodeByID
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
 - IMFTopology.GetNodeByID
---

# IMFTopology::GetNodeByID


## -description

Gets a node in the topology, specified by node identifier.

## -parameters

### -param qwTopoNodeID [in]

The identifier of the node to retrieve. To get a node's identifier, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid">IMFTopologyNode::GetTopoNodeID</a>.

### -param ppNode [out]

Receives a pointer to the node's <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface. The caller must release the interface.

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
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The topology does not contain a node with this identifier.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a>



<a href="/windows/desktop/medfound/topoid">TOPOID</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>