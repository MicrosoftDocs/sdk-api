---
UID: NN:windows.media.streaming.IMediaRendererFactory
title: IMediaRendererFactory (windows.media.streaming.h)
description: Encapsulates the methods needed to asynchronously create a new instance of an object that implements the IMediaRenderer interface.
old-location: mediastreaming\imediarendererfactory.htm
tech.root: mediastreaming
ms.assetid: E07EC208-CF00-46D0-B00D-AA8E59F12A0A
ms.date: 12/05/2018
ms.keywords: IMediaRendererFactory, IMediaRendererFactory interface [Media Streaming API], IMediaRendererFactory interface [Media Streaming API],described, mediastreaming.imediarendererfactory, windows/IMediaRendererFactory
ms.topic: interface
f1_keywords:
- windows.media.streaming/IMediaRendererFactory
dev_langs:
- c++
req.header: windows.media.streaming.h
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
- windows.media.streaming.h
api_name:
- IMediaRendererFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaRendererFactory interface


## -description


Encapsulates the methods needed to asynchronously create a new instance of an object that implements the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaRendererFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaRendererFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaRendererFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendererfactory-createmediarendererasync">CreateMediaRendererAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates a new instance of an object that implements the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a> interface using the specified Unique Device Name (UDN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarendererfactory-createmediarendererfrombasicdeviceasync">CreateMediaRendererFromBasicDeviceAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates a new instance of an object that implements the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a> interface using the specified <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a> interface.

</td>
</tr>
</table> 

