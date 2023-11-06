---
UID: NF:strmif.IAMAnalogVideoDecoder.get_VCRHorizontalLocking
title: IAMAnalogVideoDecoder::get_VCRHorizontalLocking (strmif.h)
description: The get_VCRHorizontalLocking method indicates whether the decoder is expecting video from a tape source or a broadcast source.
helpviewer_keywords: ["IAMAnalogVideoDecoder interface [DirectShow]","get_VCRHorizontalLocking method","IAMAnalogVideoDecoder.get_VCRHorizontalLocking","IAMAnalogVideoDecoder::get_VCRHorizontalLocking","IAMAnalogVideoDecoderget_VCRHorizontalLocking","dshow.iamanalogvideodecoder_get_vcrhorizontallocking","get_VCRHorizontalLocking","get_VCRHorizontalLocking method [DirectShow]","get_VCRHorizontalLocking method [DirectShow]","IAMAnalogVideoDecoder interface","strmif/IAMAnalogVideoDecoder::get_VCRHorizontalLocking"]
old-location: dshow\iamanalogvideodecoder_get_vcrhorizontallocking.htm
tech.root: dshow
ms.assetid: 0b527578-1840-4cb1-b94b-9be27b40fcf4
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_VCRHorizontalLocking method, IAMAnalogVideoDecoder.get_VCRHorizontalLocking, IAMAnalogVideoDecoder::get_VCRHorizontalLocking, IAMAnalogVideoDecoderget_VCRHorizontalLocking, dshow.iamanalogvideodecoder_get_vcrhorizontallocking, get_VCRHorizontalLocking, get_VCRHorizontalLocking method [DirectShow], get_VCRHorizontalLocking method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_VCRHorizontalLocking
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
 - IAMAnalogVideoDecoder::get_VCRHorizontalLocking
 - strmif/IAMAnalogVideoDecoder::get_VCRHorizontalLocking
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
 - IAMAnalogVideoDecoder.get_VCRHorizontalLocking
---

# IAMAnalogVideoDecoder::get_VCRHorizontalLocking


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_VCRHorizontalLocking</code> method indicates whether the decoder is expecting video from a tape source or a broadcast source.

## -parameters

### -param plVCRHorizontalLocking [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The decoder is expecting video from a broadcast source.</td>
</tr>
<tr>
<td>1</td>
<td>The decoder is expecting video from a tape source.</td>
</tr>
</table>

## -returns

Returns an HRESULT value. Possible values include the following.

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

## -remarks

The timing accuracy of synchronization pulses is typically poorer from a tape source than from a broadcast source. If the returned value is 1, the decoder might relax its sync timing standards.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>