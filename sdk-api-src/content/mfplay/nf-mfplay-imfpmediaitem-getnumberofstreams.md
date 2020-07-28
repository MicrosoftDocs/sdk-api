---
UID: NF:mfplay.IMFPMediaItem.GetNumberOfStreams
title: IMFPMediaItem::GetNumberOfStreams (mfplay.h)
description: Gets the number of streams (audio, video, and other) in the media item.
helpviewer_keywords: ["GetNumberOfStreams","GetNumberOfStreams method [Media Foundation]","GetNumberOfStreams method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetNumberOfStreams method","IMFPMediaItem.GetNumberOfStreams","IMFPMediaItem::GetNumberOfStreams","mf.imfpmediaitem_getnumberofstreams","mfplay/IMFPMediaItem::GetNumberOfStreams"]
old-location: mf\imfpmediaitem_getnumberofstreams.htm
tech.root: mf
ms.assetid: 65a3cfc8-9171-4206-b1b6-54bb0d3ecdd1
ms.date: 12/05/2018
ms.keywords: GetNumberOfStreams, GetNumberOfStreams method [Media Foundation], GetNumberOfStreams method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetNumberOfStreams method, IMFPMediaItem.GetNumberOfStreams, IMFPMediaItem::GetNumberOfStreams, mf.imfpmediaitem_getnumberofstreams, mfplay/IMFPMediaItem::GetNumberOfStreams
f1_keywords:
- mfplay/IMFPMediaItem.GetNumberOfStreams
dev_langs:
- c++
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
- IMFPMediaItem.GetNumberOfStreams
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaItem::GetNumberOfStreams


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets the number of streams (audio, video, and other) in the media item.


## -parameters




### -param pdwStreamCount [out]

Receives the number of streams.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

