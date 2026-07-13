---
UID: NN:mpegtype.IMpegAudioDecoder
title: IMpegAudioDecoder (mpegtype.h)
description: The IMpegAudioDecoder interface is exposed on the MPEG-1 Audio Decoder filter and it enables applications to control decoding parameters.
helpviewer_keywords: ["IMpegAudioDecoder","IMpegAudioDecoder interface [DirectShow]","IMpegAudioDecoder interface [DirectShow]","described","IMpegAudioDecoderInterface","dshow.impegaudiodecoder","mpegtype/IMpegAudioDecoder"]
old-location: dshow\impegaudiodecoder.htm
tech.root: dshow
ms.assetid: 59fd96ef-2f9a-4a8e-bd08-2695de52b1c6
ms.date: 4/26/2023
ms.keywords: IMpegAudioDecoder, IMpegAudioDecoder interface [DirectShow], IMpegAudioDecoder interface [DirectShow],described, IMpegAudioDecoderInterface, dshow.impegaudiodecoder, mpegtype/IMpegAudioDecoder
req.header: mpegtype.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMpegAudioDecoder
 - mpegtype/IMpegAudioDecoder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMpegAudioDecoder
---

# IMpegAudioDecoder interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMpegAudioDecoder</code> interface is exposed on the <a href="/windows/desktop/DirectShow/mpeg-1-audio-decoder-filter">MPEG-1 Audio Decoder</a> filter and it enables applications to control decoding parameters. Most of these methods are useful only when an application is running on an older system and needs to sacrifice quality to increase performance. The default values provide the optimal decoding quality.

The two methods that are still useful in some scenarios are <a href="/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_dualmode">get_DualMode</a> and <a href="/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-put_dualmode">put_DualMode</a>. These methods enable applications to access either the right or left channel in VCD-based karaoke discs.

## -inheritance

The <b>IMpegAudioDecoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMpegAudioDecoder</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

