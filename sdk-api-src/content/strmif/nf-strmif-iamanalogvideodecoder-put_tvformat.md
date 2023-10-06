---
UID: NF:strmif.IAMAnalogVideoDecoder.put_TVFormat
title: IAMAnalogVideoDecoder::put_TVFormat (strmif.h)
description: The put_TVFormat method sets the analog video format.
helpviewer_keywords: ["IAMAnalogVideoDecoder interface [DirectShow]","put_TVFormat method","IAMAnalogVideoDecoder.put_TVFormat","IAMAnalogVideoDecoder::put_TVFormat","IAMAnalogVideoDecoderput_TVFormat","dshow.iamanalogvideodecoder_put_tvformat","put_TVFormat","put_TVFormat method [DirectShow]","put_TVFormat method [DirectShow]","IAMAnalogVideoDecoder interface","strmif/IAMAnalogVideoDecoder::put_TVFormat"]
old-location: dshow\iamanalogvideodecoder_put_tvformat.htm
tech.root: dshow
ms.assetid: ea1522a0-1f00-40c4-9e50-3638495e209c
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],put_TVFormat method, IAMAnalogVideoDecoder.put_TVFormat, IAMAnalogVideoDecoder::put_TVFormat, IAMAnalogVideoDecoderput_TVFormat, dshow.iamanalogvideodecoder_put_tvformat, put_TVFormat, put_TVFormat method [DirectShow], put_TVFormat method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::put_TVFormat
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
 - IAMAnalogVideoDecoder::put_TVFormat
 - strmif/IAMAnalogVideoDecoder::put_TVFormat
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
 - IAMAnalogVideoDecoder.put_TVFormat
---

# IAMAnalogVideoDecoder::put_TVFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_TVFormat</code> method sets the analog video format.

## -parameters

### -param lAnalogVideoStandard [in]

Specifies the video format as a member of the [AnalogVideoStandard](/windows/desktop/api/strmif/ne-strmif-analogvideostandard) enumeration.

## -returns

Returns S_OK if successful, or an error code otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>