---
UID: NF:windows.media.streaming.IMediaRenderer.SetVolumeAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Sets the audio volume level on the DMR asynchronously to the specified value.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","SetVolumeAsync method","IMediaRenderer.SetVolumeAsync","IMediaRenderer.streaming","IMediaRenderer::SetVolumeAsync","IMediaRenderer::streaming","SetVolumeAsync","SetVolumeAsync method [Media Streaming API]","SetVolumeAsync method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_setvolumeasync","windows/IMediaRenderer::SetVolumeAsync"]
old-location: mediastreaming\imediarenderer_setvolumeasync.htm
tech.root: mediastreaming
ms.assetid: 422668F3-F5D6-440A-8BF1-A85B17E9A853
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetVolumeAsync method, IMediaRenderer.SetVolumeAsync, IMediaRenderer.streaming, IMediaRenderer::SetVolumeAsync, IMediaRenderer::streaming, SetVolumeAsync, SetVolumeAsync method [Media Streaming API], SetVolumeAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setvolumeasync, windows/IMediaRenderer::SetVolumeAsync
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
 - IMediaRenderer::SetVolumeAsync
 - windows.media.streaming/IMediaRenderer::SetVolumeAsync
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
 - IMediaRenderer.SetVolumeAsync
---

# IMediaRenderer::streaming


## -description

Sets the audio volume level on the DMR asynchronously to the specified value.

## -parameters

### -param volume [in]

A reference to the specified volume value.  The value must be in the range of 0 to 100, with 0 being the minimum volume and 100 being the maximum volume.

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