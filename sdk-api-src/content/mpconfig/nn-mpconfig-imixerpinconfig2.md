---
UID: NN:mpconfig.IMixerPinConfig2
title: IMixerPinConfig2 (mpconfig.h)
author: windows-sdk-content
description: The IMixerPinConfig2 interface is exposed on the input pins of the Overlay Mixer and contains methods that manipulate video color controls, if the VGA chip supports it.This interface derives from the IMixerPinConfig interface.Applications use this interface to get and set video color controls when mixing multiple video streams.
old-location: dshow\imixerpinconfig2.htm
tech.root: DirectShow
ms.assetid: d166b139-3ef7-4f47-817a-8f5b644a3776
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMixerPinConfig2, IMixerPinConfig2 interface [DirectShow], IMixerPinConfig2 interface [DirectShow],described, IMixerPinConfig2Interface, dshow.imixerpinconfig2, mpconfig/IMixerPinConfig2
ms.topic: interface
f1_keywords: 
 - "mpconfig/IMixerPinConfig2"
req.header: mpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerPinConfig2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMixerPinConfig2 interface


## -description



The <code>IMixerPinConfig2</code> interface is exposed on the input pins of the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> and contains methods that manipulate video color controls, if the VGA chip supports it.

This interface derives from the <a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig</a> interface.

Applications use this interface to get and set video color controls when mixing multiple video streams.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMixerPinConfig2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig</a>. <b>IMixerPinConfig2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig2-getoverlaysurfacecolorcontrols">GetOverlaySurfaceColorControls</a>
</td>
<td align="left" width="63%">
Retrieves the color control settings currently associated with the specified overlay surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig2-setoverlaysurfacecolorcontrols">SetOverlaySurfaceColorControls</a>
</td>
<td align="left" width="63%">
Sets the color control settings associated with the specified overlay surface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig</a>
 

 

