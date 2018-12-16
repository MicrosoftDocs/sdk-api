---
UID: NF:wmp.IWMPEvents.PlaylistCollectionPlaylistAdded
title: IWMPEvents::PlaylistCollectionPlaylistAdded
author: windows-sdk-content
description: The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.
old-location: wmp\iwmpevents_iwmpevents__playlistcollectionplaylistadded.htm
tech.root: WMP
ms.assetid: f865021c-692b-425e-a37a-b3048f7e5c64
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPEvents interface [Windows Media Player],PlaylistCollectionPlaylistAdded method, IWMPEvents.PlaylistCollectionPlaylistAdded, IWMPEvents::PlaylistCollectionPlaylistAdded, IWMPEventsPlaylistCollectionPlaylistAdded, PlaylistCollectionPlaylistAdded, PlaylistCollectionPlaylistAdded method [Windows Media Player], PlaylistCollectionPlaylistAdded method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playlistcollectionplaylistadded, wmp/IWMPEvents::PlaylistCollectionPlaylistAdded
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.PlaylistCollectionPlaylistAdded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents::PlaylistCollectionPlaylistAdded


## -description



The <b>PlaylistCollectionPlaylistAdded</b> event occurs when a playlist is added to the playlist collection.




## -parameters




### -param bstrPlaylistName [in]

Specifies the name of the playlist that was added.


## -returns



This method does not return a value.




## -remarks



The name of the playlist that was added can be used to retrieve the corresponding <b>Playlist</b> object by using the <b>IWMPPlaylistCollection::getByName</b> method.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563310(v=VS.85).aspx">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563554(v=VS.85).aspx">IWMPPlaylistCollection::getByName</a>
 

 

