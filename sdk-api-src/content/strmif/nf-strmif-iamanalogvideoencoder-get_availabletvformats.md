---
UID: NF:strmif.IAMAnalogVideoEncoder.get_AvailableTVFormats
title: IAMAnalogVideoEncoder::get_AvailableTVFormats (strmif.h)
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The get_AvailableTVFormats method retrieves the analog video standards (NTSC/M, PAL/B, SECAM/K1, and so on) supported by the encoder.
helpviewer_keywords: ["IAMAnalogVideoEncoder interface [DirectShow]","get_AvailableTVFormats method","IAMAnalogVideoEncoder.get_AvailableTVFormats","IAMAnalogVideoEncoder::get_AvailableTVFormats","IAMAnalogVideoEncoderget_AvailableTVFormats","dshow.iamanalogvideoencoder_get_availabletvformats","get_AvailableTVFormats","get_AvailableTVFormats method [DirectShow]","get_AvailableTVFormats method [DirectShow]","IAMAnalogVideoEncoder interface","strmif/IAMAnalogVideoEncoder::get_AvailableTVFormats"]
old-location: dshow\iamanalogvideoencoder_get_availabletvformats.htm
tech.root: dshow
ms.assetid: 739a5f6f-2498-49f4-9c9d-008bd71d4855
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],get_AvailableTVFormats method, IAMAnalogVideoEncoder.get_AvailableTVFormats, IAMAnalogVideoEncoder::get_AvailableTVFormats, IAMAnalogVideoEncoderget_AvailableTVFormats, dshow.iamanalogvideoencoder_get_availabletvformats, get_AvailableTVFormats, get_AvailableTVFormats method [DirectShow], get_AvailableTVFormats method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::get_AvailableTVFormats
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
 - IAMAnalogVideoEncoder::get_AvailableTVFormats
 - strmif/IAMAnalogVideoEncoder::get_AvailableTVFormats
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
 - IAMAnalogVideoEncoder.get_AvailableTVFormats
---

# IAMAnalogVideoEncoder::get_AvailableTVFormats


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>get_AvailableTVFormats</code> method retrieves the analog video standards (NTSC/M, PAL/B, SECAM/K1, and so on) supported by the encoder.

## -parameters

### -param lAnalogVideoStandard [out]

Specifies a pointer to a [AnalogVideoStandard](/windows/desktop/api/strmif/ne-strmif-analogvideostandard) enumeration and the available formats have been combined in this integer with a bitwise OR.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideoencoder">IAMAnalogVideoEncoder Interface</a>