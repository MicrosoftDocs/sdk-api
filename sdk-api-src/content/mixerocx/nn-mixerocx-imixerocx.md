---
UID: NN:mixerocx.IMixerOCX
title: IMixerOCX
author: windows-sdk-content
description: The IMixerOCX interface is implemented on the Overlay Mixer.
old-location: dshow\imixerocx.htm
tech.root: DirectShow
ms.assetid: b80d720d-921d-4d24-a168-49944cfcc411
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMixerOCX, IMixerOCX interface [DirectShow], IMixerOCX interface [DirectShow],described, IMixerOCXInterface, dshow.imixerocx, mixerocx/IMixerOCX
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mixerocx.h
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
 - IMixerOCX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMixerOCX interface


## -description



The <code>IMixerOCX</code> interface is implemented on the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a>. This interface enables clients that do not own their own windows, such as an ActiveX control, to set properties of the video rectangle and advise the filter of events.

<div class="alert"><b>Note</b>  Applications should generally use the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9) and not the Overlay Mixer. The only scenario that requires the Overlay Mixer is when the video capture or decoder hardware uses video ports to transfer video data to the graphics card. The VMR-9 does not support video ports.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMixerOCX</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMixerOCX</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMixerOCX</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6708fc46-19cb-4843-9c9d-99ff67ee6d08">Advise</a>
</td>
<td align="left" width="63%">
Provides the Overlay Mixer with a pointer to the client's <a href="https://msdn.microsoft.com/b73416c0-2312-4164-8a6d-f8776dc1447f">IMixerOCXNotify</a> interface for callback notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6143ba3c-6472-47d3-b3ca-55c06ca8da0e">GetAspectRatio</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2be28eec-99cd-4a4e-91fc-77bb51ec6fb3">GetStatus</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4cc71b6-23a5-4610-ac59-06484af6d0b4">GetVideoSize</a>
</td>
<td align="left" width="63%">
Retrieves the current size of the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d082ab6-6195-417b-ad0d-b8e97561b268">OnDisplayChange</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69b8752b-9f97-422e-8a9a-f49c7a472cb6">OnDraw</a>
</td>
<td align="left" width="63%">
Instructs the Overlay Mixer to draw the video rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f1a9b00-4a35-4772-a185-59b2bc9b9398">SetDrawRegion</a>
</td>
<td align="left" width="63%">
Specifies the location and dimensions of the video and clipping rectangles in screen coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c2837c6-ee0f-45f4-b98a-9b8957e75b48">UnAdvise</a>
</td>
<td align="left" width="63%">
Instructs the Overlay Mixer to release its pointer to the client's <b>IMixerOCXNotify</b> interface.

</td>
</tr>
</table> 

