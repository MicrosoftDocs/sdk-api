---
UID: NF:windows.media.streaming.IMediaRenderer.SetSourceFromUriAsync
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing.
old-location: mediastreaming\imediarenderer_setsourcefromuriasync.htm
tech.root: mediastreaming
ms.assetid: 3062FC13-61FD-4781-9AE6-39576D86B783
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetSourceFromUriAsync method, IMediaRenderer.SetSourceFromUriAsync, IMediaRenderer.streaming, IMediaRenderer::SetSourceFromUriAsync, IMediaRenderer::streaming, SetSourceFromUriAsync, SetSourceFromUriAsync method [Media Streaming API], SetSourceFromUriAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setsourcefromuriasync, windows/IMediaRenderer::SetSourceFromUriAsync
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
 - IMediaRenderer.SetSourceFromUriAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Instructs the DMR asynchronously to prepare the content identified by the specified URI for playing.


## -parameters




### -param URI [in]

An HSTRING containing the file path or resource location of media content.


### -param value [out]

Receives a reference to a <a href="https://msdn.microsoft.com/4899254A-C393-4D03-970F-CF272F4761B6">PlaybackOperation</a> object that is used to get results from the asynchronous operation.


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



If the DMR is not currently playing anything, the <a href="https://msdn.microsoft.com/32084664-2D1B-4303-B3B7-9B896A07CB17">PlayAsync</a> or <a href="https://msdn.microsoft.com/368510CF-FC36-4D92-AE92-024D53EE3BAD">PlayAtSpeedAsync</a> method must be used to instruct the DMR to start playing.  
If the DMR is already playing content, it will automatically switch to the content provided by the <i>URI</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

