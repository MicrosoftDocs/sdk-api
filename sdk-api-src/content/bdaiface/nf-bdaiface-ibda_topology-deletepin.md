---
UID: NF:bdaiface.IBDA_Topology.DeletePin
title: IBDA_Topology::DeletePin (bdaiface.h)
description: The DeletePin method deletes a pin from the filter's topology.
helpviewer_keywords: ["DeletePin","DeletePin method [Microsoft TV Technologies]","DeletePin method [Microsoft TV Technologies]","IBDA_Topology interface","IBDA_Topology interface [Microsoft TV Technologies]","DeletePin method","IBDA_Topology.DeletePin","IBDA_Topology::DeletePin","IBDA_TopologyDeletePin","bdaiface/IBDA_Topology::DeletePin","mstv.ibda_topology_deletepin"]
old-location: mstv\ibda_topology_deletepin.htm
tech.root: mstv
ms.assetid: 7ec81e3a-e4f2-4809-9574-8efe6240cfba
ms.date: 12/05/2018
ms.keywords: DeletePin, DeletePin method [Microsoft TV Technologies], DeletePin method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],DeletePin method, IBDA_Topology.DeletePin, IBDA_Topology::DeletePin, IBDA_TopologyDeletePin, bdaiface/IBDA_Topology::DeletePin, mstv.ibda_topology_deletepin
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
 - IBDA_Topology::DeletePin
 - bdaiface/IBDA_Topology::DeletePin
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
 - IBDA_Topology.DeletePin
---

# IBDA_Topology::DeletePin


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>DeletePin</b> method deletes a pin from the filter's topology.

## -parameters

### -param ulPinId [in]

Specifies the identifier of the pin to be deleted.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>