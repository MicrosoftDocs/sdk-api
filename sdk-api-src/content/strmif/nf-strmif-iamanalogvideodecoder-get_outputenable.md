---
UID: NF:strmif.IAMAnalogVideoDecoder.get_OutputEnable
title: IAMAnalogVideoDecoder::get_OutputEnable (strmif.h)
description: The get_OutputEnable method determines whether the video port bus is enabled.
helpviewer_keywords: ["IAMAnalogVideoDecoder interface [DirectShow]","get_OutputEnable method","IAMAnalogVideoDecoder.get_OutputEnable","IAMAnalogVideoDecoder::get_OutputEnable","IAMAnalogVideoDecoderget_OutputEnable","dshow.iamanalogvideodecoder_get_outputenable","get_OutputEnable","get_OutputEnable method [DirectShow]","get_OutputEnable method [DirectShow]","IAMAnalogVideoDecoder interface","strmif/IAMAnalogVideoDecoder::get_OutputEnable"]
old-location: dshow\iamanalogvideodecoder_get_outputenable.htm
tech.root: dshow
ms.assetid: 2379079d-3852-45c7-a290-b3a33ea8af1a
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_OutputEnable method, IAMAnalogVideoDecoder.get_OutputEnable, IAMAnalogVideoDecoder::get_OutputEnable, IAMAnalogVideoDecoderget_OutputEnable, dshow.iamanalogvideodecoder_get_outputenable, get_OutputEnable, get_OutputEnable method [DirectShow], get_OutputEnable method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_OutputEnable
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
 - IAMAnalogVideoDecoder::get_OutputEnable
 - strmif/IAMAnalogVideoDecoder::get_OutputEnable
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
 - IAMAnalogVideoDecoder.get_OutputEnable
---

# IAMAnalogVideoDecoder::get_OutputEnable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_OutputEnable</code> method determines whether the video port bus is enabled.

## -parameters

### -param plOutputEnable [out]

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
<td>Video port bus is disabled.</td>
</tr>
<tr>
<td>1</td>
<td>Video port bus is enabled.</td>
</tr>
</table>

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

## -remarks

This method applies only to devices that use a shared video port bus. If the returned value is 1, the device is actively driving the video port bus. If the value is zero, the device is tri-stated.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>