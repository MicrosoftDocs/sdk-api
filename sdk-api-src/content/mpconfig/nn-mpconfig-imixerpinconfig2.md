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

# IMixerPinConfig2 interface


## -description



The <code>IMixerPinConfig2</code> interface is exposed on the input pins of the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> and contains methods that manipulate video color controls, if the VGA chip supports it.

This interface derives from the <a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig</a> interface.

Applications use this interface to get and set video color controls when mixing multiple video streams.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMixerPinConfig2</b> interface inherits from <a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig</a>. <b>IMixerPinConfig2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMixerPinConfig2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6b47e4d-5bf2-4d76-a1e2-88a3342d75a6">GetOverlaySurfaceColorControls</a>
</td>
<td align="left" width="63%">
Retrieves the color control settings currently associated with the specified overlay surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c23c12c9-5621-4b1e-997a-51303f239175">SetOverlaySurfaceColorControls</a>
</td>
<td align="left" width="63%">
Sets the color control settings associated with the specified overlay surface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig</a>
 

 

