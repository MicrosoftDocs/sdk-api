---
UID: NN:mpconfig.IMixerPinConfig2
title: IMixerPinConfig2
author: windows-sdk-content
description: The IMixerPinConfig2 interface is exposed on the input pins of the Overlay Mixer and contains methods that manipulate video color controls, if the VGA chip supports it.This interface derives from the IMixerPinConfig interface.Applications use this interface to get and set video color controls when mixing multiple video streams.
old-location: dshow\imixerpinconfig2.htm
tech.root: DirectShow
ms.assetid: d166b139-3ef7-4f47-817a-8f5b644a3776
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMixerPinConfig2, IMixerPinConfig2 interface [DirectShow], IMixerPinConfig2 interface [DirectShow],described, IMixerPinConfig2Interface, dshow.imixerpinconfig2, mpconfig/IMixerPinConfig2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

