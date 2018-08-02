---
UID: NF:wmp.IWMPEvents.PlayStateChange
title: IWMPEvents::PlayStateChange
author: windows-sdk-content
description: The PlayStateChange event occurs when the play state of the Windows Media Player control changes.
old-location: wmp\iwmpevents_iwmpevents__playstatechange.htm
old-project: WMP
ms.assetid: d7bd4fde-8b08-4450-b291-1249393b5388
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPEvents interface [Windows Media Player],PlayStateChange method, IWMPEvents.PlayStateChange, IWMPEvents::PlayStateChange, IWMPEventsPlayStateChange, PlayStateChange, PlayStateChange method [Windows Media Player], PlayStateChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playstatechange, wmp/IWMPEvents::PlayStateChange
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
 - IWMPEvents.PlayStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents::PlayStateChange


## -description



The <b>PlayStateChange</b> event occurs when the play state of the Windows Media Player control changes.




## -parameters




### -param NewState [in]

Specifies the new state.


## -returns



This method does not return a value.




## -remarks



Windows Media Player states are not guaranteed to occur in any particular order. Furthermore, not every state necessarily occurs during a sequence of events. You should not write code that relies upon state order.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

