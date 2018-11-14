---
UID: NN:mfmediaengine.IMFMediaEngineWebSupport
title: IMFMediaEngineWebSupport
author: windows-sdk-content
description: Enables playback of web audio.
old-location: mf\imfmediaenginewebsupport.htm
tech.root: medfound
ms.assetid: 8EAA54AF-359A-48C4-9A23-BE7997DBAA89
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFMediaEngineWebSupport, IMFMediaEngineWebSupport interface [Media Foundation], IMFMediaEngineWebSupport interface [Media Foundation],described, mf.imfmediaenginewebsupport, mfmediaengine/IMFMediaEngineWebSupport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfmediaengine.h
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
 - mfmediaengine.h
api_name:
 - IMFMediaEngineWebSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineWebSupport interface


## -description


Enables playback of web audio.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineWebSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineWebSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineWebSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E2470C2B-2E55-4B4F-B00F-03ABBB1A896F">ConnectWebAudio</a>
</td>
<td align="left" width="63%">
Connects web audio to Media Engine using the specified sample rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04AE7972-B0F1-4C35-A5F4-88F0B85C99E7">DisconnectWebAudio</a>
</td>
<td align="left" width="63%">
Disconnects web audio from the Media Engine 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/850ED4DC-1790-481E-A8CD-9F87F9E389EC">ShouldDelayTheLoadEvent</a>
</td>
<td align="left" width="63%">
Gets a value indicating if the connecting to Web audio should delay the page's load event.

</td>
</tr>
</table> 

