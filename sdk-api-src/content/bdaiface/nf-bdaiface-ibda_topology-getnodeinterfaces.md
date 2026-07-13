---
UID: NF:bdaiface.IBDA_Topology.GetNodeInterfaces
title: IBDA_Topology::GetNodeInterfaces (bdaiface.h)
description: The GetNodeInterfaces method retrieves a list of the interfaces supported by a node type.
helpviewer_keywords: ["GetNodeInterfaces","GetNodeInterfaces method [Microsoft TV Technologies]","GetNodeInterfaces method [Microsoft TV Technologies]","IBDA_Topology interface","IBDA_Topology interface [Microsoft TV Technologies]","GetNodeInterfaces method","IBDA_Topology.GetNodeInterfaces","IBDA_Topology::GetNodeInterfaces","IBDA_TopologyGetNodeInterfaces","bdaiface/IBDA_Topology::GetNodeInterfaces","mstv.ibda_topology_getnodeinterfaces"]
old-location: mstv\ibda_topology_getnodeinterfaces.htm
tech.root: mstv
ms.assetid: c3dc4b38-933c-4aeb-b6eb-7273ce334ba2
ms.date: 12/05/2018
ms.keywords: GetNodeInterfaces, GetNodeInterfaces method [Microsoft TV Technologies], GetNodeInterfaces method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],GetNodeInterfaces method, IBDA_Topology.GetNodeInterfaces, IBDA_Topology::GetNodeInterfaces, IBDA_TopologyGetNodeInterfaces, bdaiface/IBDA_Topology::GetNodeInterfaces, mstv.ibda_topology_getnodeinterfaces
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_Topology::GetNodeInterfaces
 - bdaiface/IBDA_Topology::GetNodeInterfaces
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_Topology.GetNodeInterfaces
---

# IBDA_Topology::GetNodeInterfaces


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetNodeInterfaces</b> method retrieves a list of the interfaces supported by a node type.

## -parameters

### -param ulNodeType [in]

Specifies the node type for which the interface list is being requested.

### -param pulcInterfaces [out]

Pointer that receives the number of interfaces in the list.

### -param ulcInterfacesMax [in]

Specifies the maximum number of interfaces that <i>rgguidInterfaces</i> can hold.

### -param rgguidInterfaces [out]

Pointer to a buffer that holds the list of interface GUIDs.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>