---
UID: NF:strmif.IAMExtTransport.put_Mode
title: IAMExtTransport::put_Mode (strmif.h)
description: The put_Mode method sets the transport mode; for example, play, stop, or record.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","put_Mode method","IAMExtTransport.put_Mode","IAMExtTransport::put_Mode","IAMExtTransportput_Mode","dshow.iamexttransport_put_mode","put_Mode","put_Mode method [DirectShow]","put_Mode method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::put_Mode"]
old-location: dshow\iamexttransport_put_mode.htm
tech.root: dshow
ms.assetid: cf941c07-6f42-4c63-9bdf-923f7a5b0b02
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],put_Mode method, IAMExtTransport.put_Mode, IAMExtTransport::put_Mode, IAMExtTransportput_Mode, dshow.iamexttransport_put_mode, put_Mode, put_Mode method [DirectShow], put_Mode method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_Mode
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
 - IAMExtTransport::put_Mode
 - strmif/IAMExtTransport::put_Mode
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
 - IAMExtTransport.put_Mode
---

# IAMExtTransport::put_Mode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_Mode</b> method sets the transport mode; for example, play, stop, or record.

## -parameters

### -param Mode [in]

Specifies the transport mode. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_MODE_PLAY</td>
<td>Play.</td>
</tr>
<tr>
<td>ED_MODE_STOP</td>
<td>Stop.</td>
</tr>
<tr>
<td>ED_MODE_FREEZE</td>
<td>Pause.</td>
</tr>
<tr>
<td>ED_MODE_THAW</td>
<td>Resume.</td>
</tr>
<tr>
<td>ED_MODE_FF</td>
<td>Fast forward.</td>
</tr>
<tr>
<td>ED_MODE_REW</td>
<td>Rewind.</td>
</tr>
<tr>
<td>ED_MODE_RECORD</td>
<td>Record.</td>
</tr>
<tr>
<td>ED_MODE_RECORD_FREEZE</td>
<td>Pause recording.</td>
</tr>
<tr>
<td>ED_MODE_RECORD_STROBE</td>
<td>Record single frame.</td>
</tr>
<tr>
<td>ED_MODE_STEP_FWD</td>
<td>Single step forward.</td>
</tr>
<tr>
<td>ED_MODE_STEP_REV</td>
<td>Single step backward.</td>
</tr>
<tr>
<td>ED_MODE_SHUTTLE</td>
<td>Shuttle (high-speed movement with visible picture). Use with <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_rate">IAMExtTransport::put_Rate</a> to set the transport speed.</td>
</tr>
<tr>
<td>ED_MODE_EDIT_CUE</td>
<td>Position transport to the cue point for an active edit event.</td>
</tr>
<tr>
<td>ED_MODE_LINK_ON</td>
<td>Link this method to the graph's <a href="/windows/desktop/api/control/nf-control-imediacontrol-run">IMediaControl::Run</a>, <a href="/windows/desktop/api/control/nf-control-imediacontrol-stop">IMediaControl::Stop</a>, and <a href="/windows/desktop/api/control/nf-control-imediacontrol-pause">IMediaControl::Pause</a> methods.</td>
</tr>
<tr>
<td>ED_MODE_LINK_OFF</td>
<td>Disengage this method from the graph's <b>IMediaControl</b> methods.</td>
</tr>
</table>

## -returns

Returns an HRESULT. Possible errors include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_REQ_NOT_ACCEP)</b></dt>
</dl>
</td>
<td width="60%">
The device did not accept the command.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_mode">IAMExtTransport::get_Mode</a>