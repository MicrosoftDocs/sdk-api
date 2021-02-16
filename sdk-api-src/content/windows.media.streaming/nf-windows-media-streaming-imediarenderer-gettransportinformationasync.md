---
UID: NF:windows.media.streaming.IMediaRenderer.GetTransportInformationAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
description: Queries the DMR asynchronously to retrieve transport information.
helpviewer_keywords: ["GetTransportInformationAsync","GetTransportInformationAsync method [Media Streaming API]","GetTransportInformationAsync method [Media Streaming API]","IMediaRenderer interface","IMediaRenderer interface [Media Streaming API]","GetTransportInformationAsync method","IMediaRenderer.GetTransportInformationAsync","IMediaRenderer.streaming","IMediaRenderer::GetTransportInformationAsync","IMediaRenderer::streaming","mediastreaming.imediarenderer_gettransportinformationasync","windows/IMediaRenderer::GetTransportInformationAsync"]
old-location: mediastreaming\imediarenderer_gettransportinformationasync.htm
tech.root: mediastreaming
ms.assetid: C7EA3FB7-0D12-4E49-857F-D8311711AA89
ms.date: 12/05/2018
ms.keywords: GetTransportInformationAsync, GetTransportInformationAsync method [Media Streaming API], GetTransportInformationAsync method [Media Streaming API],IMediaRenderer interface, IMediaRenderer interface [Media Streaming API],GetTransportInformationAsync method, IMediaRenderer.GetTransportInformationAsync, IMediaRenderer.streaming, IMediaRenderer::GetTransportInformationAsync, IMediaRenderer::streaming, mediastreaming.imediarenderer_gettransportinformationasync, windows/IMediaRenderer::GetTransportInformationAsync
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
 - IMediaRenderer::GetTransportInformationAsync
 - windows.media.streaming/IMediaRenderer::GetTransportInformationAsync
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
 - IMediaRenderer.GetTransportInformationAsync
---

# IMediaRenderer::streaming


## -description

Queries the DMR asynchronously to retrieve transport information.

## -parameters

### -param value [out]

Receives a reference to a <a href="/windows/desktop/mediastreaming/gettransportinformationoperation">GetTransportInformationOperation</a>  object that is used to get results from the asynchronous operation.

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