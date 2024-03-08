---
UID: NF:bdaiface.IBDA_Topology.SetMedium
title: IBDA_Topology::SetMedium (bdaiface.h)
description: The SetMedium method configures the medium on which a particular pin sends data.
helpviewer_keywords: ["IBDA_Topology interface [Microsoft TV Technologies]","SetMedium method","IBDA_Topology.SetMedium","IBDA_Topology::SetMedium","IBDA_TopologySetMedium","SetMedium","SetMedium method [Microsoft TV Technologies]","SetMedium method [Microsoft TV Technologies]","IBDA_Topology interface","bdaiface/IBDA_Topology::SetMedium","mstv.ibda_topology_setmedium"]
old-location: mstv\ibda_topology_setmedium.htm
tech.root: mstv
ms.assetid: e2997929-d0a9-4732-8a8f-8f94c413fae5
ms.date: 12/05/2018
ms.keywords: IBDA_Topology interface [Microsoft TV Technologies],SetMedium method, IBDA_Topology.SetMedium, IBDA_Topology::SetMedium, IBDA_TopologySetMedium, SetMedium, SetMedium method [Microsoft TV Technologies], SetMedium method [Microsoft TV Technologies],IBDA_Topology interface, bdaiface/IBDA_Topology::SetMedium, mstv.ibda_topology_setmedium
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
 - IBDA_Topology::SetMedium
 - bdaiface/IBDA_Topology::SetMedium
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
 - IBDA_Topology.SetMedium
---

# IBDA_Topology::SetMedium


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetMedium</b> method configures the medium on which a particular pin sends data.

## -parameters

### -param ulPinId [in]

Specifies the identifier of the pin on which to set the medium.

### -param pMedium [in]

Pointer to the medium on which the pin will send data.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

A medium is a structure that identifies a hardware data path between two devices on the host system. They can be devices on the same card, such as a crossbar and a tuner on a TV card; devices on separate cards; or external devices. Kernel-mode filters based on the Windows Driver Model can use mediums instead of media types to determine pin connections.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>