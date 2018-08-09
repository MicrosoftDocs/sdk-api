---
UID: NN:effects.IWMPEffects2
title: IWMPEffects2
author: windows-sdk-content
description: IWMPEffects2 interface
old-location: wmp\iwmpeffects2.htm
old-project: WMP
ms.assetid: 44e044c1-97fd-43cb-9530-4556e485f5ae
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPEffects2, IWMPEffects2 interface [Windows Media Player], IWMPEffects2 interface [Windows Media Player],described, IWMPEffects2Interface, effects/IWMPEffects2, wmp.iwmpeffects2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: effects.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

