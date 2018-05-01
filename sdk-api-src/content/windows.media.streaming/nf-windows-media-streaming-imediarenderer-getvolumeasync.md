---
UID: NF:windows.media.streaming.IMediaRenderer.GetVolumeAsync
title: IMediaRenderer::GetVolumeAsync method
author: windows-driver-content
description: Queries the DMR asynchronously for its current audio volume level.
old-location: mediastreaming\imediarenderer_getvolumeasync.htm
old-project: mediastreaming
ms.assetid: CBE8E7EE-DC64-4FB0-B09D-58EC9BACCA26
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: GetVolumeAsync method [Media Streaming API], GetVolumeAsync method [Media Streaming API], IMediaRenderer interface, GetVolumeAsync,IMediaRenderer.GetVolumeAsync, IMediaRenderer, IMediaRenderer interface [Media Streaming API], GetVolumeAsync method, IMediaRenderer::GetVolumeAsync, mediastreaming.imediarenderer_getvolumeasync, windows/IMediaRenderer::GetVolumeAsync
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
-	IMediaRenderer.GetVolumeAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IMediaRenderer::GetVolumeAsync method


## -description


Queries the DMR asynchronously for its current audio volume level.


## -parameters




### -param value [out]

Receives a reference to a <a href="https://msdn.microsoft.com/F7BCE2AB-89B5-44CE-8BDF-347F2E3FD6C9">GetVolumeOperation</a> object that is used to get results from the asynchronous operation.


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
 

 

