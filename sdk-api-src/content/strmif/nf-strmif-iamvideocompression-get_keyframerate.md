---
UID: NF:strmif.IAMVideoCompression.get_KeyFrameRate
title: IAMVideoCompression::get_KeyFrameRate (strmif.h)
description: The get_KeyFrameRate method retrieves the current key-frame rate.
helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","get_KeyFrameRate method","IAMVideoCompression.get_KeyFrameRate","IAMVideoCompression::get_KeyFrameRate","IAMVideoCompressionget_KeyFrameRate","dshow.iamvideocompression_get_keyframerate","get_KeyFrameRate","get_KeyFrameRate method [DirectShow]","get_KeyFrameRate method [DirectShow]","IAMVideoCompression interface","strmif/IAMVideoCompression::get_KeyFrameRate"]
old-location: dshow\iamvideocompression_get_keyframerate.htm
tech.root: dshow
ms.assetid: af73cfaa-3297-44a7-96a7-8805aad057e2
ms.date: 4/26/2023
ms.keywords: IAMVideoCompression interface [DirectShow],get_KeyFrameRate method, IAMVideoCompression.get_KeyFrameRate, IAMVideoCompression::get_KeyFrameRate, IAMVideoCompressionget_KeyFrameRate, dshow.iamvideocompression_get_keyframerate, get_KeyFrameRate, get_KeyFrameRate method [DirectShow], get_KeyFrameRate method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::get_KeyFrameRate
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
 - IAMVideoCompression::get_KeyFrameRate
 - strmif/IAMVideoCompression::get_KeyFrameRate
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
 - IAMVideoCompression.get_KeyFrameRate
---

# IAMVideoCompression::get_KeyFrameRate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_KeyFrameRate</code> method retrieves the current key-frame rate.

## -parameters

### -param pKeyFrameRate [out]

Pointer to a variable that receives the current key-frame rate. If the value is negative, the filter will use the default key-frame rate. If the value is zero, only the first frame is a key frame.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The key-frame rate is the number of frames per key frame. For example, if the rate is 15, then a key frame occurs every 15 frames.

To determine if the filter supports this method, call the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanKeyFrame</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default key-frame rate.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_keyframerate">IAMVideoCompression::put_KeyFrameRate</a>