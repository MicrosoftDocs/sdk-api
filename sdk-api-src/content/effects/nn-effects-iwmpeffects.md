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

# IWMPEffects interface


## -description




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPEffects</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPEffects</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPEffects</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dadde782-577d-4dcb-b8ae-2f6ddca77a40">DisplayPropertyPage</a>
</td>
<td align="left" width="63%">
Displays the property page of a visualization, if it exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451391">GetCapabilities</a>
</td>
<td align="left" width="63%">
Gets the capabilities of the visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09ad671b-612d-4e00-8fa9-d9d76954a010">GetCurrentPreset</a>
</td>
<td align="left" width="63%">
Gets the current preset by number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6eee859b-8f39-4951-814a-41913df152db">GetPresetCount</a>
</td>
<td align="left" width="63%">
Gets the preset count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73e80221-2170-4724-b902-5c30796cb6a4">GetPresetTitle</a>
</td>
<td align="left" width="63%">
Gets the title of the current preset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/051a0d25-0773-4b9d-879e-5cc60633e406">GetTitle</a>
</td>
<td align="left" width="63%">
Gets the display title of the visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daf69206-5756-4504-9738-e16b9af39790">GoFullscreen</a>
</td>
<td align="left" width="63%">
Instructs the visualization to switch to full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1267cb11-1b45-4f38-ad3c-02213405ed66">MediaInfo</a>
</td>
<td align="left" width="63%">
Sends channel and sample-rate data to the visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9040c309-5e45-41d2-9a02-b17c6d764f59">Render</a>
</td>
<td align="left" width="63%">
Renders the visualization

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08b170fd-b40a-4beb-8c18-0a011b9486af">RenderFullScreen</a>
</td>
<td align="left" width="63%">
Renders the visualization in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/090e5f9b-e7f1-48b6-9018-3d0797493d42">SetCurrentPreset</a>
</td>
<td align="left" width="63%">
Sets the current preset by number.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b76cd0a2-7c15-468e-9673-7e607a208ddd">Custom Visualization Programming Reference</a>



<a href="https://msdn.microsoft.com/44e044c1-97fd-43cb-9530-4556e485f5ae">IWMPEffects2 Interface</a>
 

 

