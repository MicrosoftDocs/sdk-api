---
UID: NF:windows.media.streaming.IMediaRenderer.PauseAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Instructs the DMR asynchronously to pause playing the current content.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","PauseAsync method","IMediaRenderer.PauseAsync","IMediaRenderer.streaming","IMediaRenderer::PauseAsync","IMediaRenderer::streaming","PauseAsync","PauseAsync method [Media Streaming API]","PauseAsync method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_pauseasync","windows/IMediaRenderer::PauseAsync"]
old-location: mediastreaming\imediarenderer_pauseasync.htm
tech.root: mediastreaming
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],PauseAsync method, IMediaRenderer.PauseAsync, IMediaRenderer.streaming, IMediaRenderer::PauseAsync, IMediaRenderer::streaming, PauseAsync, PauseAsync method [Media Streaming API], PauseAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_pauseasync, windows/IMediaRenderer::PauseAsync
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
 - IMediaRenderer::PauseAsync
 - windows.media.streaming/IMediaRenderer::PauseAsync
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
 - IMediaRenderer.PauseAsync
---

# IMediaRenderer::streaming


## -description

Instructs the DMR asynchronously to pause playing the current content.

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

## -see-also

<a href="/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a>