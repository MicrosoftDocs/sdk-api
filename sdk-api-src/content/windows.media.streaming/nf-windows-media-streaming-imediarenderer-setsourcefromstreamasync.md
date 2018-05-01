---
UID: NF:windows.media.streaming.IMediaRenderer.SetSourceFromStreamAsync
title: IMediaRenderer::SetSourceFromStreamAsync method
author: windows-driver-content
description: Instructs the DMR asynchronously to prepare the specified media stream for playing.
old-location: mediastreaming\imediarenderer_setsourcefromstreamasync.htm
old-project: mediastreaming
ms.assetid: BBFEDCE1-A7C4-4F7E-AC22-0F117EA075CE
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: IMediaRenderer, IMediaRenderer interface [Media Streaming API], SetSourceFromStreamAsync method, IMediaRenderer::SetSourceFromStreamAsync, SetSourceFromStreamAsync method [Media Streaming API], SetSourceFromStreamAsync method [Media Streaming API], IMediaRenderer interface, SetSourceFromStreamAsync,IMediaRenderer.SetSourceFromStreamAsync, mediastreaming.imediarenderer_setsourcefromstreamasync, windows/IMediaRenderer::SetSourceFromStreamAsync
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
req.typenames: TimeSpan
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	windows.media.streaming.h
api_name:
-	IMediaRenderer.SetSourceFromStreamAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IMediaRenderer::SetSourceFromStreamAsync method


## -description


Instructs the DMR asynchronously to prepare the specified media stream for playing.


## -parameters




### -param stream [in]

A reference to an <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> interface implementing <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a>. The <b>IMFActivate</b> interface is used to query for an <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface that represents the media stream.


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
If the DMR is already playing content, it will automatically switch to the content provided by the <i>stream</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

