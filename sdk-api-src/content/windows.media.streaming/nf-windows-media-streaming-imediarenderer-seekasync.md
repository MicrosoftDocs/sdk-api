---
UID: NF:windows.media.streaming.IMediaRenderer.SeekAsync
title: IMediaRenderer::SeekAsync method
author: windows-driver-content
description: Instructs the DMR asynchronously to seek to a particular time offset.
old-location: mediastreaming\imediarenderer_seekasync.htm
old-project: mediastreaming
ms.assetid: 3179A942-7756-4763-A2F8-629D89D39542
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: IMediaRenderer, IMediaRenderer interface [Media Streaming API], SeekAsync method, IMediaRenderer::SeekAsync, SeekAsync method [Media Streaming API], SeekAsync method [Media Streaming API], IMediaRenderer interface, SeekAsync,IMediaRenderer.SeekAsync, mediastreaming.imediarenderer_seekasync, windows/IMediaRenderer::SeekAsync
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
-	IMediaRenderer.SeekAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IMediaRenderer::SeekAsync method


## -description


Instructs the DMR asynchronously to seek to a particular time offset.


## -parameters




### -param target [in]

A <a href="https://msdn.microsoft.com/c5defb66-819c-4796-85b5-07ed249a5d86">TimeSpan</a> value that specifies the seek offset. This value must be 0 (indicating the beginning of the content) or greater, but less than the value of <a href="https://msdn.microsoft.com/9601c1ae-3fd2-4761-8aa7-102b72ef4733">PositionInformation.TrackDuration</a> which is obtained by calling <a href="https://msdn.microsoft.com/07011C85-34C5-430A-9551-FFC7C24CCED8">GetPositionInformationAsync</a>.


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
 




## -see-also




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

