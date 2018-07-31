---
UID: NN:strmif.IAMOverlayFX
title: IAMOverlayFX
author: windows-sdk-content
description: The IAMOverlayFX interface controls how the video overlay appears on the user's screen. The Overlay Mixer filter implements this interface.
old-location: dshow\iamoverlayfx.htm
old-project: DirectShow
ms.assetid: 6bc78464-8c9e-4016-b9aa-6589d53d45bf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAMOverlayFX, IAMOverlayFX interface [DirectShow], IAMOverlayFX interface [DirectShow],described, IAMOverlayFXInterface, dshow.iamoverlayfx, strmif/IAMOverlayFX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMOverlayFX
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMOverlayFX interface


## -description



The <code>IAMOverlayFX</code> interface controls how the video overlay appears on the user's screen. The <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMOverlayFX</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMOverlayFX</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMOverlayFX</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8232fcf-a0d8-4155-941e-8613c09b4bbf">GetOverlayFX</a>
</td>
<td align="left" width="63%">
Retrieves the effects currently applied to the overlay surface, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01fdbe3d-bec7-4e66-87c5-b7e6c1044e8a">QueryOverlayFXCaps</a>
</td>
<td align="left" width="63%">
Retrieves information about which overlay effects are available to the Overlay Mixer filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08e44f4e-924a-4a4d-9fc5-c13b3c21c038">SetOverlayFX</a>
</td>
<td align="left" width="63%">
Applies the specified effects to the overlay surface.

</td>
</tr>
</table> 

