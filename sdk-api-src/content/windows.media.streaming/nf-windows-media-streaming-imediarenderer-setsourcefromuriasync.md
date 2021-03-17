---
UID: NF:windows.media.streaming.IMediaRenderer.SetSourceFromUriAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","SetSourceFromUriAsync method","IMediaRenderer.SetSourceFromUriAsync","IMediaRenderer.streaming","IMediaRenderer::SetSourceFromUriAsync","IMediaRenderer::streaming","SetSourceFromUriAsync","SetSourceFromUriAsync method [Media Streaming API]","SetSourceFromUriAsync method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_setsourcefromuriasync","windows/IMediaRenderer::SetSourceFromUriAsync"]
old-location: mediastreaming\imediarenderer_setsourcefromuriasync.htm
tech.root: mediastreaming
ms.assetid: 3062FC13-61FD-4781-9AE6-39576D86B783
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetSourceFromUriAsync method, IMediaRenderer.SetSourceFromUriAsync, IMediaRenderer.streaming, IMediaRenderer::SetSourceFromUriAsync, IMediaRenderer::streaming, SetSourceFromUriAsync, SetSourceFromUriAsync method [Media Streaming API], SetSourceFromUriAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setsourcefromuriasync, windows/IMediaRenderer::SetSourceFromUriAsync
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
 - IMediaRenderer::SetSourceFromUriAsync
 - windows.media.streaming/IMediaRenderer::SetSourceFromUriAsync
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
 - IMediaRenderer.SetSourceFromUriAsync
---

# IMediaRenderer::streaming


## -description

Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing.

## -parameters

### -param URI [in]

An HSTRING containing the file path or resource location of media content.

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

If the DMR is not currently playing anything, the <a href="/previous-versions/windows/desktop/legacy/hh828938(v=vs.85)">PlayAsync</a> or <a href="/previous-versions/windows/desktop/legacy/hh828939(v=vs.85)">PlayAtSpeedAsync</a> method must be used to instruct the DMR to start playing.  
If the DMR is already playing content, it will automatically switch to the content provided by the <i>URI</i> parameter.

## -see-also

<a href="/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a>