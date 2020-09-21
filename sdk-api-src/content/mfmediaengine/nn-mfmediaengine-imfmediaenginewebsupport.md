---
UID: NN:mfmediaengine.IMFMediaEngineWebSupport
title: IMFMediaEngineWebSupport (mfmediaengine.h)
description: Enables playback of web audio.
helpviewer_keywords: ["IMFMediaEngineWebSupport","IMFMediaEngineWebSupport interface [Media Foundation]","IMFMediaEngineWebSupport interface [Media Foundation]","described","mf.imfmediaenginewebsupport","mfmediaengine/IMFMediaEngineWebSupport"]
old-location: mf\imfmediaenginewebsupport.htm
tech.root: mf
ms.assetid: 8EAA54AF-359A-48C4-9A23-BE7997DBAA89
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineWebSupport, IMFMediaEngineWebSupport interface [Media Foundation], IMFMediaEngineWebSupport interface [Media Foundation],described, mf.imfmediaenginewebsupport, mfmediaengine/IMFMediaEngineWebSupport
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaEngineWebSupport
 - mfmediaengine/IMFMediaEngineWebSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineWebSupport
---

# IMFMediaEngineWebSupport interface


## -description

Enables playback of web audio.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineWebSupport</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineWebSupport</b> also has these types of members:
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
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginewebsupport-connectwebaudio">ConnectWebAudio</a>
</td>
<td align="left" width="63%">
Connects web audio to Media Engine using the specified sample rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginewebsupport-disconnectwebaudio">DisconnectWebAudio</a>
</td>
<td align="left" width="63%">
Disconnects web audio from the Media Engine 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginewebsupport-shoulddelaytheloadevent">ShouldDelayTheLoadEvent</a>
</td>
<td align="left" width="63%">
Gets a value indicating if the connecting to Web audio should delay the page's load event.

</td>
</tr>
</table>