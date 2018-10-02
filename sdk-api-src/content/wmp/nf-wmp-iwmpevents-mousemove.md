---
UID: NF:wmp.IWMPEvents.MouseMove
title: IWMPEvents::MouseMove
author: windows-sdk-content
description: The MouseMove event occurs when the mouse pointer is moved.
old-location: wmp\iwmpevents_iwmpevents__mousemove.htm
tech.root: WMP
ms.assetid: ca0b438f-2093-41b0-9170-ec59656b70e1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPEvents interface [Windows Media Player],MouseMove method, IWMPEvents.MouseMove, IWMPEvents::MouseMove, IWMPEventsMouseMove, MouseMove, MouseMove method [Windows Media Player], MouseMove method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__mousemove, wmp/IWMPEvents::MouseMove
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
 - IWMPEvents.MouseMove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents::MouseMove


## -description



The <b>MouseMove</b> event occurs when the mouse pointer is moved.




## -parameters




### -param nButton [in]

A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2). These bits correspond to the values 1, 2, and 4, respectively. Some, all, or none of the bits can be set, indicating that some, all, or none of the buttons are pressed.


### -param nShiftState [in]

A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2). These bits correspond to the values 1, 2, and 4, respectively. The shift argument indicates the state of these keys. Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.


### -param fX [in]

The <i>x</i> coordinate of the mouse pointer relative to the upper-left corner of the control.


### -param fY [in]

The <i>y</i> coordinate of the mouse pointer relative to the upper-left corner of the control.


## -returns



This method does not return a value.




## -remarks



<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/4fbf1fdf-3d15-4d43-b319-5c83712e7f2f">MouseDown</a>
 

 

