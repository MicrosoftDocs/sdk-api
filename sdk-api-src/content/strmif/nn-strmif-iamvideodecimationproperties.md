---
UID: NN:strmif.IAMVideoDecimationProperties
title: IAMVideoDecimationProperties
author: windows-sdk-content
description: The IAMVideoDecimationProperties interface controls how the Overlay Mixer performs video decimationIf a video window is smaller than the native size of the video being displayed, the video renderer must decimate the incoming video&#8212;that is, scale the video down to the smaller size. Decimation can be performed in one of the following places.The overlay hardware on the VGA chip.The scaler built in to the video port (if the connection is through a video port).The decoder supplying video to the renderer.An application can call methods on this interface to select a particular decimation strategy, in order to optimize performance. However, most applications will have no occasion to use this interface. Unless your application is designed to support particular hardware, there is no reason to modify the Overlay Mixer filter's default behavior for decimation.
old-location: dshow\iamvideodecimationproperties.htm
tech.root: DirectShow
ms.assetid: fd435eff-a4bc-40b3-8aa7-50d78d17e4ce
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAMVideoDecimationProperties, IAMVideoDecimationProperties interface [DirectShow], IAMVideoDecimationProperties interface [DirectShow],described, IAMVideoDecimationPropertiesInterface, dshow.iamvideodecimationproperties, strmif/IAMVideoDecimationProperties
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
 - IAMVideoDecimationProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoDecimationProperties interface


## -description



The <code>IAMVideoDecimationProperties</code> interface controls how the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> performs video decimation

If a video window is smaller than the native size of the video being displayed, the video renderer must <i>decimate</i> the incoming video—that is, scale the video down to the smaller size. Decimation can be performed in one of the following places.

<ul>
<li>The overlay hardware on the VGA chip.</li>
<li>The scaler built in to the video port (if the connection is through a video port).</li>
<li>The decoder supplying video to the renderer.</li>
</ul>
An application can call methods on this interface to select a particular decimation strategy, in order to optimize performance. However, most applications will have no occasion to use this interface. Unless your application is designed to support particular hardware, there is no reason to modify the Overlay Mixer filter's default behavior for decimation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoDecimationProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMVideoDecimationProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVideoDecimationProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3addb9be-61df-4310-9066-85f75c64aae4">QueryDecimationUsage</a>
</td>
<td align="left" width="63%">
Retrieves the current decimation strategy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6456154-48f5-41d9-b6f5-863b30a53596">SetDecimationUsage</a>
</td>
<td align="left" width="63%">
Sets the decimation strategy.

</td>
</tr>
</table> 

