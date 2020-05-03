---
UID: NN:effects.IWMPEffects
title: IWMPEffects (effects.h)
description: IWMPEffects interfacehelpviewer_keywords: ["EffectsInterface","IWMPEffects","IWMPEffects interface [Windows Media Player]","IWMPEffects interface [Windows Media Player]","described","effects/IWMPEffects","wmp.iwmpeffects"]
old-location: wmp\iwmpeffects.htm
tech.root: WMP
ms.assetid: 0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba
ms.date: 12/05/2018
ms.keywords: EffectsInterface, IWMPEffects, IWMPEffects interface [Windows Media Player], IWMPEffects interface [Windows Media Player],described, effects/IWMPEffects, wmp.iwmpeffects
f1_keywords:
- effects/IWMPEffects
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- effects.h
api_name:
- IWMPEffects
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEffects interface


## -description




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPEffects</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPEffects</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage">DisplayPropertyPage</a>
</td>
<td align="left" width="63%">
Displays the property page of a visualization, if it exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Gets the capabilities of the visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset">GetCurrentPreset</a>
</td>
<td align="left" width="63%">
Gets the current preset by number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount">GetPresetCount</a>
</td>
<td align="left" width="63%">
Gets the preset count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle">GetPresetTitle</a>
</td>
<td align="left" width="63%">
Gets the title of the current preset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle">GetTitle</a>
</td>
<td align="left" width="63%">
Gets the display title of the visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen">GoFullscreen</a>
</td>
<td align="left" width="63%">
Instructs the visualization to switch to full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo">MediaInfo</a>
</td>
<td align="left" width="63%">
Sends channel and sample-rate data to the visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-render">Render</a>
</td>
<td align="left" width="63%">
Renders the visualization

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen">RenderFullScreen</a>
</td>
<td align="left" width="63%">
Renders the visualization in full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset">SetCurrentPreset</a>
</td>
<td align="left" width="63%">
Sets the current preset by number.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/custom-visualization-programming-reference">Custom Visualization Programming Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/effects/nn-effects-iwmpeffects2">IWMPEffects2 Interface</a>
 

 

