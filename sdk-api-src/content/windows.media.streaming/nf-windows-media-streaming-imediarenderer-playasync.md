---
UID: NF:windows.media.streaming.IMediaRenderer.PlayAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Instructs the DMR asynchronously to play the content that was specified by calling the SetSourceFromUriAsync, SetSourceFromStreamAsync, or SetSourceFromMediaSourceAsync method.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","PlayAsync method","IMediaRenderer.PlayAsync","IMediaRenderer.streaming","IMediaRenderer::PlayAsync","IMediaRenderer::streaming","PlayAsync","PlayAsync method [Media Streaming API]","PlayAsync method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_playasync","windows/IMediaRenderer::PlayAsync"]
old-location: mediastreaming\imediarenderer_playasync.htm
tech.root: mediastreaming
ms.assetid: 32084664-2D1B-4303-B3B7-9B896A07CB17
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],PlayAsync method, IMediaRenderer.PlayAsync, IMediaRenderer.streaming, IMediaRenderer::PlayAsync, IMediaRenderer::streaming, PlayAsync, PlayAsync method [Media Streaming API], PlayAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_playasync, windows/IMediaRenderer::PlayAsync
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
 - IMediaRenderer::PlayAsync
 - windows.media.streaming/IMediaRenderer::PlayAsync
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
 - IMediaRenderer.PlayAsync
---

# IMediaRenderer::streaming


## -description

Instructs the DMR asynchronously to play the content that was specified by calling the <a href="/previous-versions/windows/desktop/legacy/hh828949(v=vs.85)">SetSourceFromUriAsync</a>, <a href="/previous-versions/windows/desktop/legacy/hh828948(v=vs.85)">SetSourceFromStreamAsync</a>, or <a href="/previous-versions/windows/desktop/legacy/hh828947(v=vs.85)">SetSourceFromMediaSourceAsync</a> method.

## -parameters

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

## -remarks

Before this method is called, you must call <a href="/previous-versions/windows/desktop/legacy/hh828949(v=vs.85)">SetSourceFromUriAsync</a>, <a href="/previous-versions/windows/desktop/legacy/hh828948(v=vs.85)">SetSourceFromStreamAsync</a>, or <a href="/previous-versions/windows/desktop/legacy/hh828947(v=vs.85)">SetSourceFromMediaSourceAsync</a> first to specify the content.

The content will be played at the normal playback rate of "1".
A different playback rate can be specified by calling the <a href="/previous-versions/windows/desktop/legacy/hh828939(v=vs.85)">PlayAtSpeedAsync</a> method.

## -see-also

<a href="/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a>