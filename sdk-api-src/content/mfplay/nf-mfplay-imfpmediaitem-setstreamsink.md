---
UID: NF:mfplay.IMFPMediaItem.SetStreamSink
title: IMFPMediaItem::SetStreamSink (mfplay.h)
description: Sets a media sink for the media item.
helpviewer_keywords: ["IMFPMediaItem interface [Media Foundation]","SetStreamSink method","IMFPMediaItem.SetStreamSink","IMFPMediaItem::SetStreamSink","SetStreamSink","SetStreamSink method [Media Foundation]","SetStreamSink method [Media Foundation]","IMFPMediaItem interface","mf.imfpmediaitem_setstreamsink","mfplay/IMFPMediaItem::SetStreamSink"]
old-location: mf\imfpmediaitem_setstreamsink.htm
tech.root: mfarchive
archived: true
ms.assetid: 97ed9cc0-5f69-4ecb-98c7-c58130b91d7c
ms.date: 12/05/2018
ms.keywords: IMFPMediaItem interface [Media Foundation],SetStreamSink method, IMFPMediaItem.SetStreamSink, IMFPMediaItem::SetStreamSink, SetStreamSink, SetStreamSink method [Media Foundation], SetStreamSink method [Media Foundation],IMFPMediaItem interface, mf.imfpmediaitem_setstreamsink, mfplay/IMFPMediaItem::SetStreamSink
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
 - IMFPMediaItem::SetStreamSink
 - mfplay/IMFPMediaItem::SetStreamSink
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
 - IMFPMediaItem.SetStreamSink
---

# IMFPMediaItem::SetStreamSink


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Sets a media sink for the media item. A <i>media sink</i> is an object that consumes the data from one or more streams.

## -parameters

### -param dwStreamIndex [in]

Zero-based index of a stream on the media source. The media sink will receive the data from this stream.

### -param pMediaSink [in]

<b>IUnknown</b> pointer that specifies the media sink. Pass in one of the following:

<ul>
<li>A pointer to a stream sink. Every media sink contains one or more <i>stream sinks</i>. Each stream sink receives the data from one stream. The stream sink must expose the  <a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a> interface.</li>
<li>A pointer to an activation object that creates the media sink. The activation object must expose the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface. The media item uses the first stream sink on the media sink (that is, the stream sink at index 0).</li>
<li><b>NULL</b>. If you set <i>pMediaSink</i> to <b>NULL</b>, the default media sink for the stream type is used.</li>
</ul>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

By default, the MFPlay player object renders audio streams to the <a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a> (SAR) and video streams to the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR). You can use the <b>SetStreamSink</b> method to provide a different media sink for an audio or video stream; or to support other stream types besides audio and video. You can also use it to configure the SAR or EVR before they are used.

Call this method before calling <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem">IMFPMediaPlayer::SetMediaItem</a>. Calling this method after <b>SetMediaItem</b> has no effect, unless you stop playback and call <b>SetMediaItem</b> again.

To reset the media item to use the default media sink, set <i>pMediaSink</i> to <b>NULL</b>.

<h3><a id="Remote_Playback_Optimizations"></a><a id="remote_playback_optimizations"></a><a id="REMOTE_PLAYBACK_OPTIMIZATIONS"></a>Remote Playback Optimizations</h3>
If the application is running over Remote Desktop, and you call this method with a non-NULL value for an audio or video stream, MFPlay disables remote playback optimizations. This remark applies only to audio and video streams. It does not apply to streams that contain some other data type, such as text.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>