---
UID: NF:strmif.IAMAnalogVideoDecoder.put_VCRHorizontalLocking
title: IAMAnalogVideoDecoder::put_VCRHorizontalLocking (strmif.h)
description: The put_VCRHorizontalLocking method specifies whether the video is a tape source or a broadcast source.
helpviewer_keywords: ["IAMAnalogVideoDecoder interface [DirectShow]","put_VCRHorizontalLocking method","IAMAnalogVideoDecoder.put_VCRHorizontalLocking","IAMAnalogVideoDecoder::put_VCRHorizontalLocking","IAMAnalogVideoDecoderput_VCRHorizontalLocking","dshow.iamanalogvideodecoder_put_vcrhorizontallocking","put_VCRHorizontalLocking","put_VCRHorizontalLocking method [DirectShow]","put_VCRHorizontalLocking method [DirectShow]","IAMAnalogVideoDecoder interface","strmif/IAMAnalogVideoDecoder::put_VCRHorizontalLocking"]
old-location: dshow\iamanalogvideodecoder_put_vcrhorizontallocking.htm
tech.root: dshow
ms.assetid: 4b215f8b-dfd9-40cf-a392-7cc42b17b214
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],put_VCRHorizontalLocking method, IAMAnalogVideoDecoder.put_VCRHorizontalLocking, IAMAnalogVideoDecoder::put_VCRHorizontalLocking, IAMAnalogVideoDecoderput_VCRHorizontalLocking, dshow.iamanalogvideodecoder_put_vcrhorizontallocking, put_VCRHorizontalLocking, put_VCRHorizontalLocking method [DirectShow], put_VCRHorizontalLocking method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::put_VCRHorizontalLocking
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
 - IAMAnalogVideoDecoder::put_VCRHorizontalLocking
 - strmif/IAMAnalogVideoDecoder::put_VCRHorizontalLocking
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
 - IAMAnalogVideoDecoder.put_VCRHorizontalLocking
---

# IAMAnalogVideoDecoder::put_VCRHorizontalLocking


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_VCRHorizontalLocking</code> method specifies whether the video is a tape source or a broadcast source.

## -parameters

### -param lVCRHorizontalLocking [in]

Specifies one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The video is from a broadcast source.</td>
</tr>
<tr>
<td>1</td>
<td>The video is from a tape source.</td>
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

The timing accuracy of synchronization pulses is typically poorer from a tape source than from a broadcast source. Setting the value to 1 tells the decoder to relax its standards, which leads to a better chance of maintaining sync.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>