---
UID: NN:mfidl.IMFTopology
title: IMFTopology
author: windows-sdk-content
description: Represents a topology. A topology describes a collection of media sources, sinks, and transforms that are connected in a certain order.
old-location: mf\imftopology.htm
tech.root: medfound
ms.assetid: f293e9ee-9bd2-4b3e-a4ff-53457ee910f6
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMFTopology, IMFTopology interface [Media Foundation], IMFTopology interface [Media Foundation],described, f293e9ee-9bd2-4b3e-a4ff-53457ee910f6, mf.imftopology, mfidl/IMFTopology
ms.prod: windows
ms.technology: windows-sdk
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
---

# IMFTopology interface


## -description


Represents a topology. A <i>topology</i> describes a collection of media sources, sinks, and transforms that are connected in a certain order. These objects are represented within the topology by <i>topology nodes</i>, which expose the <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface. A topology describes the path of multimedia data through these nodes.

To create a topology, call <a href="https://msdn.microsoft.com/9811eca7-e822-4ff7-93e4-2eb6245d4490">MFCreateTopology</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopology</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFTopology</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5e519524-f5c5-4d4d-922f-166f9e616631">AddNode</a>
</td>
<td align="left" width="63%">
Adds a node to the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/919a712f-3f1b-4681-9eeb-958ac349d8f6">Clear</a>
</td>
<td align="left" width="63%">
Removes all nodes from the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b455aa57-9785-4741-bc3b-1f99cbf4e3d9">CloneFrom</a>
</td>
<td align="left" width="63%">
Converts this topology into a copy of another topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97053d10-5ac7-40c0-b46b-77d401284d58">GetNode</a>
</td>
<td align="left" width="63%">
Gets a node in the topology, specified by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34c8326f-bd34-4bf6-9171-a1ed3191b85e">GetNodeByID</a>
</td>
<td align="left" width="63%">
Gets a node in the topology, specified by node identifier.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87378088-1d7a-4ad7-942f-69b6cfc4e573">GetNodeCount</a>
</td>
<td align="left" width="63%">
Gets the number of nodes in the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0862cd4a-4d22-4d8d-a754-0cd376d44b22">GetOutputNodeCollection</a>
</td>
<td align="left" width="63%">
Gets the output nodes in the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9da7d4cd-ad83-4d64-9773-699f39625056">GetSourceNodeCollection</a>
</td>
<td align="left" width="63%">
Gets the source nodes in the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7d33d20-1b58-4b88-9a98-1004a5c42dfa">GetTopologyID</a>
</td>
<td align="left" width="63%">
Gets the identifier of the topology.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dbafd3f-315b-4135-aecd-ad46f2c19886">RemoveNode</a>
</td>
<td align="left" width="63%">
Removes a node from the topology.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>



<a href="https://msdn.microsoft.com/50102096-a29f-4c00-a685-179ba5d71089">Topology Attributes</a>
 

 

