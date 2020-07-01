---
UID: NN:windows.media.streaming.ITransportParameters
title: ITransportParameters (windows.media.streaming.h)
description: Encapsulates the methods needed to provide information about the current transport-related settings of the DMR. These settings include the current transport state and information about what methods can currently be invoked on the DMR.
helpviewer_keywords: ["ITransportParameters","ITransportParameters interface [Media Streaming API]","ITransportParameters interface [Media Streaming API]","described","mediastreaming.itransportparameters","windows/ITransportParameters"]
old-location: mediastreaming\itransportparameters.htm
tech.root: mediastreaming
ms.assetid: 4D104C4E-18EE-418F-8D99-3E766A5478F6
ms.date: 12/05/2018
ms.keywords: ITransportParameters, ITransportParameters interface [Media Streaming API], ITransportParameters interface [Media Streaming API],described, mediastreaming.itransportparameters, windows/ITransportParameters
f1_keywords:
- windows.media.streaming/ITransportParameters
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
- ITransportParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransportParameters interface


## -description


Encapsulates the methods needed to provide information about the current transport-related settings of the DMR.  These settings include the current transport state and information about what methods can currently be invoked on the DMR.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransportParameters</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransportParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransportParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/itransportparameters-actioninformation">ActionInformation</a>
</td>
<td align="left" width="63%">
Obtains an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828915(v=vs.85)">IMediaRendererActionInformation</a> interface that provides information about which  methods can currently be invoked on the DMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828958(v=vs.85)">TrackInformation</a>
</td>
<td align="left" width="63%">
Obtains a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh829004(v=vs.85)">TrackInformation</a> structure that provides information about the DMR’s track  parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828959(v=vs.85)">TransportInformation</a>
</td>
<td align="left" width="63%">
Obtains a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh829005(v=vs.85)">TransportInformation</a> structure that provides information about the DMR’s transport parameters.

</td>
</tr>
</table> 

