---
UID: NF:wmp.IWMPEvents.DoubleClick
title: IWMPEvents::DoubleClick
author: windows-sdk-content
description: The DoubleClick event occurs when the user double-clicks a mouse button.
old-location: wmp\iwmpevents_iwmpevents__doubleclick.htm
old-project: WMP
ms.assetid: 76b1eebb-45d9-40fc-a845-24a7dac8c96c
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: DoubleClick, DoubleClick method [Windows Media Player], DoubleClick method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],DoubleClick method, IWMPEvents.DoubleClick, IWMPEvents::DoubleClick, IWMPEventsDoubleClick, wmp.iwmpevents_iwmpevents__doubleclick, wmp/IWMPEvents::DoubleClick
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPEvents.DoubleClick
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents::DoubleClick


## -description



The <b>DoubleClick</b> event occurs when the user double-clicks a mouse button.




## -parameters




### -param nButton [in]

A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2). These bits correspond to the values 1, 2, and 4, respectively. Only one of the bits is set, indicating the button that caused the event.


### -param nShiftState [in]

A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2). These bits correspond to the values 1, 2, and 4, respectively. The shift argument indicates the state of these keys. Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.


### -param fX [in]

The x coordinate of the mouse pointer relative to the upper left-hand corner of the control.


### -param fY [in]

The y coordinate of the mouse pointer relative to the upper left-hand corner of the control.


## -returns



This method does not return a value.




## -remarks



<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

