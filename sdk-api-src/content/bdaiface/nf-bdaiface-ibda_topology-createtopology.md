---
UID: NF:bdaiface.IBDA_Topology.CreateTopology
title: IBDA_Topology::CreateTopology (bdaiface.h)
description: The CreateTopology method associates an instance of an input pin with an instance of an output pin.
helpviewer_keywords: ["CreateTopology","CreateTopology method [Microsoft TV Technologies]","CreateTopology method [Microsoft TV Technologies]","IBDA_Topology interface","IBDA_Topology interface [Microsoft TV Technologies]","CreateTopology method","IBDA_Topology.CreateTopology","IBDA_Topology::CreateTopology","IBDA_TopologyCreateTopology","bdaiface/IBDA_Topology::CreateTopology","mstv.ibda_topology_createtopology"]
old-location: mstv\ibda_topology_createtopology.htm
tech.root: mstv
ms.assetid: 6c91e614-b1b4-4cf5-90d2-15823e5952cb
ms.date: 12/05/2018
ms.keywords: CreateTopology, CreateTopology method [Microsoft TV Technologies], CreateTopology method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],CreateTopology method, IBDA_Topology.CreateTopology, IBDA_Topology::CreateTopology, IBDA_TopologyCreateTopology, bdaiface/IBDA_Topology::CreateTopology, mstv.ibda_topology_createtopology
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
 - IBDA_Topology::CreateTopology
 - bdaiface/IBDA_Topology::CreateTopology
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
 - IBDA_Topology.CreateTopology
---

# IBDA_Topology::CreateTopology


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>CreateTopology</b> method associates an instance of an input pin with an instance of an output pin.

## -parameters

### -param ulInputPinId [in]

Specifies the identifier of the input pin for which a topology should be created.

### -param ulOutputPinId [in]

Specifies the identifier of the output pin for which a topology should be created.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>