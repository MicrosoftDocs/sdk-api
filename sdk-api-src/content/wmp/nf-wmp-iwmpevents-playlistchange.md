---
UID: NF:wmp.IWMPEvents.PlaylistChange
title: IWMPEvents::PlaylistChange (wmp.h)
description: The PlaylistChange event occurs when a playlist changes.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","PlaylistChange method","IWMPEvents.PlaylistChange","IWMPEvents::PlaylistChange","IWMPEventsPlaylistChange","PlaylistChange","PlaylistChange method [Windows Media Player]","PlaylistChange method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__playlistchange","wmp/IWMPEvents::PlaylistChange"]
old-location: wmp\iwmpevents_iwmpevents__playlistchange.htm
tech.root: WMP
ms.assetid: a2847bda-3003-4c80-abc1-5c873d0810b7
ms.date: 12/05/2018
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