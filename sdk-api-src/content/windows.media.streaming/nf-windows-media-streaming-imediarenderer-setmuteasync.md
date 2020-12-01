---
UID: NF:windows.media.streaming.IMediaRenderer.SetMuteAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Instructs the DMR asynchronously to either mute or unmute the audio.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","SetMuteAsync method","IMediaRenderer.SetMuteAsync","IMediaRenderer.streaming","IMediaRenderer::SetMuteAsync","IMediaRenderer::streaming","SetMuteAsync","SetMuteAsync method [Media Streaming API]","SetMuteAsync method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_setmuteasync","windows/IMediaRenderer::SetMuteAsync"]
old-location: mediastreaming\imediarenderer_setmuteasync.htm
tech.root: mediastreaming
ms.assetid: C043088B-5043-457A-A104-5CE0B228222A
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetMuteAsync method, IMediaRenderer.SetMuteAsync, IMediaRenderer.streaming, IMediaRenderer::SetMuteAsync, IMediaRenderer::streaming, SetMuteAsync, SetMuteAsync method [Media Streaming API], SetMuteAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setmuteasync, windows/IMediaRenderer::SetMuteAsync
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMediaRenderer::SetMuteAsync
 - windows.media.streaming/IMediaRenderer::SetMuteAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.streaming.h
api_name:
 - IMediaRenderer.SetMuteAsync
---

# IMediaRenderer::streaming


## -description

Instructs the DMR asynchronously to either mute or unmute the audio.

## -parameters

### -param mute [in]

A reference to a boolean value that specifies the mute setting. A value of True specifies that mute is turned on, and a value of False specifies that it is turned off.

### -param value [out]

Receives a reference to a <a href="/windows/desktop/mediastreaming/playbackoperation">PlaybackOperation</a> object that is used to get results from the asynchronous operation.

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
</table>

## -see-also

<a href="/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a>