---
UID: NF:windows.media.streaming.IMediaRenderer.SetNextSourceFromStreamAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Instructs the DMR asynchronously to prepare the specified media stream for playing once the current content has finished playing.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","SetNextSourceFromStreamAsync method","IMediaRenderer.SetNextSourceFromStreamAsync","IMediaRenderer.streaming","IMediaRenderer::SetNextSourceFromStreamAsync","IMediaRenderer::streaming","SetNextSourceFromStreamAsync","SetNextSourceFromStreamAsync method [Media Streaming API]","SetNextSourceFromStreamAsync method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_setnextsourcefromstreamasync","windows/IMediaRenderer::SetNextSourceFromStreamAsync"]
old-location: mediastreaming\imediarenderer_setnextsourcefromstreamasync.htm
tech.root: mediastreaming
ms.assetid: 602B4C9B-88A3-4D91-9330-FC02E62F723A
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetNextSourceFromStreamAsync method, IMediaRenderer.SetNextSourceFromStreamAsync, IMediaRenderer.streaming, IMediaRenderer::SetNextSourceFromStreamAsync, IMediaRenderer::streaming, SetNextSourceFromStreamAsync, SetNextSourceFromStreamAsync method [Media Streaming API], SetNextSourceFromStreamAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setnextsourcefromstreamasync, windows/IMediaRenderer::SetNextSourceFromStreamAsync
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
 - IMediaRenderer::SetNextSourceFromStreamAsync
 - windows.media.streaming/IMediaRenderer::SetNextSourceFromStreamAsync
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
 - IMediaRenderer.SetNextSourceFromStreamAsync
---

# IMediaRenderer::streaming


## -description

Instructs the DMR asynchronously to prepare the specified media stream for playing once the current content has finished playing.

## -parameters

### -param stream [in]

A reference to an <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interface implementing <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a>. The <b>IMFActivate</b> interface is used to query for an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface that represents the media stream.

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

Once the DMR finishes playing the current content, it will automatically switch to the content specified by the <i>stream</i> parameter.

## -see-also

<a href="/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a>