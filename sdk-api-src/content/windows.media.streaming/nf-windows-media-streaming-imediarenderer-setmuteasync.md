---
UID: NF:windows.media.streaming.IMediaRenderer.SetMuteAsync
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Instructs the DMR asynchronously to either mute or unmute the audio.
old-location: mediastreaming\imediarenderer_setmuteasync.htm
tech.root: mediastreaming
ms.assetid: C043088B-5043-457A-A104-5CE0B228222A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetMuteAsync method, IMediaRenderer.SetMuteAsync, IMediaRenderer.streaming, IMediaRenderer::SetMuteAsync, IMediaRenderer::streaming, SetMuteAsync, SetMuteAsync method [Media Streaming API], SetMuteAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setmuteasync, windows/IMediaRenderer::SetMuteAsync
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
 - IMediaRenderer.SetMuteAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Instructs the DMR asynchronously to either mute or unmute the audio.




## -parameters




### -param mute [in]

A reference to a boolean value that specifies the mute setting. A value of True specifies that mute is turned on, and a value of False specifies that it is turned off.


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
 

 

