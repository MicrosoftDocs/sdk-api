---
UID: NF:mfidl.IMFTopologyNode.GetTopoNodeID
title: IMFTopologyNode::GetTopoNodeID (mfidl.h)
description: Retrieves the identifier of the node.
helpviewer_keywords: ["9c0e5be9-6481-4132-ad5b-9db13fb07391","GetTopoNodeID","GetTopoNodeID method [Media Foundation]","GetTopoNodeID method [Media Foundation]","IMFTopologyNode interface","IMFTopologyNode interface [Media Foundation]","GetTopoNodeID method","IMFTopologyNode.GetTopoNodeID","IMFTopologyNode::GetTopoNodeID","mf.imftopologynode_gettoponodeid","mfidl/IMFTopologyNode::GetTopoNodeID"]
old-location: mf\imftopologynode_gettoponodeid.htm
tech.root: mf
ms.assetid: 9c0e5be9-6481-4132-ad5b-9db13fb07391
ms.date: 12/05/2018
ms.keywords: 9c0e5be9-6481-4132-ad5b-9db13fb07391, GetTopoNodeID, GetTopoNodeID method [Media Foundation], GetTopoNodeID method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetTopoNodeID method, IMFTopologyNode.GetTopoNodeID, IMFTopologyNode::GetTopoNodeID, mf.imftopologynode_gettoponodeid, mfidl/IMFTopologyNode::GetTopoNodeID
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
 - IMFTopologyNode::GetTopoNodeID
 - mfidl/IMFTopologyNode::GetTopoNodeID
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
 - IMFTopologyNode.GetTopoNodeID
---

# IMFTopologyNode::GetTopoNodeID


## -description

Retrieves the identifier of the node.

## -parameters

### -param pID [out]

Receives the identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a node is first created, it is assigned an identifier. Node identifiers are unique within a topology, but can be reused across several topologies. The topology loader uses the identifier to look up nodes in the previous topology, so that it can reuse objects from the previous topology.
      

To find a node in a topology by its identifier, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid">IMFTopology::GetNodeByID</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topoid">TOPOID</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>