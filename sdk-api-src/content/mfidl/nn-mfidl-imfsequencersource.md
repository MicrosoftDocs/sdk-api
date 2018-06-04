---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMFSequencerSource interface


## -description


Implemented by the <a href="https://msdn.microsoft.com/788ede68-2fd7-45f6-90cb-2426c40f7d4c">Sequencer Source</a>. The sequencer source enables an application to create a sequence of topologies. To create the sequencer source, call <a href="https://msdn.microsoft.com/e4640731-f262-4ceb-8d17-908c2c6b192e">MFCreateSequencerSource</a>. For step-by-step instructions about how to create a playlist, see <a href="https://msdn.microsoft.com/5a760492-bd52-40b8-a652-8a62646db6ae">How to Create a Playlist</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSequencerSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSequencerSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSequencerSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ff20d56-6095-495d-89ee-9086c61da8ac">AppendTopology</a>
</td>
<td align="left" width="63%">
Adds a topology to the end of the queue of topologies.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ef3512d-f953-46a3-8604-bec3904a962f">DeleteTopology</a>
</td>
<td align="left" width="63%">
Deletes a topology from the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c444ccad-68b8-40eb-9e87-0b4d61ac725d">GetPresentationContext</a>
</td>
<td align="left" width="63%">
Maps a presentation descriptor to its associated sequencer element identifier and topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ed6be6c-a031-4628-a3c5-7f0676cc0baf">UpdateTopology</a>
</td>
<td align="left" width="63%">
Updates a topology in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee71b574-0456-4091-bbb0-da5c57a7506e">UpdateTopologyFlags</a>
</td>
<td align="left" width="63%">
Updates the flags for a topology in the queue.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/788ede68-2fd7-45f6-90cb-2426c40f7d4c">Sequencer Source</a>
 

 

