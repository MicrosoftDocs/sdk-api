---
UID: NF:wmp.IWMPEvents.SwitchedToControl
title: IWMPEvents::SwitchedToControl (wmp.h)
description: The SwitchedToControl event occurs when a remoted Windows Media Player control switches to the docked state.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","SwitchedToControl method","IWMPEvents.SwitchedToControl","IWMPEvents::SwitchedToControl","IWMPEventsSwitchedToControl","SwitchedToControl","SwitchedToControl method [Windows Media Player]","SwitchedToControl method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__switchedtocontrol","wmp/IWMPEvents::SwitchedToControl"]
old-location: wmp\iwmpevents_iwmpevents__switchedtocontrol.htm
tech.root: WMP
ms.assetid: 3f6d6a77-8d8a-4ed8-8222-95086c08037c
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],SwitchedToControl method, IWMPEvents.SwitchedToControl, IWMPEvents::SwitchedToControl, IWMPEventsSwitchedToControl, SwitchedToControl, SwitchedToControl method [Windows Media Player], SwitchedToControl method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__switchedtocontrol, wmp/IWMPEvents::SwitchedToControl
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
 - IWMPEvents::SwitchedToControl
 - wmp/IWMPEvents::SwitchedToControl
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
 - IWMPEvents.SwitchedToControl
---

# IWMPEvents::SwitchedToControl


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SwitchedToControl</b> event occurs when a remoted Windows Media Player control switches to the docked state.



## -remarks

This event occurs only when remoting the Windows Media Player control, and only occurs for the Player control instance being switched to.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>
