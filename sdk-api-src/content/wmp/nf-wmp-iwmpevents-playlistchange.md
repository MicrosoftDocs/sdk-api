---
UID: NF:wmp.IWMPEvents.PlaylistChange
title: IWMPEvents::PlaylistChange
author: windows-sdk-content
description: The PlaylistChange event occurs when a playlist changes.
old-location: wmp\iwmpevents_iwmpevents__playlistchange.htm
tech.root: WMP
ms.assetid: a2847bda-3003-4c80-abc1-5c873d0810b7
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPEvents interface [Windows Media Player],PlaylistChange method, IWMPEvents.PlaylistChange, IWMPEvents::PlaylistChange, IWMPEventsPlaylistChange, PlaylistChange, PlaylistChange method [Windows Media Player], PlaylistChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playlistchange, wmp/IWMPEvents::PlaylistChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMPEvents.PlaylistChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents::PlaylistChange


## -description



The <b>PlaylistChange</b> event occurs when a playlist changes.




## -parameters




### -param Playlist [in]

Pointer to an <b>IDispatch</b> interface for the playlist that changed.


### -param change [in]

A <b>WMPPlaylistChangeEventType</b> enumeration value.


## -returns



This method does not return a value.




## -remarks



<b>Windows Media Player 10 Mobile: </b>This event is not supported.	 
	 




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/ebddaf22-9052-4180-9cc4-75059f9d286c">WMPPlaylistChangeEventType</a>
 

 

