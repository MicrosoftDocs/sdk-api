---
UID: NF:strmif.IAMVideoCompression.put_Quality
title: IAMVideoCompression::put_Quality (strmif.h)
description: The put_Quality method sets the compression quality.
helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","put_Quality method","IAMVideoCompression.put_Quality","IAMVideoCompression::put_Quality","IAMVideoCompressionput_Quality","dshow.iamvideocompression_put_quality","put_Quality","put_Quality method [DirectShow]","put_Quality method [DirectShow]","IAMVideoCompression interface","strmif/IAMVideoCompression::put_Quality"]
old-location: dshow\iamvideocompression_put_quality.htm
tech.root: dshow
ms.assetid: 7ecc00f9-73d4-4d26-b7b0-1b6419027d69
ms.date: 4/26/2023
ms.keywords: IAMVideoCompression interface [DirectShow],put_Quality method, IAMVideoCompression.put_Quality, IAMVideoCompression::put_Quality, IAMVideoCompressionput_Quality, dshow.iamvideocompression_put_quality, put_Quality, put_Quality method [DirectShow], put_Quality method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::put_Quality
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
 - IAMVideoCompression::put_Quality
 - strmif/IAMVideoCompression::put_Quality
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
 - IAMVideoCompression.put_Quality
---

# IAMVideoCompression::put_Quality


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Quality</code> method sets the compression quality.

## -parameters

### -param Quality [in]

Specifies the quality as a value between 0.0 and 1.0, where 1.0 indicates the best quality and 0.0 indicates the worst quality. If the value is negative, the filter will use the default quality.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

To determine if the filter supports this method, call the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanQuality</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default quality.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_quality">IAMVideoCompression::get_Quality</a>