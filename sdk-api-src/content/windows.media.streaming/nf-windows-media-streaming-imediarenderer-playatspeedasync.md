---
UID: NF:windows.media.streaming.IMediaRenderer.PlayAtSpeedAsync
title: IMediaRenderer::streaming (windows.media.streaming.h)
author: windows-sdk-content
description: Instructs the DMR asynchronously to play the content that was specified by calling the SetSourceFromUriAsync, SetSourceFromStreamAsync, or SetSourceFromMediaSourceAsync method at the specified rate.
old-location: mediastreaming\imediarenderer_playatspeedasync.htm
tech.root: mediastreaming
ms.assetid: 368510CF-FC36-4D92-AE92-024D53EE3BAD
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],PlayAtSpeedAsync method, IMediaRenderer.PlayAtSpeedAsync, IMediaRenderer.streaming, IMediaRenderer::PlayAtSpeedAsync, IMediaRenderer::streaming, PlayAtSpeedAsync, PlayAtSpeedAsync method [Media Streaming API], PlayAtSpeedAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_playatspeedasync, windows/IMediaRenderer::PlayAtSpeedAsync
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
 - IMediaRenderer.PlayAtSpeedAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Instructs the DMR asynchronously to play the content that was specified by calling the <a href="https://msdn.microsoft.com/3062FC13-61FD-4781-9AE6-39576D86B783">SetSourceFromUriAsync</a>, <a href="https://msdn.microsoft.com/BBFEDCE1-A7C4-4F7E-AC22-0F117EA075CE">SetSourceFromStreamAsync</a>, or <a href="https://msdn.microsoft.com/AC30F3C4-30DD-41B1-B2CE-5F908588A779">SetSourceFromMediaSourceAsync</a> method at the specified rate.


## -parameters




### -param playSpeed [in]

The rate at which the DMR will be instructed to play the content. This value must correspond to one of the values returned by the <a href="https://msdn.microsoft.com/0AB63E39-6A26-4199-9978-A10866A7C805">IMediaRendererActionInformation::PlaySpeeds</a> method.


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



Before this method is called, you must call <a href="https://msdn.microsoft.com/3062FC13-61FD-4781-9AE6-39576D86B783">SetSourceFromUriAsync</a>, <a href="https://msdn.microsoft.com/BBFEDCE1-A7C4-4F7E-AC22-0F117EA075CE">SetSourceFromStreamAsync</a>, or <a href="https://msdn.microsoft.com/AC30F3C4-30DD-41B1-B2CE-5F908588A779">SetSourceFromMediaSourceAsync</a> first to specify the content.




## -see-also




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

