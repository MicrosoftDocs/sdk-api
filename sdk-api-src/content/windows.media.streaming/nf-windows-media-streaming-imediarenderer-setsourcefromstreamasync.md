---
UID: NF:windows.media.streaming.IMediaRenderer.SetSourceFromStreamAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Instructs the DMR asynchronously to prepare the specified media stream for playing.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","SetSourceFromStreamAsync method","IMediaRenderer.SetSourceFromStreamAsync","IMediaRenderer.streaming","IMediaRenderer::SetSourceFromStreamAsync","IMediaRenderer::streaming","SetSourceFromStreamAsync","SetSourceFromStreamAsync method [Media Streaming API]","SetSourceFromStreamAsync method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_setsourcefromstreamasync","windows/IMediaRenderer::SetSourceFromStreamAsync"]
old-location: mediastreaming\imediarenderer_setsourcefromstreamasync.htm
tech.root: mediastreaming
ms.assetid: BBFEDCE1-A7C4-4F7E-AC22-0F117EA075CE
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetSourceFromStreamAsync method, IMediaRenderer.SetSourceFromStreamAsync, IMediaRenderer.streaming, IMediaRenderer::SetSourceFromStreamAsync, IMediaRenderer::streaming, SetSourceFromStreamAsync, SetSourceFromStreamAsync method [Media Streaming API], SetSourceFromStreamAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setsourcefromstreamasync, windows/IMediaRenderer::SetSourceFromStreamAsync
f1_keywords:
- windows.media.streaming/IMediaRenderer.SetSourceFromStreamAsync
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- windows.media.streaming.h
api_name:
- IMediaRenderer.SetSourceFromStreamAsync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaRenderer::streaming


## -description


Instructs the DMR asynchronously to prepare the specified media stream for playing.


## -parameters




### -param stream [in]

A reference to an <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interface implementing <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a>. The <b>IMFActivate</b> interface is used to query for an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface that represents the media stream.


### -param value [out]

Receives a reference to a <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/playbackoperation">PlaybackOperation</a> object that is used to get results from the asynchronous operation.


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



If the DMR is not currently playing anything, the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828938(v=vs.85)">PlayAsync</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828939(v=vs.85)">PlayAtSpeedAsync</a> method must be used to instruct the DMR to start playing.  
If the DMR is already playing content, it will automatically switch to the content provided by the <i>stream</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a>
 

 

