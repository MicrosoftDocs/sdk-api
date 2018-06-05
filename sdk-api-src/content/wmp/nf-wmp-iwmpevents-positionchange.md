---
UID: NF:wmp.IWMPEvents.PositionChange
title: IWMPEvents::PositionChange
author: windows-sdk-content
description: The PositionChange event occurs when the current playback position within the media item has been changed.
old-location: wmp\iwmpevents_iwmpevents__positionchange.htm
old-project: WMP
ms.assetid: 644aaab0-8028-4dd2-9f56-f97db2b22d69
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPEvents interface [Windows Media Player],PositionChange method, IWMPEvents.PositionChange, IWMPEvents::PositionChange, IWMPEventsPositionChange, PositionChange, PositionChange method [Windows Media Player], PositionChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__positionchange, wmp/IWMPEvents::PositionChange
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPEvents.PositionChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents::PositionChange


## -description



The <b>PositionChange</b> event occurs when the current playback position within the media item has been changed.




## -parameters




### -param oldPosition [in]

Specifies the original position.


### -param newPosition [in]

Specifies the new position.


## -returns



This method does not return a value.




## -remarks



This event is not raised routinely during playback. It only occurs when something actively changes the current playback position within the playing media item, such as the user moving the seek handle or code specifying a value for <b>IWMPControls::currentPosition</b>.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

