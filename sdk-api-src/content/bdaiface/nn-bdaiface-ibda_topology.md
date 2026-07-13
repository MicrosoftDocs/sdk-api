---
UID: NN:bdaiface.IBDA_Topology
title: IBDA_Topology (bdaiface.h)
description: The IBDA_Topology interface is implemented on BDA device filters.
helpviewer_keywords: ["IBDA_Topology","IBDA_Topology interface [Microsoft TV Technologies]","IBDA_Topology interface [Microsoft TV Technologies]","described","IBDA_TopologyInterface","bdaiface/IBDA_Topology","mstv.ibda_topology"]
old-location: mstv\ibda_topology.htm
tech.root: mstv
ms.assetid: 35dfe39e-05b4-4c7b-9358-081429b064f2
ms.date: 12/05/2018
ms.keywords: IBDA_Topology, IBDA_Topology interface [Microsoft TV Technologies], IBDA_Topology interface [Microsoft TV Technologies],described, IBDA_TopologyInterface, bdaiface/IBDA_Topology, mstv.ibda_topology
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
 - IBDA_Topology
 - bdaiface/IBDA_Topology
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
 - IBDA_Topology
---

# IBDA_Topology interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IBDA_Topology</b> interface is implemented on BDA device filters. A single filter may represent multiple hardware devices (called control nodes) which may be connected in various ways within the filter itself. These connections generally represent hardware paths on the card. This interface provides methods that enable a Network Provider to configure or discover the types of nodes within the filter, and how these nodes are connected. The methods correspond closely to the Ring 0 property sets which are documented in the Windows DDK.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.

## -inheritance

The <b>IBDA_Topology</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_Topology</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_Topology)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
