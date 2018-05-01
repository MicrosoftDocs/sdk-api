---
UID: NN:wmdxva.IWMPlayerTimestampHook
title: IWMPlayerTimestampHook
author: windows-driver-content
description: The IWMPlayerTimestampHook interface is implemented on a player's source filter.
old-location: wmformat\iwmplayertimestamphook.htm
old-project: wmformat
ms.assetid: 8a1b3b1f-1c9c-429f-958e-757b383c7e2a
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMPlayerTimestampHook, IWMPlayerTimestampHook interface [windows Media Format], IWMPlayerTimestampHook interface [windows Media Format], described, IWMPlayerTimestampHookInterface, wmdxva/IWMPlayerTimestampHook, wmformat.iwmplayertimestamphook
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmdxva.h
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
req.typenames: ASF_INDEX_IDENTIFIER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmdxva.h
api_name:
-	IWMPlayerTimestampHook
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPlayerTimestampHook interface


## -description



The <b>IWMPlayerTimestampHook</b> interface is implemented on a player's source filter. It enables the filter to modify the time stamps on the samples before sending them to the renderer.

This method is provided to provide the filter with a greater degree of control over the streaming process than would otherwise be possible. Specifically, the method enables changing video time stamps to allow playback at higher rates than normal.

When DirectX video acceleration is enabled, the <b>OnSample</b> method is never called. Therefore, if you plan to play video on a different timeline than a media timeline, this is the only chance to update the time stamp on the media sample to match the timeline.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPlayerTimestampHook</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPlayerTimestampHook</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPlayerTimestampHook</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67da583f-85da-4a09-be2c-44cf96bf51e7">MapTimestamp</a>
</td>
<td align="left" width="63%">
Provides the decoder with a time stamp that it will apply to the sample before delivering it to the video renderer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>
 

 

