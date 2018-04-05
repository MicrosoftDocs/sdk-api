---
UID: NN:strmif.IAMResourceControl
title: IAMResourceControl
author: windows-driver-content
description: The IAMResourceControl interface opens and holds an audio device resource before the device is actually needed, so that playback can be guaranteed or the application can learn in advance that a device is not available.The following filters implement this interface:Audio Capture filter.DirectSound Renderer filter.Audio Renderer (WaveOut) filter.
old-location: dshow\iamresourcecontrol.htm
old-project: DirectShow
ms.assetid: 9b0b6b46-bf61-44c2-981a-44df4d7c6dfb
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IAMResourceControl, IAMResourceControl interface [DirectShow], IAMResourceControl interface [DirectShow], described, IAMResourceControlInterface, dshow.iamresourcecontrol, strmif/IAMResourceControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMResourceControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMResourceControl interface


## -description



The <code>IAMResourceControl</code> interface opens and holds an audio device resource before the device is actually needed, so that playback can be guaranteed or the application can learn in advance that a device is not available.

The following filters implement this interface:

<ul>
<li>
<a href="https://msdn.microsoft.com/f76d5c82-33b2-4579-9420-8f97eca53ede">Audio Capture</a> filter.</li>
<li>
<a href="https://msdn.microsoft.com/ec6cc790-8c1f-4de4-a7ca-a7073894380e">DirectSound Renderer</a> filter.</li>
<li>
<a href="https://msdn.microsoft.com/a3f2776b-974b-4886-82a3-38e00b607a07">Audio Renderer (WaveOut)</a> filter.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMResourceControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMResourceControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMResourceControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f264b87-dae4-4478-811f-1c99e670928a">Reserve</a>
</td>
<td align="left" width="63%">
Reserves or unreserves a device resource.

</td>
</tr>
</table> 

