---
UID: NN:effects.IWMPEffects2
title: IWMPEffects2 (effects.h)
description: IWMPEffects2 interface
helpviewer_keywords: ["IWMPEffects2","IWMPEffects2 interface [Windows Media Player]","IWMPEffects2 interface [Windows Media Player]","described","IWMPEffects2Interface","effects/IWMPEffects2","wmp.iwmpeffects2"]
old-location: wmp\iwmpeffects2.htm
tech.root: WMP
ms.assetid: 44e044c1-97fd-43cb-9530-4556e485f5ae
ms.date: 12/05/2018
ms.keywords: IWMPEffects2, IWMPEffects2 interface [Windows Media Player], IWMPEffects2 interface [Windows Media Player],described, IWMPEffects2Interface, effects/IWMPEffects2, wmp.iwmpeffects2
f1_keywords:
- effects/IWMPEffects2
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
- IWMPEffects2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEffects2 interface


## -description

The IWMPEffects2 interface.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPEffects2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects</a>. <b>IWMPEffects2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects2-create">Create</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to instantiate a visualization window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy">Destroy</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to destroy a visualization window instantiated in the <b>Create</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia">NotifyNewMedia</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to inform the visualization that a new media item has been loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage">OnWindowMessage</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to pass window messages to a visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed">RenderWindowed</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to render a windowed visualization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore">SetCore</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to provide visualization access to the core Windows Media Player APIs.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/custom-visualization-programming-reference">Custom Visualization Programming Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>