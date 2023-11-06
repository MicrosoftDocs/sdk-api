---
UID: NF:strmif.IAMVideoCompression.get_Quality
title: IAMVideoCompression::get_Quality (strmif.h)
description: The get_Quality method retrieves the current compression quality.
helpviewer_keywords: ["IAMVideoCompression interface [DirectShow]","get_Quality method","IAMVideoCompression.get_Quality","IAMVideoCompression::get_Quality","IAMVideoCompressionget_Quality","dshow.iamvideocompression_get_quality","get_Quality","get_Quality method [DirectShow]","get_Quality method [DirectShow]","IAMVideoCompression interface","strmif/IAMVideoCompression::get_Quality"]
old-location: dshow\iamvideocompression_get_quality.htm
tech.root: dshow
ms.assetid: a34b6d15-3c84-476e-bd2f-ee10b59ded82
ms.date: 4/26/2023
ms.keywords: IAMVideoCompression interface [DirectShow],get_Quality method, IAMVideoCompression.get_Quality, IAMVideoCompression::get_Quality, IAMVideoCompressionget_Quality, dshow.iamvideocompression_get_quality, get_Quality, get_Quality method [DirectShow], get_Quality method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::get_Quality
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
 - IAMVideoCompression::get_Quality
 - strmif/IAMVideoCompression::get_Quality
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
 - IAMVideoCompression.get_Quality
---

# IAMVideoCompression::get_Quality


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Quality</code> method retrieves the current compression quality.

## -parameters

### -param pQuality [out]

Pointer to a variable that receives the relative compression quality. The quality is expressed as a value between 0.0 and 1.0, where 1.0 indicates the best quality and 0.0 indicates the worst quality. If the value is negative, the filter will use the default quality.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The exact meaning of the quality setting depends on the filter.

To determine if the filter supports this method, call the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-getinfo">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanQuality</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default quality.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_quality">IAMVideoCompression::put_Quality</a>