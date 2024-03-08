---
UID: NF:strmif.IAMAnalogVideoEncoder.get_CCEnable
title: IAMAnalogVideoEncoder::get_CCEnable (strmif.h)
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The get_CCEnable determines whether closed captioning on the encoder is currently enabled.
helpviewer_keywords: ["IAMAnalogVideoEncoder interface [DirectShow]","get_CCEnable method","IAMAnalogVideoEncoder.get_CCEnable","IAMAnalogVideoEncoder::get_CCEnable","IAMAnalogVideoEncoderget_CCEnable","dshow.iamanalogvideoencoder_get_ccenable","get_CCEnable","get_CCEnable method [DirectShow]","get_CCEnable method [DirectShow]","IAMAnalogVideoEncoder interface","strmif/IAMAnalogVideoEncoder::get_CCEnable"]
old-location: dshow\iamanalogvideoencoder_get_ccenable.htm
tech.root: dshow
ms.assetid: 0dab4b3a-f139-4ac5-ab30-f223e9120c44
ms.date: 4/26/2023
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],get_CCEnable method, IAMAnalogVideoEncoder.get_CCEnable, IAMAnalogVideoEncoder::get_CCEnable, IAMAnalogVideoEncoderget_CCEnable, dshow.iamanalogvideoencoder_get_ccenable, get_CCEnable, get_CCEnable method [DirectShow], get_CCEnable method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::get_CCEnable
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
 - IAMAnalogVideoEncoder::get_CCEnable
 - strmif/IAMAnalogVideoEncoder::get_CCEnable
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
 - IAMAnalogVideoEncoder.get_CCEnable
---

# IAMAnalogVideoEncoder::get_CCEnable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>get_CCEnable</code> determines whether closed captioning on the encoder is currently enabled.

## -parameters

### -param lCCEnable [out]

Specifies a pointer to a long integer to receive the current status of closed captioning on the encoder.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>1</td>
<td>Closed captioning enabled.</td>
</tr>
<tr>
<td>0</td>
<td>Closed captioning disabled.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideoencoder">IAMAnalogVideoEncoder Interface</a>