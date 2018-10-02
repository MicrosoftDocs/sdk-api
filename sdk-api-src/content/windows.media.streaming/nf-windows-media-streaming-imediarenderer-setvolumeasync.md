---
UID: NF:windows.media.streaming.IMediaRenderer.SetVolumeAsync
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Sets the audio volume level on the DMR asynchronously to the specified value.
old-location: mediastreaming\imediarenderer_setvolumeasync.htm
tech.root: mediastreaming
ms.assetid: 422668F3-F5D6-440A-8BF1-A85B17E9A853
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],SetVolumeAsync method, IMediaRenderer.SetVolumeAsync, IMediaRenderer.streaming, IMediaRenderer::SetVolumeAsync, IMediaRenderer::streaming, SetVolumeAsync, SetVolumeAsync method [Media Streaming API], SetVolumeAsync method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_setvolumeasync, windows/IMediaRenderer::SetVolumeAsync
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
 - IMediaRenderer.SetVolumeAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Sets the audio volume level on the DMR asynchronously to the specified value.


## -parameters




### -param volume [in]

A reference to the specified volume value.  The value must be in the range of 0 to 100, with 0 being the minimum volume and 100 being the maximum volume.


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
 

 

