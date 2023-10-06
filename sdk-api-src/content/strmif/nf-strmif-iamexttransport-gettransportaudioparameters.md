---
UID: NF:strmif.IAMExtTransport.GetTransportAudioParameters
title: IAMExtTransport::GetTransportAudioParameters (strmif.h)
description: The GetTransportAudioParameters method retrieves audio parameter setting for external transport.
helpviewer_keywords: ["GetTransportAudioParameters","GetTransportAudioParameters method [DirectShow]","GetTransportAudioParameters method [DirectShow]","IAMExtTransport interface","IAMExtTransport interface [DirectShow]","GetTransportAudioParameters method","IAMExtTransport.GetTransportAudioParameters","IAMExtTransport::GetTransportAudioParameters","IAMExtTransportGetTransportAudioParameters","dshow.iamexttransport_gettransportaudioparameters","strmif/IAMExtTransport::GetTransportAudioParameters"]
old-location: dshow\iamexttransport_gettransportaudioparameters.htm
tech.root: dshow
ms.assetid: 90650920-f151-4e19-9133-4f1eb5eecbc2
ms.date: 4/26/2023
ms.keywords: GetTransportAudioParameters, GetTransportAudioParameters method [DirectShow], GetTransportAudioParameters method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetTransportAudioParameters method, IAMExtTransport.GetTransportAudioParameters, IAMExtTransport::GetTransportAudioParameters, IAMExtTransportGetTransportAudioParameters, dshow.iamexttransport_gettransportaudioparameters, strmif/IAMExtTransport::GetTransportAudioParameters
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
 - IAMExtTransport::GetTransportAudioParameters
 - strmif/IAMExtTransport::GetTransportAudioParameters
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
 - IAMExtTransport.GetTransportAudioParameters
---

# IAMExtTransport::GetTransportAudioParameters


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetTransportAudioParameters</code> method retrieves audio parameter setting for external transport.



This method is not implemented.

## -parameters

### -param Param [in]

Specifies the audio parameter, whose value you want receive, as a <b>long</b> integer containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_OUTPUT</td>
<td>Audio output channel(s)</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_RECORD</td>
<td>Audio recording channel(s)</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_SELSYNC</td>
<td>Audio selsync recording channel(s)</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_SET_MONITOR</td>
<td>Monitor output audio channel(s)</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_SET_SOURCE</td>
<td>Audio source channel(s)</td>
</tr>
</table>

### -param pValue [out]

Specifies a pointer to a <b>long</b> integer to receive the channel or channels set in the <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportaudioparameters">IAMExtTransport::SetTransportAudioParameters</a> method.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>