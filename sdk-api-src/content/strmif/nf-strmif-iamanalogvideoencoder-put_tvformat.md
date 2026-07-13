---
UID: NF:strmif.IAMAnalogVideoEncoder.put_TVFormat
title: IAMAnalogVideoEncoder::put_TVFormat (strmif.h)
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The put_TVFormat method sets the encoder to a particular analog video standard (NTSC/M, PAL/B, SECAM/K1, and so on).
helpviewer_keywords: ["IAMAnalogVideoEncoder interface [DirectShow]","put_TVFormat method","IAMAnalogVideoEncoder.put_TVFormat","IAMAnalogVideoEncoder::put_TVFormat","IAMAnalogVideoEncoderput_TVFormat","dshow.iamanalogvideoencoder_put_tvformat","put_TVFormat","put_TVFormat method [DirectShow]","put_TVFormat method [DirectShow]","IAMAnalogVideoEncoder interface","strmif/IAMAnalogVideoEncoder::put_TVFormat"]
old-location: dshow\iamanalogvideoencoder_put_tvformat.htm
tech.root: dshow
ms.assetid: 76109fa1-2f7a-4538-9755-6e2de5852d4b
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],put_TVFormat method, IAMAnalogVideoEncoder.put_TVFormat, IAMAnalogVideoEncoder::put_TVFormat, IAMAnalogVideoEncoderput_TVFormat, dshow.iamanalogvideoencoder_put_tvformat, put_TVFormat, put_TVFormat method [DirectShow], put_TVFormat method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::put_TVFormat
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMAnalogVideoEncoder::put_TVFormat
 - strmif/IAMAnalogVideoEncoder::put_TVFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMAnalogVideoEncoder.put_TVFormat
---

# IAMAnalogVideoEncoder::put_TVFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>put_TVFormat</code> method sets the encoder to a particular analog video standard (NTSC/M, PAL/B, SECAM/K1, and so on).

## -parameters

### -param lAnalogVideoStandard [in]

Specifies the video standard to set in the encoder as a [AnalogVideoStandard](/windows/desktop/api/strmif/ne-strmif-analogvideostandard) enumeration.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideoencoder">IAMAnalogVideoEncoder Interface</a>