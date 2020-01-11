---
UID: NN:wmdxva.IWMPlayerTimestampHook
title: IWMPlayerTimestampHook (wmdxva.h)
description: The IWMPlayerTimestampHook interface is implemented on a player's source filter.
old-location: wmformat\iwmplayertimestamphook.htm
tech.root: wmformat
ms.assetid: 8a1b3b1f-1c9c-429f-958e-757b383c7e2a
ms.date: 12/05/2018
ms.keywords: IWMPlayerTimestampHook, IWMPlayerTimestampHook interface [windows Media Format], IWMPlayerTimestampHook interface [windows Media Format],described, IWMPlayerTimestampHookInterface, wmdxva/IWMPlayerTimestampHook, wmformat.iwmplayertimestamphook
f1_keywords:
- wmdxva/IWMPlayerTimestampHook
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmdxva.h
api_name:
- IWMPlayerTimestampHook
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPlayerTimestampHook interface


## -description



The <b>IWMPlayerTimestampHook</b> interface is implemented on a player's source filter. It enables the filter to modify the time stamps on the samples before sending them to the renderer.

This method is provided to provide the filter with a greater degree of control over the streaming process than would otherwise be possible. Specifically, the method enables changing video time stamps to allow playback at higher rates than normal.

When DirectX video acceleration is enabled, the <b>OnSample</b> method is never called. Therefore, if you plan to play video on a different timeline than a media timeline, this is the only chance to update the time stamp on the media sample to match the timeline.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPlayerTimestampHook</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPlayerTimestampHook</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmdxva/nf-wmdxva-iwmplayertimestamphook-maptimestamp">MapTimestamp</a>
</td>
<td align="left" width="63%">
Provides the decoder with a time stamp that it will apply to the sample before delivering it to the video renderer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>
 

 

