---
UID: NF:windows.media.streaming.IMediaRendererFactory.CreateMediaRendererAsync
title: IMediaRendererFactory::streaming (windows.media.streaming.h)
description: Asynchronously creates a new instance of an object that implements the IMediaRenderer interface using the specified Unique Device Name (UDN).
helpviewer_keywords: ["CreateMediaRendererAsync","CreateMediaRendererAsync method [Media Streaming API]","CreateMediaRendererAsync method [Media Streaming API]","IMediaRendererFactory interface","IMediaRendererFactory interface [Media Streaming API]","CreateMediaRendererAsync method","IMediaRendererFactory.CreateMediaRendererAsync","IMediaRendererFactory.streaming","IMediaRendererFactory::CreateMediaRendererAsync","IMediaRendererFactory::streaming","mediastreaming.imediarendererfactory_createmediarendererasync","windows/IMediaRendererFactory::CreateMediaRendererAsync"]
old-location: mediastreaming\imediarendererfactory_createmediarendererasync.htm
tech.root: mediastreaming
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
ms.date: 12/05/2018
ms.keywords: CreateMediaRendererAsync, CreateMediaRendererAsync method [Media Streaming API], CreateMediaRendererAsync method [Media Streaming API],IMediaRendererFactory interface, IMediaRendererFactory interface [Media Streaming API],CreateMediaRendererAsync method, IMediaRendererFactory.CreateMediaRendererAsync, IMediaRendererFactory.streaming, IMediaRendererFactory::CreateMediaRendererAsync, IMediaRendererFactory::streaming, mediastreaming.imediarendererfactory_createmediarendererasync, windows/IMediaRendererFactory::CreateMediaRendererAsync
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
 - IMediaRendererFactory::CreateMediaRendererAsync
 - windows.media.streaming/IMediaRendererFactory::CreateMediaRendererAsync
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
 - IMediaRendererFactory.CreateMediaRendererAsync
---

# IMediaRendererFactory::streaming


## -description

Asynchronously creates a new instance of an object that implements the <a href="/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a> interface using the specified Unique Device Name (UDN).

## -parameters

### -param deviceIdentifier [in]

An HSTRING containing a UDN that identifies the DLNA DMR device for which an instance of <a href="/windows/desktop/mediastreaming/imediarenderer">IMediaRenderer</a> will be created.

### -param value [out, retval]

Receives a reference to a <a href="/windows/desktop/mediastreaming/createmediarendereroperation">CreateMediaRendererOperation</a> object that is used to get results from the asynchronous operation.

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

<a href="/previous-versions/windows/desktop/legacy/hh828924(v=vs.85)">IMediaRendererFactory</a>