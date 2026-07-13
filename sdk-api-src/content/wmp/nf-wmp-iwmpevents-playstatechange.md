---
UID: NF:wmp.IWMPEvents.PlayStateChange
title: IWMPEvents::PlayStateChange (wmp.h)
description: The PlayStateChange event occurs when the play state of the Windows Media Player control changes.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","PlayStateChange method","IWMPEvents.PlayStateChange","IWMPEvents::PlayStateChange","IWMPEventsPlayStateChange","PlayStateChange","PlayStateChange method [Windows Media Player]","PlayStateChange method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__playstatechange","wmp/IWMPEvents::PlayStateChange"]
old-location: wmp\iwmpevents_iwmpevents__playstatechange.htm
tech.root: WMP
ms.assetid: d7bd4fde-8b08-4450-b291-1249393b5388
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],PlayStateChange method, IWMPEvents.PlayStateChange, IWMPEvents::PlayStateChange, IWMPEventsPlayStateChange, PlayStateChange, PlayStateChange method [Windows Media Player], PlayStateChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playstatechange, wmp/IWMPEvents::PlayStateChange
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
 - IWMPEvents::PlayStateChange
 - wmp/IWMPEvents::PlayStateChange
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
 - IWMPEvents.PlayStateChange
---

# IWMPEvents::PlayStateChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>PlayStateChange</b> event occurs when the play state of the Windows Media Player control changes.

## -parameters

### -param NewState [in]

Specifies the new state.

## -remarks

Windows Media Player states are not guaranteed to occur in any particular order. Furthermore, not every state necessarily occurs during a sequence of events. You should not write code that relies upon state order.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>