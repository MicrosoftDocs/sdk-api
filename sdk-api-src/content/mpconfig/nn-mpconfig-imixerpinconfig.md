---
UID: NN:mpconfig.IMixerPinConfig
title: IMixerPinConfig
author: windows-sdk-content
description: The IMixerPinConfig interface is exposed on the input pins of the Overlay Mixer filter and contains methods that manipulate video streams in various ways.
old-location: dshow\imixerpinconfig.htm
old-project: DirectShow
ms.assetid: 6a4f3462-4596-4f02-a41f-47161f8aa4db
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IMixerPinConfig, IMixerPinConfig interface [DirectShow], IMixerPinConfig interface [DirectShow],described, IMixerPinConfigInterface, dshow.imixerpinconfig, mpconfig/IMixerPinConfig
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
tech.root: 
req.typenames: AM_ASPECT_RATIO_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerPinConfig
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerPinConfig interface


## -description



The <code>IMixerPinConfig</code> interface is exposed on the input pins of the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter and contains methods that manipulate video streams in various ways. The Overlay Mixer contains multiple input pins that are dynamically created as video input streams are added. The video stream on the first pin is known as the <i>primary stream</i> and subsequent streams are known as <i>secondary streams</i>.

Use this interface to manipulate the parameters involved in mixing various video streams. These parameters include getting and setting position, z-order, blending and transparency levels, aspect ratio correction, and color keys of streams.

When setting the position of video streams in the display window, the default relative position of all secondary streams is {0, 0, 0, 0}. Therefore, use the <a href="https://msdn.microsoft.com/2b8ff58b-04df-4a6a-b501-f5c138b8abbf">IMixerPinConfig::SetRelativePosition</a> method on secondary streams to ensure that all video streams are placed properly.

Applications use this interface to get and set attributes when mixing multiple video streams.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMixerPinConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMixerPinConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMixerPinConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/091ebea0-8688-4965-8727-0738cc19d47e">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Retrieves the aspect ratio correction mode for window resizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcd54b8d-d742-4ac0-bcea-8de77b7f0074">GetBlendingParameter</a>
</td>
<td align="left" width="63%">
Retrieves the value of the blending parameter that defines how a secondary stream is blended with a primary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07e97d05-f273-4e93-8da8-838975d6f96c">GetColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the color key being used by a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a2bcc3e-361d-4374-9444-717287c07116">GetRelativePosition</a>
</td>
<td align="left" width="63%">
Retrieves the position of the stream in the display window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5089a2b3-2973-4761-82f6-f6af3ac9f560">GetZOrder</a>
</td>
<td align="left" width="63%">
Retrieves the z-order of a particular video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/907ab0cf-c0a4-4e81-8fb4-90914427d9c0">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Sets the aspect ratio correction mode for window resizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/262814eb-386b-409e-b22c-48f9f2a845b4">SetBlendingParameter</a>
</td>
<td align="left" width="63%">
Sets the blending parameter that defines how a secondary stream is blended with a primary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2d4ffa2-0b10-4bc5-9af1-83f4ee68b35f">SetColorKey</a>
</td>
<td align="left" width="63%">
Sets the color key being used by a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b8ff58b-04df-4a6a-b501-f5c138b8abbf">SetRelativePosition</a>
</td>
<td align="left" width="63%">
Sets the position of the stream in the display window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1f60a35-ffef-4ebb-b331-558772310bcb">SetStreamTransparent</a>
</td>
<td align="left" width="63%">
Sets the stream to transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1f60a35-ffef-4ebb-b331-558772310bcb">SetStreamTransparent</a>
</td>
<td align="left" width="63%">
Determines whether a stream is transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe8e71b8-9aaf-438e-b370-5ba9f131bf7a">SetZOrder</a>
</td>
<td align="left" width="63%">
Sets the z-order of a particular video stream.

</td>
</tr>
</table> 

