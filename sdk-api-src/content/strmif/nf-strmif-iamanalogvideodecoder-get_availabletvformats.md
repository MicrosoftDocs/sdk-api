---
UID: NF:strmif.IAMAnalogVideoDecoder.get_AvailableTVFormats
title: IAMAnalogVideoDecoder::get_AvailableTVFormats (strmif.h)
description: The get_AvailableTVFormats method retrieves the analog video formats that the decoder supports.
helpviewer_keywords: ["IAMAnalogVideoDecoder interface [DirectShow]","get_AvailableTVFormats method","IAMAnalogVideoDecoder.get_AvailableTVFormats","IAMAnalogVideoDecoder::get_AvailableTVFormats","IAMAnalogVideoDecoderget_AvailableTVFormats","dshow.iamanalogvideodecoder_get_availabletvformats","get_AvailableTVFormats","get_AvailableTVFormats method [DirectShow]","get_AvailableTVFormats method [DirectShow]","IAMAnalogVideoDecoder interface","strmif/IAMAnalogVideoDecoder::get_AvailableTVFormats"]
old-location: dshow\iamanalogvideodecoder_get_availabletvformats.htm
tech.root: dshow
ms.assetid: 651f902f-de27-4185-b368-ce2cbf12cfae
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_AvailableTVFormats method, IAMAnalogVideoDecoder.get_AvailableTVFormats, IAMAnalogVideoDecoder::get_AvailableTVFormats, IAMAnalogVideoDecoderget_AvailableTVFormats, dshow.iamanalogvideodecoder_get_availabletvformats, get_AvailableTVFormats, get_AvailableTVFormats method [DirectShow], get_AvailableTVFormats method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_AvailableTVFormats
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
 - IAMAnalogVideoDecoder::get_AvailableTVFormats
 - strmif/IAMAnalogVideoDecoder::get_AvailableTVFormats
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
 - IAMAnalogVideoDecoder.get_AvailableTVFormats
---

# IAMAnalogVideoDecoder::get_AvailableTVFormats


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_AvailableTVFormats</b> method retrieves the analog video formats that the decoder supports.

## -parameters

### -param lAnalogVideoStandard [out]

Pointer to a variable that receives a bitwise [AnalogVideoStandard](/windows/desktop/api/strmif/ne-strmif-analogvideostandard) enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>