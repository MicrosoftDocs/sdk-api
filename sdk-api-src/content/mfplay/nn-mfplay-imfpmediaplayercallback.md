---
UID: NN:mfplay.IMFPMediaPlayerCallback
title: IMFPMediaPlayerCallback (mfplay.h)
description: Callback interface for the IMFPMediaPlayer interface.
helpviewer_keywords: ["IMFPMediaPlayerCallback","IMFPMediaPlayerCallback interface [Media Foundation]","IMFPMediaPlayerCallback interface [Media Foundation]","described","mf.imfpmediaplayercallback","mfplay/IMFPMediaPlayerCallback"]
old-location: mf\imfpmediaplayercallback.htm
tech.root: mf
ms.assetid: 7d9d01bf-861a-4c35-93b1-dbf85cbf0a32
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayerCallback, IMFPMediaPlayerCallback interface [Media Foundation], IMFPMediaPlayerCallback interface [Media Foundation],described, mf.imfpmediaplayercallback, mfplay/IMFPMediaPlayerCallback
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFPMediaPlayerCallback
 - mfplay/IMFPMediaPlayerCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayerCallback
---

# IMFPMediaPlayerCallback interface


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Callback interface for the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> interface.

To set the callback, pass an <b>IMFPMediaPlayerCallback</b> pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a>  function in the  <i>pCallback</i>  parameter. The application implements the <b>IMFPMediaPlayerCallback</b> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMediaPlayerCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMediaPlayerCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMediaPlayerCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">OnMediaPlayerEvent</a>
</td>
<td align="left" width="63%">
Called by the MFPlay player object to notify the application of a playback event.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>

