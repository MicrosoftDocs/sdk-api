---
UID: NF:mfplay.IMFPMediaPlayer.SetPosition
title: IMFPMediaPlayer::SetPosition (mfplay.h)
description: Sets the playback position.
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","SetPosition method","IMFPMediaPlayer.SetPosition","IMFPMediaPlayer::SetPosition","MFP_POSITIONTYPE_100NS","SetPosition","SetPosition method [Media Foundation]","SetPosition method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_setposition","mfplay/IMFPMediaPlayer::SetPosition"]
old-location: mf\imfpmediaplayer_setposition.htm
tech.root: mfarchive
archived: true
ms.assetid: d8665c3b-e0da-4a6f-a61b-38d507d1e78a
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetPosition method, IMFPMediaPlayer.SetPosition, IMFPMediaPlayer::SetPosition, MFP_POSITIONTYPE_100NS, SetPosition, SetPosition method [Media Foundation], SetPosition method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setposition, mfplay/IMFPMediaPlayer::SetPosition
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMediaPlayer::SetPosition
 - mfplay/IMFPMediaPlayer::SetPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayer.SetPosition
---

# IMFPMediaPlayer::SetPosition


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Sets the playback position.

## -parameters

### -param guidPositionType [in]

Unit of time for the playback position. The following value is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFP_POSITIONTYPE_100NS"></a><a id="mfp_positiontype_100ns"></a><dl>
<dt><b>MFP_POSITIONTYPE_100NS</b></dt>
</dl>
</td>
<td width="60%">
100-nanosecond units. 

The value of <i>pvPositionValue</i> must be a <b>LARGE_INTEGER</b>.

<ul>
<li>Variant type (<b>vt</b>): <b>VT_I8</b></li>
<li>Variant member: <b>hVal</b></li>
</ul>
</td>
</tr>
</table>

### -param pvPositionValue [in]

New playback position. The meaning and data type of this parameter are indicated by the <i>guidPositionType</i> parameter.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

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
<dt><b>HRESULT_FROM_WIN32( ERROR_SEEK )</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pvPositionValue</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
No media item has been queued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a> method was called.

</td>
</tr>
</table>

## -remarks

If you call this method while playback is stopped, the new position takes effect after playback resumes.

This method completes asynchronously. When the operation completes, the application's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_POSITION_SET</b>.

If playback was started before <b>SetPosition</b> is called, playback resumes at the new position. If playback was paused, the video is refreshed to display the current frame at the new position. 

If you make two consecutive calls to <b>SetPosition</b> with <i>guidPositionType</i> equal to <b>MFP_POSITIONTYPE_100NS</b>, and the second call is made before the first call has completed, the second call supersedes the first. The status code for the superseded call is set to <b>S_FALSE</b> in the event data for that call. This behavior prevents excessive latency from repeated calls to <b>SetPosition</b>, as each call may force the media source to perform a relatively lengthy seek operation.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>