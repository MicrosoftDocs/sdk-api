---
UID: NF:bdaiface.IBDA_Topology.GetControlNode
title: IBDA_Topology::GetControlNode (bdaiface.h)
description: The GetControlNode method retrieves an IUnknown interface pointer for a specified control node.
helpviewer_keywords: ["GetControlNode","GetControlNode method [Microsoft TV Technologies]","GetControlNode method [Microsoft TV Technologies]","IBDA_Topology interface","IBDA_Topology interface [Microsoft TV Technologies]","GetControlNode method","IBDA_Topology.GetControlNode","IBDA_Topology::GetControlNode","IBDA_TopologyGetControlNode","bdaiface/IBDA_Topology::GetControlNode","mstv.ibda_topology_getcontrolnode"]
old-location: mstv\ibda_topology_getcontrolnode.htm
tech.root: mstv
ms.assetid: eff76633-10c0-4f71-a267-b2e454dcfa6c
ms.date: 12/05/2018
ms.keywords: GetControlNode, GetControlNode method [Microsoft TV Technologies], GetControlNode method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],GetControlNode method, IBDA_Topology.GetControlNode, IBDA_Topology::GetControlNode, IBDA_TopologyGetControlNode, bdaiface/IBDA_Topology::GetControlNode, mstv.ibda_topology_getcontrolnode
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
 - IBDA_Topology::GetControlNode
 - bdaiface/IBDA_Topology::GetControlNode
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
 - IBDA_Topology.GetControlNode
---

# IBDA_Topology::GetControlNode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetControlNode</b> method retrieves an <b>IUnknown</b> interface pointer for a specified control node.

## -parameters

### -param ulInputPinId [in]

Specifies the identifier of the input pin for which a topology should be created.

### -param ulOutputPinId [in]

Specifies the identifier of the output pin for which a topology should be created.

### -param ulNodeType [in]

The type of node to be opened.

### -param ppControlNode [out]

Pointer to a pointer to the control node's <b>IUnknown</b> interface

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>