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

# IWMPEffects2 interface


## -description




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPEffects2</b> interface inherits from <a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects</a>. <b>IWMPEffects2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPEffects2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0bc4e45-7174-4dbd-a902-06c685c9a9ac">Create</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to instantiate a visualization window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dad290e6-a3be-47f0-a893-7a60eebc2a64">Destroy</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to destroy a visualization window instantiated in the <b>Create</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad1082af-9cba-4427-bacb-e552910f8e16">NotifyNewMedia</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to inform the visualization that a new media item has been loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4efdac9-b50f-4448-98f2-efe015527a4e">OnWindowMessage</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to pass window messages to a visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95a0b71e-6485-4b14-81cf-b853a664b3cc">RenderWindowed</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to render a windowed visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5afbf1d-ecb9-43d4-8396-db7c54720731">SetCore</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to provide visualization access to the core Windows Media Player APIs.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b76cd0a2-7c15-468e-9673-7e607a208ddd">Custom Visualization Programming Reference</a>



<a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects Interface</a>
 

 

