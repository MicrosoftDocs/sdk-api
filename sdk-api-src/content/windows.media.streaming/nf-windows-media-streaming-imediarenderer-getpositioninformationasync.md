---
UID: NF:windows.media.streaming.IMediaRenderer.GetPositionInformationAsync
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Queries the DMR asynchronously to retrieve position information.
old-location: mediastreaming\imediarenderer_getpositioninformationasync.htm
tech.root: mediastreaming
ms.assetid: 07011C85-34C5-430A-9551-FFC7C24CCED8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPositionInformationAsync, GetPositionInformationAsync method [Media Streaming API], GetPositionInformationAsync method [Media Streaming API],IMediaRenderer interface, IMediaRenderer interface [Media Streaming API],GetPositionInformationAsync method, IMediaRenderer.GetPositionInformationAsync, IMediaRenderer.streaming, IMediaRenderer::GetPositionInformationAsync, IMediaRenderer::streaming, mediastreaming.imediarenderer_getpositioninformationasync, windows/IMediaRenderer::GetPositionInformationAsync
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
 - IMediaRenderer.GetPositionInformationAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Queries the DMR asynchronously to retrieve position information.


## -parameters




### -param value [out]

Receives a reference to a  <a href="https://msdn.microsoft.com/57DDE3B2-EFA9-4FEB-B701-D987C58F5CEA">GetPositionInformationOperation</a> object that is used to get results from the asynchronous operation.


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
 

 

