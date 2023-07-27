---
UID: NF:strmif.IDvdInfo2.GetCurrentAudio
title: IDvdInfo2::GetCurrentAudio (strmif.h)
description: The GetCurrentAudio method retrieves the number of available audio streams and the number of the currently selected audio stream.
helpviewer_keywords: ["GetCurrentAudio","GetCurrentAudio method [DirectShow]","GetCurrentAudio method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetCurrentAudio method","IDvdInfo2.GetCurrentAudio","IDvdInfo2::GetCurrentAudio","IDvdInfo2GetCurrentAudio","dshow.idvdinfo2_getcurrentaudio","strmif/IDvdInfo2::GetCurrentAudio"]
old-location: dshow\idvdinfo2_getcurrentaudio.htm
tech.root: dshow
ms.assetid: 0f2ff79f-cefa-43e5-ab91-348a5341a171
ms.date: 4/26/2023
ms.keywords: GetCurrentAudio, GetCurrentAudio method [DirectShow], GetCurrentAudio method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentAudio method, IDvdInfo2.GetCurrentAudio, IDvdInfo2::GetCurrentAudio, IDvdInfo2GetCurrentAudio, dshow.idvdinfo2_getcurrentaudio, strmif/IDvdInfo2::GetCurrentAudio
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IDvdInfo2::GetCurrentAudio
 - strmif/IDvdInfo2::GetCurrentAudio
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
 - IDvdInfo2.GetCurrentAudio
---

# IDvdInfo2::GetCurrentAudio


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentAudio</code> method retrieves the number of available audio streams and the number of the currently selected audio stream.

## -parameters

### -param pulStreamsAvailable [out]

Receives the number of available audio streams.

### -param pulCurrentStream [out]

Receives the currently selected audio stream number in the current title.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Input arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized or not in a valid domain.

</td>
</tr>
</table>

## -remarks

To get the available audio languages on the disc, call <code>GetCurrentAudio</code> and then call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getaudiolanguage">GetAudioLanguage</a> for each stream, starting from zero through (<i>pulStreamsAvailable</i> - 1) to get the language content.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/ec-dvd-audio-stream-change">EC_DVD_AUDIO_STREAM_CHANGE</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>