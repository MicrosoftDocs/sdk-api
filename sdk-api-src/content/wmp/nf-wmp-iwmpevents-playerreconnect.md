---
UID: NF:wmp.IWMPEvents.PlayerReconnect
title: IWMPEvents::PlayerReconnect (wmp.h)
description: The PlayerReconnect event occurs when a remoted Windows Media Player control reconnects to the Player.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","PlayerReconnect method","IWMPEvents.PlayerReconnect","IWMPEvents::PlayerReconnect","IWMPEventsPlayerReconnect","PlayerReconnect","PlayerReconnect method [Windows Media Player]","PlayerReconnect method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__playerreconnect","wmp/IWMPEvents::PlayerReconnect"]
old-location: wmp\iwmpevents_iwmpevents__playerreconnect.htm
tech.root: WMP
ms.assetid: 16e9aa76-8ecf-471e-a30c-b8cf834cee0e
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],PlayerReconnect method, IWMPEvents.PlayerReconnect, IWMPEvents::PlayerReconnect, IWMPEventsPlayerReconnect, PlayerReconnect, PlayerReconnect method [Windows Media Player], PlayerReconnect method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playerreconnect, wmp/IWMPEvents::PlayerReconnect
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
 - IWMPEvents::PlayerReconnect
 - wmp/IWMPEvents::PlayerReconnect
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
 - IWMPEvents.PlayerReconnect
---

# IWMPEvents::PlayerReconnect


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>PlayerReconnect</b> event occurs when a remoted Windows Media Player control reconnects to the Player.



## -remarks

This event occurs only when remoting the Windows Media Player control.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>
