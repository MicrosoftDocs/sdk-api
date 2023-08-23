---
UID: NF:strmif.IAMTVAudio.GetAvailableTVAudioModes
title: IAMTVAudio::GetAvailableTVAudioModes (strmif.h)
description: The GetAvailableTVAudioModes method retrieves a bitmask of the possible modes.
helpviewer_keywords: ["GetAvailableTVAudioModes","GetAvailableTVAudioModes method [DirectShow]","GetAvailableTVAudioModes method [DirectShow]","IAMTVAudio interface","IAMTVAudio interface [DirectShow]","GetAvailableTVAudioModes method","IAMTVAudio.GetAvailableTVAudioModes","IAMTVAudio::GetAvailableTVAudioModes","IAMTVAudioGetAvailableTVAudioModes","dshow.iamtvaudio_getavailabletvaudiomodes","strmif/IAMTVAudio::GetAvailableTVAudioModes"]
old-location: dshow\iamtvaudio_getavailabletvaudiomodes.htm
tech.root: dshow
ms.assetid: c64dc038-7ebf-4aa4-a7ae-b3eb0e8eaf1a
ms.date: 4/26/2023
ms.keywords: GetAvailableTVAudioModes, GetAvailableTVAudioModes method [DirectShow], GetAvailableTVAudioModes method [DirectShow],IAMTVAudio interface, IAMTVAudio interface [DirectShow],GetAvailableTVAudioModes method, IAMTVAudio.GetAvailableTVAudioModes, IAMTVAudio::GetAvailableTVAudioModes, IAMTVAudioGetAvailableTVAudioModes, dshow.iamtvaudio_getavailabletvaudiomodes, strmif/IAMTVAudio::GetAvailableTVAudioModes
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
 - IAMTVAudio::GetAvailableTVAudioModes
 - strmif/IAMTVAudio::GetAvailableTVAudioModes
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
 - IAMTVAudio.GetAvailableTVAudioModes
---

# IAMTVAudio::GetAvailableTVAudioModes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAvailableTVAudioModes</code> method retrieves a bitmask of the possible modes.

## -parameters

### -param plModes [out]

Pointer to a [TVAudioMode](/windows/desktop/api/strmif/ne-strmif-tvaudiomode) enumeration type, identifying the audio mode.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation. <b>HRESULT</b> can be one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Null pointer argument.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method isn't supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK or NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio Interface</a>