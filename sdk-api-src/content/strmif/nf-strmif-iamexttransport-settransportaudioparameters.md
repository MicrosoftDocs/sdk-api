---
UID: NF:strmif.IAMExtTransport.SetTransportAudioParameters
title: IAMExtTransport::SetTransportAudioParameters (strmif.h)
description: The SetTransportAudioParameters assigns audio parameter settings for external transport.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","SetTransportAudioParameters method","IAMExtTransport.SetTransportAudioParameters","IAMExtTransport::SetTransportAudioParameters","IAMExtTransportSetTransportAudioParameters","SetTransportAudioParameters","SetTransportAudioParameters method [DirectShow]","SetTransportAudioParameters method [DirectShow]","IAMExtTransport interface","dshow.iamexttransport_settransportaudioparameters","strmif/IAMExtTransport::SetTransportAudioParameters"]
old-location: dshow\iamexttransport_settransportaudioparameters.htm
tech.root: dshow
ms.assetid: e013dd73-7276-48b3-bf5f-ffb4b3d49419
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],SetTransportAudioParameters method, IAMExtTransport.SetTransportAudioParameters, IAMExtTransport::SetTransportAudioParameters, IAMExtTransportSetTransportAudioParameters, SetTransportAudioParameters, SetTransportAudioParameters method [DirectShow], SetTransportAudioParameters method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_settransportaudioparameters, strmif/IAMExtTransport::SetTransportAudioParameters
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
 - IAMExtTransport::SetTransportAudioParameters
 - strmif/IAMExtTransport::SetTransportAudioParameters
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
 - IAMExtTransport.SetTransportAudioParameters
---

# IAMExtTransport::SetTransportAudioParameters


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetTransportAudioParameters</code> assigns audio parameter settings for external transport.



This method is not implemented.

## -parameters

### -param Param [in]

Specifies the audio parameter you want to set as a <b>long</b> integer.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_OUTPUT</td>
<td>Enable audio channel(s) for output.</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_RECORD</td>
<td>Enable audio channel(s) for recording.</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_SELSYNC</td>
<td>Enable audio channel(s) for selsync recording.</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_SET_MONITOR</td>
<td>Set the monitor output source.</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_SET_SOURCE</td>
<td>Set the active audio input.</td>
</tr>
</table>

### -param Value [in]

Specifies which audio channel or channels is assigned the parameter as a <b>long</b> integer.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

Specify an exact channel or channels in <i>Value</i> by selecting ED_AUDIO_1 through ED_AUDIO_24 (use a bitwise OR to combine), or all channels by selecting ED_AUDIO_ALL.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-gettransportaudioparameters">IAMExtTransport::GetTransportAudioParameters</a>