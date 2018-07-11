---
UID: NF:wmp.IWMPEvents.PlaylistCollectionPlaylistAdded
title: IWMPEvents::PlaylistCollectionPlaylistAdded
author: windows-sdk-content
description: The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.
old-location: wmp\iwmpevents_iwmpevents__playlistcollectionplaylistadded.htm
old-project: WMP
ms.assetid: f865021c-692b-425e-a37a-b3048f7e5c64
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPEvents interface [Windows Media Player],PlaylistCollectionPlaylistAdded method, IWMPEvents.PlaylistCollectionPlaylistAdded, IWMPEvents::PlaylistCollectionPlaylistAdded, IWMPEventsPlaylistCollectionPlaylistAdded, PlaylistCollectionPlaylistAdded, PlaylistCollectionPlaylistAdded method [Windows Media Player], PlaylistCollectionPlaylistAdded method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playlistcollectionplaylistadded, wmp/IWMPEvents::PlaylistCollectionPlaylistAdded
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/9d837c57-8612-47ef-a0fa-a3ffa77ac704">IWMPPlaylistCollection::getByName</a>
 

 

