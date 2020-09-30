---
UID: NF:windows.media.streaming.IMediaRenderer.SeekAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Instructs the DMR asynchronously to seek to a particular time offset.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","SeekAsync method","IMediaRenderer.SeekAsync","IMediaRenderer.streaming","IMediaRenderer::SeekAsync","IMediaRenderer::streaming","SeekAsync","SeekAsync method [Media Streaming API]","SeekAsync method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_seekasync","windows/IMediaRenderer::SeekAsync"]
old-location: mediastreaming\imediarenderer_seekasync.htm
tech.root: mediastreaming
ms.assetid: 3179A942-7756-4763-A2F8-629D89D39542
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SeekAsync method, IMediaRenderer.SeekAsync, IMediaRenderer.streaming, IMediaRenderer::SeekAsync, IMediaRenderer::streaming, SeekAsync, SeekAsync method [Media Streaming API], SeekAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_seekasync, windows/IMediaRenderer::SeekAsync
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
 - IMediaRenderer::SeekAsync
 - windows.media.streaming/IMediaRenderer::SeekAsync
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
 - IMediaRenderer.SeekAsync
---

# IMediaRenderer::streaming


## -description

Instructs the DMR asynchronously to seek to a particular time offset.

## -parameters

### -param target [in]

A <a href="/previous-versions/windows/desktop/axe/timespan">TimeSpan</a> value that specifies the seek offset. This value must be 0 (indicating the beginning of the content) or greater, but less than the value of <a href="/previous-versions/windows/desktop/legacy/hh828991(v=vs.85)">PositionInformation.TrackDuration</a> which is obtained by calling <a href="/previous-versions/windows/desktop/legacy/hh828931(v=vs.85)">GetPositionInformationAsync</a>.

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