---
UID: NN:strmif.IAMDecoderCaps
title: IAMDecoderCaps (strmif.h)
description: The IAMDecoderCaps interface returns capabilities information from an MPEG decoder filter.
helpviewer_keywords: ["IAMDecoderCaps","IAMDecoderCaps interface [DirectShow]","IAMDecoderCaps interface [DirectShow]","described","IAMDecoderCapsInterface","dshow.iamdecodercaps","strmif/IAMDecoderCaps"]
old-location: dshow\iamdecodercaps.htm
tech.root: dshow
ms.assetid: 3951200b-5a81-4832-9dae-021a76c1ab20
ms.date: 4/26/2023
ms.keywords: IAMDecoderCaps, IAMDecoderCaps interface [DirectShow], IAMDecoderCaps interface [DirectShow],described, IAMDecoderCapsInterface, dshow.iamdecodercaps, strmif/IAMDecoderCaps
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMDecoderCaps
 - strmif/IAMDecoderCaps
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
 - IAMDecoderCaps
---

# IAMDecoderCaps interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMDecoderCaps</code> interface returns capabilities information from an MPEG decoder filter. The capabilities reported through this interface include whether the decoder supports the Video Mixing Renderer filter and whether it supports DirectX Video Acceleration.

Some DirectShow components, such as the DVD Graph Builder, use this interface to determine the correct filter graph to build. Applications might use this interface to query the decoder's capabilities.

## -inheritance

The <b>IAMDecoderCaps</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDecoderCaps</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
