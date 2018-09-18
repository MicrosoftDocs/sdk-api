---
UID: NF:windows.media.streaming.IMediaRenderer.SetSourceFromMediaSourceAsync
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Instructs the DMR asynchronously to prepare the specified content for playing.
old-location: mediastreaming\imediarenderer_setsourcefrommediasourceasync.htm
tech.root: mediastreaming
ms.assetid: AC30F3C4-30DD-41B1-B2CE-5F908588A779
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetSourceFromMediaSourceAsync method, IMediaRenderer.SetSourceFromMediaSourceAsync, IMediaRenderer.streaming, IMediaRenderer::SetSourceFromMediaSourceAsync, IMediaRenderer::streaming, SetSourceFromMediaSourceAsync, SetSourceFromMediaSourceAsync method [Media Streaming API], SetSourceFromMediaSourceAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setsourcefrommediasourceasync, windows/IMediaRenderer::SetSourceFromMediaSourceAsync
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
 - IMediaRenderer.SetSourceFromMediaSourceAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Instructs the DMR asynchronously to prepare the specified content for playing.


## -parameters




### -param mediaSource [in]

A reference to an <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> interface implementing <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a>. The <b>IMFActivate</b> interface is used to query for an <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface that represents the media source.


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
If the DMR is already playing content, it will automatically switch to the content provided by the <i>mediaSource</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

