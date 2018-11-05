---
UID: NF:windows.media.streaming.IMediaRenderer.GetMuteAsync
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Queries the DMR asynchronously to determine if audio is currently muted or unmuted.
old-location: mediastreaming\imediarenderer_getmuteasync.htm
tech.root: mediastreaming
ms.assetid: 411CAF71-2888-46A3-8777-80B0D6D9CDE5
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetMuteAsync, GetMuteAsync method [Media Streaming API], GetMuteAsync method [Media Streaming API],IMediaRenderer interface, IMediaRenderer interface [Media Streaming API],GetMuteAsync method, IMediaRenderer.GetMuteAsync, IMediaRenderer.streaming, IMediaRenderer::GetMuteAsync, IMediaRenderer::streaming, mediastreaming.imediarenderer_getmuteasync, windows/IMediaRenderer::GetMuteAsync
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
 - IMediaRenderer.GetMuteAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Queries the DMR asynchronously to determine if audio is currently muted or unmuted.


## -parameters




### -param value [out]

Receives a reference to a  <a href="https://msdn.microsoft.com/691D4936-604A-496F-B62E-FB36B406F0DD">GetMuteOperation</a> object that is used to get results from the asynchronous operation.


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
 

 

