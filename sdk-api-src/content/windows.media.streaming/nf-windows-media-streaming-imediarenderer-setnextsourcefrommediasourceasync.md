---
UID: NF:windows.media.streaming.IMediaRenderer.SetNextSourceFromMediaSourceAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Instructs the DMR asynchronously to prepare the specified content for playing once the current content has finished playing.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","SetNextSourceFromMediaSourceAsync method","IMediaRenderer.SetNextSourceFromMediaSourceAsync","IMediaRenderer.streaming","IMediaRenderer::SetNextSourceFromMediaSourceAsync","IMediaRenderer::streaming","SetNextSourceFromMediaSourceAsync","SetNextSourceFromMediaSourceAsync method [Media Streaming API]","SetNextSourceFromMediaSourceAsync method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_setnextsourcefrommediasourceasync","windows/IMediaRenderer::SetNextSourceFromMediaSourceAsync"]
old-location: mediastreaming\imediarenderer_setnextsourcefrommediasourceasync.htm
tech.root: mediastreaming
ms.assetid: 054203C8-766B-4448-A275-CA61C9D177AD
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetNextSourceFromMediaSourceAsync method, IMediaRenderer.SetNextSourceFromMediaSourceAsync, IMediaRenderer.streaming, IMediaRenderer::SetNextSourceFromMediaSourceAsync, IMediaRenderer::streaming, SetNextSourceFromMediaSourceAsync, SetNextSourceFromMediaSourceAsync method [Media Streaming API], SetNextSourceFromMediaSourceAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setnextsourcefrommediasourceasync, windows/IMediaRenderer::SetNextSourceFromMediaSourceAsync
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
 - IMediaRenderer::SetNextSourceFromMediaSourceAsync
 - windows.media.streaming/IMediaRenderer::SetNextSourceFromMediaSourceAsync
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
 - IMediaRenderer.SetNextSourceFromMediaSourceAsync
---

# IMediaRenderer::streaming


## -description

Instructs the DMR asynchronously to prepare the specified content for playing once the current content has finished playing.

## -parameters

### -param mediaSource [in]

A reference to an <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interface implementing <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a>. The <b>IMFActivate</b> interface is used to query for an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface that represents the media source.

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

Once the DMR finishes playing the current content, it will automatically switch to the content specified by the <i>mediaSource</i> parameter.

## -see-also

<a href="/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a>