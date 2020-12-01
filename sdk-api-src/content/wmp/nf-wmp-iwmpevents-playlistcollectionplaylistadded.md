---
UID: NF:wmp.IWMPEvents.PlaylistCollectionPlaylistAdded
title: IWMPEvents::PlaylistCollectionPlaylistAdded (wmp.h)
description: The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","PlaylistCollectionPlaylistAdded method","IWMPEvents.PlaylistCollectionPlaylistAdded","IWMPEvents::PlaylistCollectionPlaylistAdded","IWMPEventsPlaylistCollectionPlaylistAdded","PlaylistCollectionPlaylistAdded","PlaylistCollectionPlaylistAdded method [Windows Media Player]","PlaylistCollectionPlaylistAdded method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__playlistcollectionplaylistadded","wmp/IWMPEvents::PlaylistCollectionPlaylistAdded"]
old-location: wmp\iwmpevents_iwmpevents__playlistcollectionplaylistadded.htm
tech.root: WMP
ms.assetid: f865021c-692b-425e-a37a-b3048f7e5c64
ms.date: 12/05/2018
ms.keywords: IWMPEvents interface [Windows Media Player],PlaylistCollectionPlaylistAdded method, IWMPEvents.PlaylistCollectionPlaylistAdded, IWMPEvents::PlaylistCollectionPlaylistAdded, IWMPEventsPlaylistCollectionPlaylistAdded, PlaylistCollectionPlaylistAdded, PlaylistCollectionPlaylistAdded method [Windows Media Player], PlaylistCollectionPlaylistAdded method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playlistcollectionplaylistadded, wmp/IWMPEvents::PlaylistCollectionPlaylistAdded
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
 - IWMPEvents::PlaylistCollectionPlaylistAdded
 - wmp/IWMPEvents::PlaylistCollectionPlaylistAdded
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
 - IWMPEvents.PlaylistCollectionPlaylistAdded
---

# IWMPEvents::PlaylistCollectionPlaylistAdded


## -description

The <b>PlaylistCollectionPlaylistAdded</b> event occurs when a playlist is added to the playlist collection.

## -parameters

### -param bstrPlaylistName [in]

Specifies the name of the playlist that was added.

## -remarks

The name of the playlist that was added can be used to retrieve the corresponding <b>Playlist</b> object by using the <b>IWMPPlaylistCollection::getByName</b> method.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-getbyname">IWMPPlaylistCollection::getByName</a>