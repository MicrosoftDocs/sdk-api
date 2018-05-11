---
UID: NF:mfplay.IMFPMediaItem.SetStreamSink
title: IMFPMediaItem::SetStreamSink
author: windows-driver-content
description: Sets a media sink for the media item.
old-location: mf\imfpmediaitem_setstreamsink.htm
old-project: medfound
ms.assetid: 97ed9cc0-5f69-4ecb-98c7-c58130b91d7c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFPMediaItem interface [Media Foundation],SetStreamSink method, IMFPMediaItem.SetStreamSink, IMFPMediaItem::SetStreamSink, SetStreamSink, SetStreamSink method [Media Foundation], SetStreamSink method [Media Foundation],IMFPMediaItem interface, mf.imfpmediaitem_setstreamsink, mfplay/IMFPMediaItem::SetStreamSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplay.h
api_name:
-	IMFPMediaItem.SetStreamSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaItem::SetStreamSink


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>



        Sets a media sink for the media item. A <i>media sink</i> is an object that consumes the data from one or more streams.
      


## -parameters




### -param dwStreamIndex [in]

Zero-based index of a stream on the media source. The media sink will receive the data from this stream.


### -param pMediaSink [in]

<b>IUnknown</b> pointer that specifies the media sink. Pass in one of the following:

<ul>
<li>A pointer to a stream sink. Every media sink contains one or more <i>stream sinks</i>. Each stream sink receives the data from one stream. The stream sink must expose the  <a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a> interface.</li>
<li>A pointer to an activation object that creates the media sink. The activation object must expose the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface. The media item uses the first stream sink on the media sink (that is, the stream sink at index 0).</li>
<li><b>NULL</b>. If you set <i>pMediaSink</i> to <b>NULL</b>, the default media sink for the stream type is used.</li>
</ul>

## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



By default, the MFPlay player object renders audio streams to the <a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a> (SAR) and video streams to the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR). You can use the <b>SetStreamSink</b> method to provide a different media sink for an audio or video stream; or to support other stream types besides audio and video. You can also use it to configure the SAR or EVR before they are used.

Call this method before calling <a href="https://msdn.microsoft.com/c792a024-c4f8-4e0b-9720-259d1dc28ee8">IMFPMediaPlayer::SetMediaItem</a>. Calling this method after <b>SetMediaItem</b> has no effect, unless you stop playback and call <b>SetMediaItem</b> again.

To reset the media item to use the default media sink, set <i>pMediaSink</i> to <b>NULL</b>.

<h3><a id="Remote_Playback_Optimizations"></a><a id="remote_playback_optimizations"></a><a id="REMOTE_PLAYBACK_OPTIMIZATIONS"></a>Remote Playback Optimizations</h3>
If the application is running over Remote Desktop, and you call this method with a non-NULL value for an audio or video stream, MFPlay disables remote playback optimizations. This remark applies only to audio and video streams. It does not apply to streams that contain some other data type, such as text.




## -see-also




<a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

