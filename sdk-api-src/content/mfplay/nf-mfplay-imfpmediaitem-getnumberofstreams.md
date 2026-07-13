---
UID: NF:mfplay.IMFPMediaItem.GetNumberOfStreams
title: IMFPMediaItem::GetNumberOfStreams (mfplay.h)
description: Gets the number of streams (audio, video, and other) in the media item.
helpviewer_keywords: ["GetNumberOfStreams","GetNumberOfStreams method [Media Foundation]","GetNumberOfStreams method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetNumberOfStreams method","IMFPMediaItem.GetNumberOfStreams","IMFPMediaItem::GetNumberOfStreams","mf.imfpmediaitem_getnumberofstreams","mfplay/IMFPMediaItem::GetNumberOfStreams"]
old-location: mf\imfpmediaitem_getnumberofstreams.htm
tech.root: mfarchive
archived: true
ms.assetid: 65a3cfc8-9171-4206-b1b6-54bb0d3ecdd1
ms.date: 12/05/2018
ms.keywords: GetNumberOfStreams, GetNumberOfStreams method [Media Foundation], GetNumberOfStreams method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetNumberOfStreams method, IMFPMediaItem.GetNumberOfStreams, IMFPMediaItem::GetNumberOfStreams, mf.imfpmediaitem_getnumberofstreams, mfplay/IMFPMediaItem::GetNumberOfStreams
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
 - IMFPMediaItem::GetNumberOfStreams
 - mfplay/IMFPMediaItem::GetNumberOfStreams
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
 - IMFPMediaItem.GetNumberOfStreams
---

# IMFPMediaItem::GetNumberOfStreams


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the number of streams (audio, video, and other) in the media item.

## -parameters

### -param pdwStreamCount [out]

Receives the number of streams.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>