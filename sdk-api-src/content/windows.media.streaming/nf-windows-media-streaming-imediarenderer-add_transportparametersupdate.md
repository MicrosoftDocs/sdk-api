---
UID: NF:windows.media.streaming.IMediaRenderer.add_TransportParametersUpdate
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Registers an event handler for the TransportParametersUpdate event.
helpviewer_keywords: ["IMediaRenderer interface [Media Streaming API]","add_TransportParametersUpdate method","IMediaRenderer.add_TransportParametersUpdate","IMediaRenderer.streaming","IMediaRenderer::add_TransportParametersUpdate","IMediaRenderer::streaming","add_TransportParametersUpdate","add_TransportParametersUpdate method [Media Streaming API]","add_TransportParametersUpdate method [Media Streaming API]","IMediaRenderer interface","mediastreaming.imediarenderer_add_transportparametersupdate","windows/IMediaRenderer::add_TransportParametersUpdate"]
old-location: mediastreaming\imediarenderer_add_transportparametersupdate.htm
tech.root: mediastreaming
ms.assetid: 34D11925-387B-414F-A176-336BBCF87821
ms.date: 12/05/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],add_TransportParametersUpdate method, IMediaRenderer.add_TransportParametersUpdate, IMediaRenderer.streaming, IMediaRenderer::add_TransportParametersUpdate, IMediaRenderer::streaming, add_TransportParametersUpdate, add_TransportParametersUpdate method [Media Streaming API], add_TransportParametersUpdate method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_add_transportparametersupdate, windows/IMediaRenderer::add_TransportParametersUpdate
f1_keywords:
- windows.media.streaming/IMediaRenderer.add_TransportParametersUpdate
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
- IMediaRenderer.add_TransportParametersUpdate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaRenderer::streaming


## -description


Registers an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/transportparametersupdate">TransportParametersUpdate</a> event.


## -parameters




### -param handler [in]

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)">TransportParametersUpdateHandler</a> event handler function.


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



To unregister the event handler that was registered by this method, pass the <i>token</i> value to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828941(v=vs.85)">remove_TransportParametersUpdate</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a>
 

 

