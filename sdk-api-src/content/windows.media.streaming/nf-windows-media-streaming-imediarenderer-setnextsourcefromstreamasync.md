---
UID: NF:windows.media.streaming.IMediaRenderer.SetNextSourceFromStreamAsync
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Instructs the DMR asynchronously to prepare the specified media stream for playing once the current content has finished playing.
old-location: mediastreaming\imediarenderer_setnextsourcefromstreamasync.htm
tech.root: mediastreaming
ms.assetid: 602B4C9B-88A3-4D91-9330-FC02E62F723A
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetNextSourceFromStreamAsync method, IMediaRenderer.SetNextSourceFromStreamAsync, IMediaRenderer.streaming, IMediaRenderer::SetNextSourceFromStreamAsync, IMediaRenderer::streaming, SetNextSourceFromStreamAsync, SetNextSourceFromStreamAsync method [Media Streaming API], SetNextSourceFromStreamAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setnextsourcefromstreamasync, windows/IMediaRenderer::SetNextSourceFromStreamAsync
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
 - IMediaRenderer.SetNextSourceFromStreamAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Instructs the DMR asynchronously to prepare the specified media stream for playing once the current content has finished playing.


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



Once the DMR finishes playing the current content, it will automatically switch to the content specified by the <i>stream</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

