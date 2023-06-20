---
UID: NF:wmp.IWMPEvents.OpenPlaylistSwitch
title: IWMPEvents::OpenPlaylistSwitch (wmp.h)
description: The OpenPlaylistSwitch event occurs when a title on a DVD begins playing.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","OpenPlaylistSwitch method","IWMPEvents.OpenPlaylistSwitch","IWMPEvents::OpenPlaylistSwitch","IWMPEventsOpenPlaylistSwitch","OpenPlaylistSwitch","OpenPlaylistSwitch method [Windows Media Player]","OpenPlaylistSwitch method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__openplaylistswitch","wmp/IWMPEvents::OpenPlaylistSwitch"]
old-location: wmp\iwmpevents_iwmpevents__openplaylistswitch.htm
tech.root: WMP
ms.assetid: 08fef94e-82ef-4606-a7d5-6258fddd8717
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],OpenPlaylistSwitch method, IWMPEvents.OpenPlaylistSwitch, IWMPEvents::OpenPlaylistSwitch, IWMPEventsOpenPlaylistSwitch, OpenPlaylistSwitch, OpenPlaylistSwitch method [Windows Media Player], OpenPlaylistSwitch method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__openplaylistswitch, wmp/IWMPEvents::OpenPlaylistSwitch
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
 - IWMPEvents::OpenPlaylistSwitch
 - wmp/IWMPEvents::OpenPlaylistSwitch
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
 - IWMPEvents.OpenPlaylistSwitch
---

# IWMPEvents::OpenPlaylistSwitch


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OpenPlaylistSwitch</b> event occurs when a title on a DVD begins playing.

## -parameters

### -param pItem [in]

Pointer to an <b>IDispatch</b> interface for the given playlist.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>