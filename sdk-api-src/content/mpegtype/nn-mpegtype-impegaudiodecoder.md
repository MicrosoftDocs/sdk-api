---
UID: NN:mpegtype.IMpegAudioDecoder
title: IMpegAudioDecoder (mpegtype.h)
description: The IMpegAudioDecoder interface is exposed on the MPEG-1 Audio Decoder filter and it enables applications to control decoding parameters.
helpviewer_keywords: ["IMpegAudioDecoder","IMpegAudioDecoder interface [DirectShow]","IMpegAudioDecoder interface [DirectShow]","described","IMpegAudioDecoderInterface","dshow.impegaudiodecoder","mpegtype/IMpegAudioDecoder"]
old-location: dshow\impegaudiodecoder.htm
tech.root: dshow
ms.assetid: 59fd96ef-2f9a-4a8e-bd08-2695de52b1c6
ms.date: 12/05/2018
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

The <code>IMpegAudioDecoder</code> interface is exposed on the <a href="/windows/desktop/DirectShow/mpeg-1-audio-decoder-filter">MPEG-1 Audio Decoder</a> filter and it enables applications to control decoding parameters. Most of these methods are useful only when an application is running on an older system and needs to sacrifice quality to increase performance. The default values provide the optimal decoding quality.

The two methods that are still useful in some scenarios are <a href="/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-get_dualmode">get_DualMode</a> and <a href="/windows/desktop/api/mpegtype/nf-mpegtype-impegaudiodecoder-put_dualmode">put_DualMode</a>. These methods enable applications to access either the right or left channel in VCD-based karaoke discs.

## -inheritance

The <b>IMpegAudioDecoder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMpegAudioDecoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

