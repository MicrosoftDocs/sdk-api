---
UID: NF:control.IMediaPosition.put_StopTime
title: IMediaPosition::put_StopTime (control.h)
description: The put_StopTime method sets the time at which the playback will stop, relative to the duration of the stream.
helpviewer_keywords: ["IMediaPosition interface [DirectShow]","put_StopTime method","IMediaPosition.put_StopTime","IMediaPosition::put_StopTime","IMediaPositionput_StopTime","control/IMediaPosition::put_StopTime","dshow.imediaposition_put_stoptime","put_StopTime","put_StopTime method [DirectShow]","put_StopTime method [DirectShow]","IMediaPosition interface"]
old-location: dshow\imediaposition_put_stoptime.htm
tech.root: dshow
ms.assetid: c068310e-4083-46ac-8ec6-3d57976f4a88
ms.date: 4/26/2023
ms.keywords: IMediaPosition interface [DirectShow],put_StopTime method, IMediaPosition.put_StopTime, IMediaPosition::put_StopTime, IMediaPositionput_StopTime, control/IMediaPosition::put_StopTime, dshow.imediaposition_put_stoptime, put_StopTime, put_StopTime method [DirectShow], put_StopTime method [DirectShow],IMediaPosition interface
req.header: control.h
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
 - IMediaPosition::put_StopTime
 - control/IMediaPosition::put_StopTime
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
 - IMediaPosition.put_StopTime
---

# IMediaPosition::put_StopTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_StopTime</code> method sets the time at which the playback will stop, relative to the duration of the stream.

## -parameters

### -param llTime [in]

Stop time, in seconds.

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
Not implemented.

</td>
</tr>
</table>

## -remarks

The stop time ignores the start time and the playback rate. For example, if the start time is 2 seconds, the stop time is 12 seconds, and the playback rate is 2.0, playback will stop after 5 seconds (real time).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition Interface</a>