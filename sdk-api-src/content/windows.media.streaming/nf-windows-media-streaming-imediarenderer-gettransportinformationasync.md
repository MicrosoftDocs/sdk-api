---
UID: NF:windows.media.streaming.IMediaRenderer.GetTransportInformationAsync
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Queries the DMR asynchronously to retrieve transport information.
old-location: mediastreaming\imediarenderer_gettransportinformationasync.htm
tech.root: mediastreaming
ms.assetid: C7EA3FB7-0D12-4E49-857F-D8311711AA89
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetTransportInformationAsync, GetTransportInformationAsync method [Media Streaming API], GetTransportInformationAsync method [Media Streaming API],IMediaRenderer interface, IMediaRenderer interface [Media Streaming API],GetTransportInformationAsync method, IMediaRenderer.GetTransportInformationAsync, IMediaRenderer.streaming, IMediaRenderer::GetTransportInformationAsync, IMediaRenderer::streaming, mediastreaming.imediarenderer_gettransportinformationasync, windows/IMediaRenderer::GetTransportInformationAsync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMediaRenderer.GetTransportInformationAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- windows.media.streaming.h
: 
- IMediaRenderer.GetTransportInformationAsync
: 
---

# IMediaRenderer::streaming


## -description


Queries the DMR asynchronously to retrieve transport information.


## -parameters




### -param value [out]

Receives a reference to a <a href="https://msdn.microsoft.com/EDB7E338-94E9-47DA-A95E-E49123655505">GetTransportInformationOperation</a>  object that is used to get results from the asynchronous operation.


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




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

