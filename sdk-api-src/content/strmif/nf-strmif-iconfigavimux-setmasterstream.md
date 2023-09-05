---
UID: NF:strmif.IConfigAviMux.SetMasterStream
title: IConfigAviMux::SetMasterStream (strmif.h)
description: The SetMasterStream method specifies a stream that will be used to synchronize the other streams in the file.
helpviewer_keywords: ["IConfigAviMux interface [DirectShow]","SetMasterStream method","IConfigAviMux.SetMasterStream","IConfigAviMux::SetMasterStream","IConfigAviMuxSetMasterStream","SetMasterStream","SetMasterStream method [DirectShow]","SetMasterStream method [DirectShow]","IConfigAviMux interface","dshow.iconfigavimux_setmasterstream","strmif/IConfigAviMux::SetMasterStream"]
old-location: dshow\iconfigavimux_setmasterstream.htm
tech.root: dshow
ms.assetid: 1f255498-8bbb-48a0-ae97-0cf2698e609b
ms.date: 4/26/2023
ms.keywords: IConfigAviMux interface [DirectShow],SetMasterStream method, IConfigAviMux.SetMasterStream, IConfigAviMux::SetMasterStream, IConfigAviMuxSetMasterStream, SetMasterStream, SetMasterStream method [DirectShow], SetMasterStream method [DirectShow],IConfigAviMux interface, dshow.iconfigavimux_setmasterstream, strmif/IConfigAviMux::SetMasterStream
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
 - IConfigAviMux::SetMasterStream
 - strmif/IConfigAviMux::SetMasterStream
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
 - IConfigAviMux.SetMasterStream
---

# IConfigAviMux::SetMasterStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetMasterStream</code> method specifies a stream that will be used to synchronize the other streams in the file.

## -parameters

### -param iStream [in]

Specifies the index of the stream, or –1 to indicate no master stream. The AVI Mux writes one stream for each connected input pin. Stream numbers are indexed from zero.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

If you are capturing audio and video from two different sources, use this method to synchronize the streams. Streams coming from separate capture sources may be captured at slightly different rates. If you specify a master stream, the AVI Mux adjusts the playback rates for the other streams, to compensate for any drift that might occur.

It is recommended to use the audio stream as the master stream, because minor adjustments to the video playback rate are less noticeable than changes to the audio playback rate. Also, modifying the audio playback rate will cause the audio to be resampled by the audio driver.

This method works by adjusting the <i>dwScale</i> and <i>dwRate</i> values in the <a href="/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader">AVISTREAMHEADER</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/avi-riff-file-reference">AVI RIFF File Reference</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iconfigavimux">IConfigAviMux Interface</a>