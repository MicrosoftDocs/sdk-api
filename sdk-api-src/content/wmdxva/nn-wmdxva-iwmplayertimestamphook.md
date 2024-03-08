---
UID: NN:wmdxva.IWMPlayerTimestampHook
title: IWMPlayerTimestampHook (wmdxva.h)
description: The IWMPlayerTimestampHook interface is implemented on a player's source filter.
helpviewer_keywords: ["IWMPlayerTimestampHook","IWMPlayerTimestampHook interface [windows Media Format]","IWMPlayerTimestampHook interface [windows Media Format]","described","IWMPlayerTimestampHookInterface","wmdxva/IWMPlayerTimestampHook","wmformat.iwmplayertimestamphook"]
old-location: wmformat\iwmplayertimestamphook.htm
tech.root: wmformat
ms.assetid: 8a1b3b1f-1c9c-429f-958e-757b383c7e2a
ms.date: 4/26/2023
ms.keywords: IWMPlayerTimestampHook, IWMPlayerTimestampHook interface [windows Media Format], IWMPlayerTimestampHook interface [windows Media Format],described, IWMPlayerTimestampHookInterface, wmdxva/IWMPlayerTimestampHook, wmformat.iwmplayertimestamphook
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPlayerTimestampHook
 - wmdxva/IWMPlayerTimestampHook
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmdxva.h
api_name:
 - IWMPlayerTimestampHook
---

# IWMPlayerTimestampHook interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPlayerTimestampHook</b> interface is implemented on a player's source filter. It enables the filter to modify the time stamps on the samples before sending them to the renderer.

This method is provided to provide the filter with a greater degree of control over the streaming process than would otherwise be possible. Specifically, the method enables changing video time stamps to allow playback at higher rates than normal.

When DirectX video acceleration is enabled, the <b>OnSample</b> method is never called. Therefore, if you plan to play video on a different timeline than a media timeline, this is the only chance to update the time stamp on the media sample to match the timeline.

## -inheritance

The <b>IWMPlayerTimestampHook</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPlayerTimestampHook</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>
