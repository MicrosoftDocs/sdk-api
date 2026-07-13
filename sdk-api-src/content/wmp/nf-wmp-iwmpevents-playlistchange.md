---
UID: NF:wmp.IWMPEvents.PlaylistChange
title: IWMPEvents::PlaylistChange (wmp.h)
description: The PlaylistChange event occurs when a playlist changes.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","PlaylistChange method","IWMPEvents.PlaylistChange","IWMPEvents::PlaylistChange","IWMPEventsPlaylistChange","PlaylistChange","PlaylistChange method [Windows Media Player]","PlaylistChange method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__playlistchange","wmp/IWMPEvents::PlaylistChange"]
old-location: wmp\iwmpevents_iwmpevents__playlistchange.htm
tech.root: WMP
ms.assetid: a2847bda-3003-4c80-abc1-5c873d0810b7
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],PlaylistChange method, IWMPEvents.PlaylistChange, IWMPEvents::PlaylistChange, IWMPEventsPlaylistChange, PlaylistChange, PlaylistChange method [Windows Media Player], PlaylistChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playlistchange, wmp/IWMPEvents::PlaylistChange
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
 - IWMPEvents::PlaylistChange
 - wmp/IWMPEvents::PlaylistChange
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
 - IWMPEvents.PlaylistChange
---

# IWMPEvents::PlaylistChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>PlaylistChange</b> event occurs when a playlist changes.

## -parameters

### -param Playlist [in]

Pointer to an <b>IDispatch</b> interface for the playlist that changed.

### -param change [in]

A <b>WMPPlaylistChangeEventType</b> enumeration value.

## -remarks

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype">WMPPlaylistChangeEventType</a>