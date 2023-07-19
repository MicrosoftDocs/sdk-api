---
UID: NF:bdaiface.IBDA_Topology.CreatePin
title: IBDA_Topology::CreatePin (bdaiface.h)
description: The CreatePin method creates an instance of a specified pin type.
helpviewer_keywords: ["CreatePin","CreatePin method [Microsoft TV Technologies]","CreatePin method [Microsoft TV Technologies]","IBDA_Topology interface","IBDA_Topology interface [Microsoft TV Technologies]","CreatePin method","IBDA_Topology.CreatePin","IBDA_Topology::CreatePin","IBDA_TopologyCreatePin","bdaiface/IBDA_Topology::CreatePin","mstv.ibda_topology_createpin"]
old-location: mstv\ibda_topology_createpin.htm
tech.root: mstv
ms.assetid: ced0f8a8-7a34-4357-8795-491e60a22e91
ms.date: 12/05/2018
ms.keywords: CreatePin, CreatePin method [Microsoft TV Technologies], CreatePin method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],CreatePin method, IBDA_Topology.CreatePin, IBDA_Topology::CreatePin, IBDA_TopologyCreatePin, bdaiface/IBDA_Topology::CreatePin, mstv.ibda_topology_createpin
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
 - IBDA_Topology::CreatePin
 - bdaiface/IBDA_Topology::CreatePin
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
 - IBDA_Topology.CreatePin
---

# IBDA_Topology::CreatePin


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>CreatePin</b> method creates an instance of a specified pin type.

## -parameters

### -param ulPinType [in]

Specifies the type of pin to create. To obtain the available values, call <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-getpintypes">IBDA_Topology::GetPinTypes</a>.

### -param pulPinId [out]

Pointer that receives the identifier for the new pin.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>