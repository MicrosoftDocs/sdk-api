---
UID: NF:wmp.IWMPEvents.PlaylistCollectionPlaylistRemoved
title: IWMPEvents::PlaylistCollectionPlaylistRemoved (wmp.h)
description: The PlaylistCollectionPlaylistRemoved event occurs when a playlist is removed from the playlist collection.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","PlaylistCollectionPlaylistRemoved method","IWMPEvents.PlaylistCollectionPlaylistRemoved","IWMPEvents::PlaylistCollectionPlaylistRemoved","IWMPEventsPlaylistCollectionPlaylistRemoved","PlaylistCollectionPlaylistRemoved","PlaylistCollectionPlaylistRemoved method [Windows Media Player]","PlaylistCollectionPlaylistRemoved method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__playlistcollectionplaylistremoved","wmp/IWMPEvents::PlaylistCollectionPlaylistRemoved"]
old-location: wmp\iwmpevents_iwmpevents__playlistcollectionplaylistremoved.htm
tech.root: WMP
ms.assetid: 53b7e883-f392-4a07-8952-ab7a6e9c436e
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],PlaylistCollectionPlaylistRemoved method, IWMPEvents.PlaylistCollectionPlaylistRemoved, IWMPEvents::PlaylistCollectionPlaylistRemoved, IWMPEventsPlaylistCollectionPlaylistRemoved, PlaylistCollectionPlaylistRemoved, PlaylistCollectionPlaylistRemoved method [Windows Media Player], PlaylistCollectionPlaylistRemoved method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playlistcollectionplaylistremoved, wmp/IWMPEvents::PlaylistCollectionPlaylistRemoved
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
 - IWMPEvents::PlaylistCollectionPlaylistRemoved
 - wmp/IWMPEvents::PlaylistCollectionPlaylistRemoved
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
 - IWMPEvents.PlaylistCollectionPlaylistRemoved
---

# IWMPEvents::PlaylistCollectionPlaylistRemoved


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>PlaylistCollectionPlaylistRemoved</b> event occurs when a playlist is removed from the playlist collection.

## -parameters

### -param bstrPlaylistName [in]

Specifies the name of the playlist that was removed.

## -remarks

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>