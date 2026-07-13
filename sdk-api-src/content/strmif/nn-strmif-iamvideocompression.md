---
UID: NN:strmif.IAMVideoCompression
title: IAMVideoCompression (strmif.h)
description: The IAMVideoCompression interface sets and retrieves video compression properties.
helpviewer_keywords: ["IAMVideoCompression","IAMVideoCompression interface [DirectShow]","IAMVideoCompression interface [DirectShow]","described","IAMVideoCompressionInterface","dshow.iamvideocompression","strmif/IAMVideoCompression"]
old-location: dshow\iamvideocompression.htm
tech.root: dshow
ms.assetid: 6b7d8a98-35b8-442f-bf51-9e66fd03e2c9
ms.date: 4/26/2023
ms.keywords: IAMVideoCompression, IAMVideoCompression interface [DirectShow], IAMVideoCompression interface [DirectShow],described, IAMVideoCompressionInterface, dshow.iamvideocompression, strmif/IAMVideoCompression
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMVideoCompression
 - strmif/IAMVideoCompression
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
 - IAMVideoCompression
---

# IAMVideoCompression interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IAMVideoCompression</b> interface sets and retrieves video compression properties. It is supported by some video compression filters, and also by some video capture filters that output compressed video. Filters that support this interface expose it through their output pins.

An application can use this interface to control how video is compressed, including characteristics such as the key-frame rate or the compression quality.

A filter that supports this interface might not support every method. Use the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method to determine which methods the filter supports.

<div class="alert"><b>Note</b>  To use this interface on a capture filter, you might need to connect the filter to another filter in the graph.</div>
<div> </div>

## -inheritance

The <b>IAMVideoCompression</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoCompression</b> also has these types of members:

## -remarks

For Windows Driver Model (WDM) devices, the <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="/windows-hardware/drivers/stream/propsetid-vidcap-videocompression">PROPSETID_VIDCAP_VIDEOCOMPRESSION</a> property set. For more information, see the <a href="/windows-hardware/drivers/gettingstarted/">Windows Driver Kit (WDK)</a> documentation.

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
