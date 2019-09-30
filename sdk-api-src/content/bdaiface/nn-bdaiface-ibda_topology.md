---
UID: NN:bdaiface.IBDA_Topology
title: IBDA_Topology (bdaiface.h)
author: windows-sdk-content
description: The IBDA_Topology interface is implemented on BDA device filters.
old-location: mstv\ibda_topology.htm
tech.root: mstv
ms.assetid: 35dfe39e-05b4-4c7b-9358-081429b064f2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBDA_Topology, IBDA_Topology interface [Microsoft TV Technologies], IBDA_Topology interface [Microsoft TV Technologies],described, IBDA_TopologyInterface, bdaiface/IBDA_Topology, mstv.ibda_topology
ms.topic: interface
f1_keywords: 
 - "bdaiface/IBDA_Topology"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_Topology
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_Topology interface


## -description



The <b>IBDA_Topology</b> interface is implemented on BDA device filters. A single filter may represent multiple hardware devices (called control nodes) which may be connected in various ways within the filter itself. These connections generally represent hardware paths on the card. This interface provides methods that enable a Network Provider to configure or discover the types of nodes within the filter, and how these nodes are connected. The methods correspond closely to the Ring 0 property sets which are documented in the Windows DDK.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_Topology</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_Topology</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_Topology</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-createpin">CreatePin</a>
</td>
<td align="left" width="63%">
Creates an instance of a specified pin type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-createtopology">CreateTopology</a>
</td>
<td align="left" width="63%">
Associates an instance of an input pin with an instance of an output pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-deletepin">DeletePin</a>
</td>
<td align="left" width="63%">
Deletes a pin from the filter's topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-getcontrolnode">GetControlNode</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IUnknown</b> interface pointer for a specified control node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-getnodedescriptors">GetNodeDescriptors</a>
</td>
<td align="left" width="63%">
Retrieves a list of descriptors for the nodes in the topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-getnodeinterfaces">GetNodeInterfaces</a>
</td>
<td align="left" width="63%">
Retrieves a list of the interfaces supported by a node type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-getnodetypes">GetNodeTypes</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the node types in the template topology for this filter and network type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-getpintypes">GetPinTypes</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the pin types in the template topology for this filter and network type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-gettemplateconnections">GetTemplateConnections</a>
</td>
<td align="left" width="63%">
Retrieves a list of all template connections that appear in the template topology for this filter and network type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-setmediatype">SetMediaType</a>
</td>
<td align="left" width="63%">
Configures the media types that can be accepted by a particular pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_topology-setmedium">SetMedium</a>
</td>
<td align="left" width="63%">
Configures the media types that can be accepted by a particular pin.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_Topology)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

