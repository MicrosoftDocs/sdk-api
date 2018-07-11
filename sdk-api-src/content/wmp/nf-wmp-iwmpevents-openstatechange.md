---
UID: NF:wmp.IWMPEvents.OpenStateChange
title: IWMPEvents::OpenStateChange
author: windows-sdk-content
description: The OpenStateChange event occurs when the Windows Media Player control changes state.
old-location: wmp\iwmpevents_iwmpevents__openstatechange.htm
old-project: WMP
ms.assetid: 6f228bc5-39a4-4bf8-a887-43ba13c1c414
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPEvents interface [Windows Media Player],OpenStateChange method, IWMPEvents.OpenStateChange, IWMPEvents::OpenStateChange, IWMPEventsOpenStateChange, OpenStateChange, OpenStateChange method [Windows Media Player], OpenStateChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__openstatechange, wmp/IWMPEvents::OpenStateChange
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
 - IWMPEvents.OpenStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents::OpenStateChange


## -description



The <b>OpenStateChange</b> event occurs when the Windows Media Player control changes state.




## -parameters




### -param NewState [in]

Specifies the new open state.


## -returns



This method does not return a value.




## -remarks



Windows Media Player can go through several open states while it attempts to open a file over a network, such as locating the server, connecting to the server, and opening the file. This event will be fired each time the open state changes.

Windows Media Player states are not guaranteed to occur in any particular order. Furthermore, not every state necessarily occurs during a sequence of events. You should not write code that relies upon state order.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

