---
UID: NF:strmif.IAMAudioInputMixer.put_Enable
title: IAMAudioInputMixer::put_Enable (strmif.h)
description: The put_Enable method enables or disables an input.
helpviewer_keywords: ["IAMAudioInputMixer interface [DirectShow]","put_Enable method","IAMAudioInputMixer.put_Enable","IAMAudioInputMixer::put_Enable","IAMAudioInputMixerput_Enable","dshow.iamaudioinputmixer_put_enable","put_Enable","put_Enable method [DirectShow]","put_Enable method [DirectShow]","IAMAudioInputMixer interface","strmif/IAMAudioInputMixer::put_Enable"]
old-location: dshow\iamaudioinputmixer_put_enable.htm
tech.root: dshow
ms.assetid: 84f179bf-2e2f-4ba0-81b7-c20acd09ccea
ms.date: 4/26/2023
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Enable method, IAMAudioInputMixer.put_Enable, IAMAudioInputMixer::put_Enable, IAMAudioInputMixerput_Enable, dshow.iamaudioinputmixer_put_enable, put_Enable, put_Enable method [DirectShow], put_Enable method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Enable
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
 - IAMAudioInputMixer::put_Enable
 - strmif/IAMAudioInputMixer::put_Enable
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
 - IAMAudioInputMixer.put_Enable
---

# IAMAudioInputMixer::put_Enable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Enable</code> method enables or disables an input.

## -parameters

### -param fEnable [in]

Specifies whether to enable or disable the input. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Enable the input.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Disable the input.</td>
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
</table>

## -remarks

If an input is enabled, it is mixed into the recorded signal.

This method applies to specific input pins on the <a href="/windows/desktop/DirectShow/audio-capture-filter">Audio Capture Filter</a>, so the filter itself returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamaudioinputmixer">IAMAudioInputMixer Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamaudioinputmixer-get_enable">IAMAudioInputMixer::get_Enable</a>