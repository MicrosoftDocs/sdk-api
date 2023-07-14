---
UID: NF:bdaiface.IBDA_Topology.GetPinTypes
title: IBDA_Topology::GetPinTypes (bdaiface.h)
description: The GetPinTypes method retrieves a list of all the pin types in the template topology for this filter and network type.
helpviewer_keywords: ["GetPinTypes","GetPinTypes method [Microsoft TV Technologies]","GetPinTypes method [Microsoft TV Technologies]","IBDA_Topology interface","IBDA_Topology interface [Microsoft TV Technologies]","GetPinTypes method","IBDA_Topology.GetPinTypes","IBDA_Topology::GetPinTypes","IBDA_TopologyGetPinTypes","bdaiface/IBDA_Topology::GetPinTypes","mstv.ibda_topology_getpintypes"]
old-location: mstv\ibda_topology_getpintypes.htm
tech.root: mstv
ms.assetid: e94c5ae3-1d5f-4ca6-a09b-7190cbe2035b
ms.date: 12/05/2018
ms.keywords: GetPinTypes, GetPinTypes method [Microsoft TV Technologies], GetPinTypes method [Microsoft TV Technologies],IBDA_Topology interface, IBDA_Topology interface [Microsoft TV Technologies],GetPinTypes method, IBDA_Topology.GetPinTypes, IBDA_Topology::GetPinTypes, IBDA_TopologyGetPinTypes, bdaiface/IBDA_Topology::GetPinTypes, mstv.ibda_topology_getpintypes
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
 - IBDA_Topology::GetPinTypes
 - bdaiface/IBDA_Topology::GetPinTypes
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
 - IBDA_Topology.GetPinTypes
---

# IBDA_Topology::GetPinTypes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetPinTypes</b> method retrieves a list of all the pin types in the template topology for this filter and network type.

## -parameters

### -param pulcPinTypes [out]

Pointer to a value that receives the number of pin types in the list.

### -param ulcPinTypesMax [in]

The maximum number of pin types that can be held by the <i>rgulPinTypes</i> buffer.

### -param rgulPinTypes [out]

Pointer to a buffer to receive the list of pin types.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_topology">IBDA_Topology Interface</a>