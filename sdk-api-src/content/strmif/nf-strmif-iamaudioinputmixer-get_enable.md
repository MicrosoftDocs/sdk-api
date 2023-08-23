---
UID: NF:strmif.IAMAudioInputMixer.get_Enable
title: IAMAudioInputMixer::get_Enable (strmif.h)
description: The get_Enable method retrieves whether the input is enabled.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","get_Enable method","IAMAudioInputMixer.get_Enable","IAMAudioInputMixer::get_Enable","IAMAudioInputMixerget_Enable","dshow.iamaudioinputmixer_get_enable","get_Enable","get_Enable method [DirectShow]","get_Enable method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::get_Enable"]
old-location: dshow\iamaudioinputmixer_get_enable.htm
tech.root: dshow
ms.assetid: d3ec509c-9990-4803-a4e3-abc88fc8c522
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Enable method, IAMAudioInputMixer.get_Enable, IAMAudioInputMixer::get_Enable, IAMAudioInputMixerget_Enable, dshow.iamaudioinputmixer_get_enable, get_Enable, get_Enable method [DirectShow], get_Enable method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Enable
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
 - IAMAudioInputMixer::get_Enable
 - strmif/IAMAudioInputMixer::get_Enable
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
 - IAMAudioInputMixer.get_Enable
---

# IAMAudioInputMixer::get_Enable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Enable</code> method retrieves whether the input is enabled.

## -parameters

### -param pfEnable [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Input is enabled.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Input is disabled.</td>
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
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

This method applies to specific input pins on the <a href="/windows/desktop/DirectShow/audio-capture-filter">Audio Capture Filter</a>, so the filter itself returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-put_enable">IAMAudioInputMixer::put_Enable</a>