---
UID: NF:bdaiface.IBDA_Topology.GetNodeTypes
title: IBDA_Topology::GetNodeTypes (bdaiface.h)
description: The GetNodeTypes method retrieves a list of all the node types in the template topology for this filter and network type.
helpviewer_keywords: ["GetNodeTypes","GetNodeTypes method [Microsoft TV Technologies]","GetNodeTypes method [Microsoft TV Technologies]","IBDA_Topology interface","IBDA_Topology interface [Microsoft TV Technologies]","GetNodeTypes method","IBDA_Topology.GetNodeTypes","IBDA_Topology::GetNodeTypes","IBDA_TopologyGetNodeTypes","bdaiface/IBDA_Topology::GetNodeTypes","mstv.ibda_topology_getnodetypes"]
old-location: mstv\ibda_topology_getnodetypes.htm
tech.root: mstv
ms.assetid: 6912cd69-76c2-4dae-bda3-42139acffe4c
ms.date: 12/05/2018
ms.keywords: GetNodeTypes, GetNodeTypes method [Microsoft TV Technologies], GetNodeTypes method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],GetNodeTypes method, IBDA_Topology.GetNodeTypes, IBDA_Topology::GetNodeTypes, IBDA_TopologyGetNodeTypes, bdaiface/IBDA_Topology::GetNodeTypes, mstv.ibda_topology_getnodetypes
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
 - IBDA_Topology::GetNodeTypes
 - bdaiface/IBDA_Topology::GetNodeTypes
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
 - IBDA_Topology.GetNodeTypes
---

# IBDA_Topology::GetNodeTypes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetNodeTypes</b> method retrieves a list of all the node types in the template topology for this filter and network type.

## -parameters

### -param pulcNodeTypes [out]

Pointer that receives the number of node types in the list.

### -param ulcNodeTypesMax [in]

The maximum number of node types that can be held by the <i>rgulNodeTypes</i> buffer.

### -param rgulNodeTypes [out]

Pointer to a buffer that receives the list of node types.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The <b>IBDA_Topology</b> interface is implemented by a BDA Device Filter. It is used by a Network Provider to query a BDA Device Filter's possible topologies (template topology) and to configure the device with an appropriate topology for the current tuning request. It is also used to get an <b>IUnknown</b> to a control node which may be used to set specific tuning information.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>