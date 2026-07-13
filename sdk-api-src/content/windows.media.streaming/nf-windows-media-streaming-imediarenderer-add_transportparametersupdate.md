---
UID: NF:windows.media.streaming.IMediaRenderer.add_TransportParametersUpdate
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Registers an event handler for the TransportParametersUpdate event.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","add_TransportParametersUpdate method","IMediaRenderer.add_TransportParametersUpdate","IMediaRenderer.streaming","IMediaRenderer::add_TransportParametersUpdate","IMediaRenderer::streaming","add_TransportParametersUpdate","add_TransportParametersUpdate method [Media Streaming API]","add_TransportParametersUpdate method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_add_transportparametersupdate","windows/IMediaRenderer::add_TransportParametersUpdate"]
old-location: mediastreaming\imediarenderer_add_transportparametersupdate.htm
tech.root: mediastreaming
ms.assetid: 34D11925-387B-414F-A176-336BBCF87821
ms.date: 4/26/2023
ms.keywords: IMediaRenderer interface [Media Streaming API],add_TransportParametersUpdate method, IMediaRenderer.add_TransportParametersUpdate, IMediaRenderer.streaming, IMediaRenderer::add_TransportParametersUpdate, IMediaRenderer::streaming, add_TransportParametersUpdate, add_TransportParametersUpdate method [Media Streaming API], add_TransportParametersUpdate method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_add_transportparametersupdate, windows/IMediaRenderer::add_TransportParametersUpdate
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
 - IMediaRenderer::add_TransportParametersUpdate
 - windows.media.streaming/IMediaRenderer::add_TransportParametersUpdate
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
 - IMediaRenderer.add_TransportParametersUpdate
---

# IMediaRenderer::streaming


## -description

\[The feature associated with this page, [Windows Media Streaming API](/windows/win32/mediastreaming/media-streaming-api-portal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). **Media Casting** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Media Casting** instead of **Windows Media Streaming API**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Registers an event handler for the <a href="/windows/desktop/mediastreaming/transportparametersupdate">TransportParametersUpdate</a> event.

## -parameters

### -param handler [in]

A <a href="/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)">TransportParametersUpdateHandler</a> event handler function.

### -param token [out, retval]

Reference to a token that can be used to unregister the event handler.

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

To unregister the event handler that was registered by this method, pass the <i>token</i> value to the <a href="/previous-versions/windows/desktop/legacy/hh828941(v=vs.85)">remove_TransportParametersUpdate</a> method.

## -see-also

<a href="/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a>