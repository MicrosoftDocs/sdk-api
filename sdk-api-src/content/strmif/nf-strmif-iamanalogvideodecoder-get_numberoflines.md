---
UID: NF:strmif.IAMAnalogVideoDecoder.get_NumberOfLines
title: IAMAnalogVideoDecoder::get_NumberOfLines (strmif.h)
description: The get_NumberOfLInes method retrieves the number of scan lines in the video signal.
helpviewer_keywords: ["IAMAnalogVideoDecoder interface [DirectShow]","get_NumberOfLines method","IAMAnalogVideoDecoder.get_NumberOfLines","IAMAnalogVideoDecoder::get_NumberOfLines","IAMAnalogVideoDecoderget_NumberOfLines","dshow.iamanalogvideodecoder_get_numberoflines","get_NumberOfLines","get_NumberOfLines method [DirectShow]","get_NumberOfLines method [DirectShow]","IAMAnalogVideoDecoder interface","strmif/IAMAnalogVideoDecoder::get_NumberOfLines"]
old-location: dshow\iamanalogvideodecoder_get_numberoflines.htm
tech.root: dshow
ms.assetid: d1c30230-bd47-4bdb-a89a-332c4da7cc00
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_NumberOfLines method, IAMAnalogVideoDecoder.get_NumberOfLines, IAMAnalogVideoDecoder::get_NumberOfLines, IAMAnalogVideoDecoderget_NumberOfLines, dshow.iamanalogvideodecoder_get_numberoflines, get_NumberOfLines, get_NumberOfLines method [DirectShow], get_NumberOfLines method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_NumberOfLines
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
 - IAMAnalogVideoDecoder::get_NumberOfLines
 - strmif/IAMAnalogVideoDecoder::get_NumberOfLines
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
 - IAMAnalogVideoDecoder.get_NumberOfLines
---

# IAMAnalogVideoDecoder::get_NumberOfLines


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_NumberOfLInes</code> method retrieves the number of scan lines in the video signal.

## -parameters

### -param plNumberOfLines [out]

Pointer to a variable that receives the number of scan lines in the video signal. This is generally by 525 lines for NTSC and 625 lines for PAL or SECAM.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PROP_ID_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>