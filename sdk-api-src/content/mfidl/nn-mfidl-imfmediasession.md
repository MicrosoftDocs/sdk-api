---
UID: NN:mfidl.IMFMediaSession
title: IMFMediaSession (mfidl.h)
description: Provides playback controls for protected and unprotected content.
helpviewer_keywords: ["IMFMediaSession","IMFMediaSession interface [Media Foundation]","IMFMediaSession interface [Media Foundation]","described","feebf891-73fa-4fe6-94ca-3594986fc92d","mf.imfmediasession","mfidl/IMFMediaSession"]
old-location: mf\imfmediasession.htm
tech.root: mf
ms.assetid: feebf891-73fa-4fe6-94ca-3594986fc92d
ms.date: 12/05/2018
ms.keywords: IMFMediaSession, IMFMediaSession interface [Media Foundation], IMFMediaSession interface [Media Foundation],described, feebf891-73fa-4fe6-94ca-3594986fc92d, mf.imfmediasession, mfidl/IMFMediaSession
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaSession
 - mfidl/IMFMediaSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSession
---

# IMFMediaSession interface


## -description

Provides playback controls for protected and unprotected content. The Media Session and the protected media path (PMP) session objects expose this interface. This interface is the primary interface that applications use to control the Media Foundation pipeline.

To obtain a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession">MFCreateMediaSession</a> or <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession">MFCreatePMPMediaSession</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSession</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>. <b>IMFMediaSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies">ClearTopologies</a>
</td>
<td align="left" width="63%">
Clears all of the presentations that are queued for playback in the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close">Close</a>
</td>
<td align="left" width="63%">
Closes the Media Session and releases all of the resources it is using.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock">GetClock</a>
</td>
<td align="left" width="63%">
Retrieves the Media Session's presentation clock.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getfulltopology">GetFullTopology</a>
</td>
<td align="left" width="63%">
Gets a topology from the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities">GetSessionCapabilities</a>
</td>
<td align="left" width="63%">
Gets the capabilities of the Media Session, based on the current presentation.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology">SetTopology</a>
</td>
<td align="left" width="63%">
Sets a topology on the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the Media Session and releases all the resources used by the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start">Start</a>
</td>
<td align="left" width="63%">
Starts the Media Session.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the Media Session.
        

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/how-to-play-unprotected-media-files">How to Play Media Files with Media Foundation</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>