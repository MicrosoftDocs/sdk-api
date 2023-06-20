---
UID: NF:wmp.IWMPEvents.OpenStateChange
title: IWMPEvents::OpenStateChange (wmp.h)
description: The OpenStateChange event occurs when the Windows Media Player control changes state.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","OpenStateChange method","IWMPEvents.OpenStateChange","IWMPEvents::OpenStateChange","IWMPEventsOpenStateChange","OpenStateChange","OpenStateChange method [Windows Media Player]","OpenStateChange method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__openstatechange","wmp/IWMPEvents::OpenStateChange"]
old-location: wmp\iwmpevents_iwmpevents__openstatechange.htm
tech.root: WMP
ms.assetid: 6f228bc5-39a4-4bf8-a887-43ba13c1c414
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],OpenStateChange method, IWMPEvents.OpenStateChange, IWMPEvents::OpenStateChange, IWMPEventsOpenStateChange, OpenStateChange, OpenStateChange method [Windows Media Player], OpenStateChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__openstatechange, wmp/IWMPEvents::OpenStateChange
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents::OpenStateChange
 - wmp/IWMPEvents::OpenStateChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.OpenStateChange
---

# IWMPEvents::OpenStateChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OpenStateChange</b> event occurs when the Windows Media Player control changes state.

## -parameters

### -param NewState [in]

Specifies the new open state.

## -remarks

Windows Media Player can go through several open states while it attempts to open a file over a network, such as locating the server, connecting to the server, and opening the file. This event will be fired each time the open state changes.

Windows Media Player states are not guaranteed to occur in any particular order. Furthermore, not every state necessarily occurs during a sequence of events. You should not write code that relies upon state order.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>