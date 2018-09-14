---
UID: NF:windows.media.streaming.IMediaRenderer.SetNextSourceFromMediaSourceAsync
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Instructs the DMR asynchronously to prepare the specified content for playing once the current content has finished playing.
old-location: mediastreaming\imediarenderer_setnextsourcefrommediasourceasync.htm
tech.root: mediastreaming
ms.assetid: 054203C8-766B-4448-A275-CA61C9D177AD
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetNextSourceFromMediaSourceAsync method, IMediaRenderer.SetNextSourceFromMediaSourceAsync, IMediaRenderer.streaming, IMediaRenderer::SetNextSourceFromMediaSourceAsync, IMediaRenderer::streaming, SetNextSourceFromMediaSourceAsync, SetNextSourceFromMediaSourceAsync method [Media Streaming API], SetNextSourceFromMediaSourceAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setnextsourcefrommediasourceasync, windows/IMediaRenderer::SetNextSourceFromMediaSourceAsync
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
 - IMediaRenderer.SetNextSourceFromMediaSourceAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Instructs the DMR asynchronously to prepare the specified content for playing once the current content has finished playing.


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



Once the DMR finishes playing the current content, it will automatically switch to the content specified by the <i>mediaSource</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

