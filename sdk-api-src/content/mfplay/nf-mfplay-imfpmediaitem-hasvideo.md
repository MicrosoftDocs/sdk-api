---
UID: NF:mfplay.IMFPMediaItem.HasVideo
title: IMFPMediaItem::HasVideo (mfplay.h)
author: windows-sdk-content
description: Queries whether the media item contains a video stream.
old-location: mf\imfpmediaitem_hasvideo.htm
tech.root: medfound
ms.assetid: 6dc8a85c-25e4-4da7-965d-c8882514fc7d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HasVideo, HasVideo method [Media Foundation], HasVideo method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],HasVideo method, IMFPMediaItem.HasVideo, IMFPMediaItem::HasVideo, mf.imfpmediaitem_hasvideo, mfplay/IMFPMediaItem::HasVideo
ms.topic: method
f1_keywords: 
 - "mfplay/IMFPMediaItem.HasVideo"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaItem.HasVideo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaItem::HasVideo


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Queries whether the media item contains a video stream.


## -parameters




### -param pfHasVideo [out]

Receives the value <b>TRUE</b> if the media item contains at least one video stream, or <b>FALSE</b> otherwise.


### -param pfSelected [out]

Receives the value <b>TRUE</b> if at least one video stream is selected, or <b>FALSE</b> otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To select or deselect streams before playback starts, call <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstreamselection">IMFPMediaItem::SetStreamSelection</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

