---
UID: NF:wmp.IWMPEvents.CurrentPlaylistItemAvailable
title: IWMPEvents::CurrentPlaylistItemAvailable
author: windows-sdk-content
description: The CurrentPlaylistItemAvailable event occurs when the current playlist item becomes available.
old-location: wmp\iwmpevents_iwmpevents__currentplaylistitemavailable.htm
old-project: WMP
ms.assetid: 77209df0-3b3d-4fc8-b560-a2c02138e746
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: CurrentPlaylistItemAvailable, CurrentPlaylistItemAvailable method [Windows Media Player], CurrentPlaylistItemAvailable method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],CurrentPlaylistItemAvailable method, IWMPEvents.CurrentPlaylistItemAvailable, IWMPEvents::CurrentPlaylistItemAvailable, IWMPEventsCurrentPlaylistItemAvailable, wmp.iwmpevents_iwmpevents__currentplaylistitemavailable, wmp/IWMPEvents::CurrentPlaylistItemAvailable
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
 - IWMPEvents.CurrentPlaylistItemAvailable
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents::CurrentPlaylistItemAvailable


## -description



The <b>CurrentPlaylistItemAvailable</b> event occurs when the current playlist item becomes available.




## -parameters




### -param bstrItemName [in]

Specifies the item name.


## -returns



This method does not return a value.




## -remarks



The name of the current playlist can be used to retrieve the corresponding <b>Playlist</b> object by using the <b>IWMPPlaylistCollection::getByName</b> method.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/9d837c57-8612-47ef-a0fa-a3ffa77ac704">IWMPPlaylistCollection::getByName</a>
 

 

