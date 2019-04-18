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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_Topology interface


## -description



The <b>IBDA_Topology</b> interface is implemented on BDA device filters. A single filter may represent multiple hardware devices (called control nodes) which may be connected in various ways within the filter itself. These connections generally represent hardware paths on the card. This interface provides methods that enable a Network Provider to configure or discover the types of nodes within the filter, and how these nodes are connected. The methods correspond closely to the Ring 0 property sets which are documented in the Windows DDK.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://msdn.microsoft.com/7b641b94-9854-4ca8-8362-a9e1e49bbdd2">OCUR Devices</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_Topology</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_Topology</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd693448(v=VS.85).aspx">CreatePin</a>
</td>
<td align="left" width="63%">
Creates an instance of a specified pin type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693449(v=VS.85).aspx">CreateTopology</a>
</td>
<td align="left" width="63%">
Associates an instance of an input pin with an instance of an output pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693450(v=VS.85).aspx">DeletePin</a>
</td>
<td align="left" width="63%">
Deletes a pin from the filter's topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693451(v=VS.85).aspx">GetControlNode</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IUnknown</b> interface pointer for a specified control node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693452(v=VS.85).aspx">GetNodeDescriptors</a>
</td>
<td align="left" width="63%">
Retrieves a list of descriptors for the nodes in the topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693453(v=VS.85).aspx">GetNodeInterfaces</a>
</td>
<td align="left" width="63%">
Retrieves a list of the interfaces supported by a node type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693454(v=VS.85).aspx">GetNodeTypes</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the node types in the template topology for this filter and network type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693455(v=VS.85).aspx">GetPinTypes</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the pin types in the template topology for this filter and network type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693456(v=VS.85).aspx">GetTemplateConnections</a>
</td>
<td align="left" width="63%">
Retrieves a list of all template connections that appear in the template topology for this filter and network type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693457(v=VS.85).aspx">SetMediaType</a>
</td>
<td align="left" width="63%">
Configures the media types that can be accepted by a particular pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693458(v=VS.85).aspx">SetMedium</a>
</td>
<td align="left" width="63%">
Configures the media types that can be accepted by a particular pin.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_Topology)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

