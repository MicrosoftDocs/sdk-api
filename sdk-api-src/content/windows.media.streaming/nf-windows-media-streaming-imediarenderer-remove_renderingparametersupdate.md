---
UID: NF:windows.media.streaming.IMediaRenderer.remove_RenderingParametersUpdate
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Unregisters an event handler for the RenderingParametersUpdate event.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","remove_RenderingParametersUpdate method","IMediaRenderer.remove_RenderingParametersUpdate","IMediaRenderer.streaming","IMediaRenderer::remove_RenderingParametersUpdate","IMediaRenderer::streaming","mediastreaming.imediarenderer_remove_renderingparametersupdate","remove_RenderingParametersUpdate","remove_RenderingParametersUpdate method [Media Streaming API]","remove_RenderingParametersUpdate method [Media Streaming API]","IMediaRenderer interface","windows/IMediaRenderer::remove_RenderingParametersUpdate"]
old-location: mediastreaming\imediarenderer_remove_renderingparametersupdate.htm
tech.root: mediastreaming
ms.assetid: 5642D180-7FE8-4058-B346-109D5C5817F6
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],remove_RenderingParametersUpdate method, IMediaRenderer.remove_RenderingParametersUpdate, IMediaRenderer.streaming, IMediaRenderer::remove_RenderingParametersUpdate, IMediaRenderer::streaming, mediastreaming.imediarenderer_remove_renderingparametersupdate, remove_RenderingParametersUpdate, remove_RenderingParametersUpdate method [Media Streaming API], remove_RenderingParametersUpdate method [Media Streaming API],IMediaRenderer interface, windows/IMediaRenderer::remove_RenderingParametersUpdate
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
 - IMediaRenderer::remove_RenderingParametersUpdate
 - windows.media.streaming/IMediaRenderer::remove_RenderingParametersUpdate
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
 - IMediaRenderer.remove_RenderingParametersUpdate
---

# IMediaRenderer::streaming


## -description

Unregisters an event handler for the <a href="/windows/desktop/mediastreaming/renderingparametersupdate">RenderingParametersUpdate</a> event.

## -parameters

### -param token [in]

A reference to a token obtained from the <a href="/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate">add_RenderingParametersUpdate</a> method when the event handler was registered.

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