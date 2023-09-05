---
UID: NN:strmif.IVideoEncoder
title: IVideoEncoder (strmif.h)
description: The IVideoEncoder interface is optionally exposed by video encoder filters.
helpviewer_keywords: ["IVideoEncoder","IVideoEncoder interface [DirectShow]","IVideoEncoder interface [DirectShow]","described","dshow.ivideoencoder","strmif/IVideoEncoder"]
old-location: dshow\ivideoencoder.htm
tech.root: dshow
ms.assetid: 9264f7a2-b2d4-4449-913b-f1e5ecb40cac
ms.date: 4/26/2023
ms.keywords: IVideoEncoder, IVideoEncoder interface [DirectShow], IVideoEncoder interface [DirectShow],described, dshow.ivideoencoder, strmif/IVideoEncoder
req.header: strmif.h
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
 - IVideoEncoder
 - strmif/IVideoEncoder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IVideoEncoder
---

# IVideoEncoder interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IVideoEncoder</b> may be altered or unavailable in 

subsequent versions.]

The <b>IVideoEncoder</b> interface is optionally exposed by video encoder filters.

## -remarks

The original purpose of this interface was to enable application to determine whether a filter was a video decoder, by calling <b>QueryInterface</b> for the <b>IVideoEncoder</b> interface. The application could then use the <a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a> interface (which <b>IVideoEncoder</b> inherits) to set properties on the encoder. However, <b>IEncoderAPI</b> is deprecated. Encoder filters should expose <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a> instead, and applications should use <b>ICodecAPI</b> to configure encoders.

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a>