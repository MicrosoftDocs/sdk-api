---
UID: NF:strmif.IAMAudioInputMixer.put_MixLevel
title: IAMAudioInputMixer::put_MixLevel (strmif.h)
description: The put_MixLevel method sets the recording level for this input.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","put_MixLevel method","IAMAudioInputMixer.put_MixLevel","IAMAudioInputMixer::put_MixLevel","IAMAudioInputMixerput_MixLevel","dshow.iamaudioinputmixer_put_mixlevel","put_MixLevel","put_MixLevel method [DirectShow]","put_MixLevel method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::put_MixLevel"]
old-location: dshow\iamaudioinputmixer_put_mixlevel.htm
tech.root: dshow
ms.assetid: 07fd327f-d78b-4fc0-9c6a-69cdaa2bcdf6
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_MixLevel method, IAMAudioInputMixer.put_MixLevel, IAMAudioInputMixer::put_MixLevel, IAMAudioInputMixerput_MixLevel, dshow.iamaudioinputmixer_put_mixlevel, put_MixLevel, put_MixLevel method [DirectShow], put_MixLevel method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_MixLevel
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
 - IAMAudioInputMixer::put_MixLevel
 - strmif/IAMAudioInputMixer::put_MixLevel
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
 - IAMAudioInputMixer.put_MixLevel
---

# IAMAudioInputMixer::put_MixLevel


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_MixLevel</code> method sets the recording level for this input.

## -parameters

### -param Level [in]

Specifies the recording level. The following values are possible.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0.0 to 1.0</td>
<td>Zero indicates that the recording level is off; the value 1.0 indicates that the recording level is at full volume. Intermediate values are also allowed.</td>
</tr>
<tr>
<td>AMF_AUTOMATICGAIN</td>
<td>Enable automatic adjustment of the recording level.</td>
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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This filter does not support the AMF_AUTOMATICGAIN flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_mixlevel">IAMAudioInputMixer::get_MixLevel</a>