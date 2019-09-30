---
UID: NN:mpconfig.IMixerPinConfig
title: IMixerPinConfig (mpconfig.h)
author: windows-sdk-content
description: The IMixerPinConfig interface is exposed on the input pins of the Overlay Mixer filter and contains methods that manipulate video streams in various ways.
old-location: dshow\imixerpinconfig.htm
tech.root: DirectShow
ms.assetid: 6a4f3462-4596-4f02-a41f-47161f8aa4db
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMixerPinConfig, IMixerPinConfig interface [DirectShow], IMixerPinConfig interface [DirectShow],described, IMixerPinConfigInterface, dshow.imixerpinconfig, mpconfig/IMixerPinConfig
ms.topic: interface
f1_keywords: 
 - "mpconfig/IMixerPinConfig"
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
 - IMixerPinConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMixerPinConfig interface


## -description



The <code>IMixerPinConfig</code> interface is exposed on the input pins of the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter and contains methods that manipulate video streams in various ways. The Overlay Mixer contains multiple input pins that are dynamically created as video input streams are added. The video stream on the first pin is known as the <i>primary stream</i> and subsequent streams are known as <i>secondary streams</i>.

Use this interface to manipulate the parameters involved in mixing various video streams. These parameters include getting and setting position, z-order, blending and transparency levels, aspect ratio correction, and color keys of streams.

When setting the position of video streams in the display window, the default relative position of all secondary streams is {0, 0, 0, 0}. Therefore, use the <a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setrelativeposition">IMixerPinConfig::SetRelativePosition</a> method on secondary streams to ensure that all video streams are placed properly.

Applications use this interface to get and set attributes when mixing multiple video streams.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMixerPinConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMixerPinConfig</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getaspectratiomode">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Retrieves the aspect ratio correction mode for window resizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getblendingparameter">GetBlendingParameter</a>
</td>
<td align="left" width="63%">
Retrieves the value of the blending parameter that defines how a secondary stream is blended with a primary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getcolorkey">GetColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the color key being used by a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getrelativeposition">GetRelativePosition</a>
</td>
<td align="left" width="63%">
Retrieves the position of the stream in the display window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getzorder">GetZOrder</a>
</td>
<td align="left" width="63%">
Retrieves the z-order of a particular video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setaspectratiomode">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Sets the aspect ratio correction mode for window resizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setblendingparameter">SetBlendingParameter</a>
</td>
<td align="left" width="63%">
Sets the blending parameter that defines how a secondary stream is blended with a primary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setcolorkey">SetColorKey</a>
</td>
<td align="left" width="63%">
Sets the color key being used by a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setrelativeposition">SetRelativePosition</a>
</td>
<td align="left" width="63%">
Sets the position of the stream in the display window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setstreamtransparent">SetStreamTransparent</a>
</td>
<td align="left" width="63%">
Sets the stream to transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setstreamtransparent">SetStreamTransparent</a>
</td>
<td align="left" width="63%">
Determines whether a stream is transparent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setzorder">SetZOrder</a>
</td>
<td align="left" width="63%">
Sets the z-order of a particular video stream.

</td>
</tr>
</table> 

