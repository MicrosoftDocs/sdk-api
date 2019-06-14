---
UID: NN:mfidl.IMFTopology
title: IMFTopology (mfidl.h)
author: windows-sdk-content
description: Represents a topology. A topology describes a collection of media sources, sinks, and transforms that are connected in a certain order.
old-location: mf\imftopology.htm
tech.root: medfound
ms.assetid: f293e9ee-9bd2-4b3e-a4ff-53457ee910f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFTopology, IMFTopology interface [Media Foundation], IMFTopology interface [Media Foundation],described, f293e9ee-9bd2-4b3e-a4ff-53457ee910f6, mf.imftopology, mfidl/IMFTopology
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopology
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTopology interface


## -description


Represents a topology. A <i>topology</i> describes a collection of media sources, sinks, and transforms that are connected in a certain order. These objects are represented within the topology by <i>topology nodes</i>, which expose the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface. A topology describes the path of multimedia data through these nodes.

To create a topology, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology">MFCreateTopology</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopology</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFTopology</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTopology</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode">AddNode</a>
</td>
<td align="left" width="63%">
Adds a node to the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all nodes from the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-clonefrom">CloneFrom</a>
</td>
<td align="left" width="63%">
Converts this topology into a copy of another topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnode">GetNode</a>
</td>
<td align="left" width="63%">
Gets a node in the topology, specified by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid">GetNodeByID</a>
</td>
<td align="left" width="63%">
Gets a node in the topology, specified by node identifier.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodecount">GetNodeCount</a>
</td>
<td align="left" width="63%">
Gets the number of nodes in the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection">GetOutputNodeCollection</a>
</td>
<td align="left" width="63%">
Gets the output nodes in the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-getsourcenodecollection">GetSourceNodeCollection</a>
</td>
<td align="left" width="63%">
Gets the source nodes in the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid">GetTopologyID</a>
</td>
<td align="left" width="63%">
Gets the identifier of the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopology-removenode">RemoveNode</a>
</td>
<td align="left" width="63%">
Removes a node from the topology.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topologies">Topologies</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topology-attributes">Topology Attributes</a>
 

 

