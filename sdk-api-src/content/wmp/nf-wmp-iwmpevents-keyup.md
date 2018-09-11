---
UID: NF:wmp.IWMPEvents.KeyUp
title: IWMPEvents::KeyUp
author: windows-sdk-content
description: The KeyUp event occurs when a key is released.
old-location: wmp\iwmpevents_iwmpevents__keyup.htm
tech.root: WMP
ms.assetid: e76e11d8-6cb9-488e-b5ca-1b5b11898d4b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPEvents interface [Windows Media Player],KeyUp method, IWMPEvents.KeyUp, IWMPEvents::KeyUp, IWMPEventsKeyUp, KeyUp, KeyUp method [Windows Media Player], KeyUp method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__keyup, wmp/IWMPEvents::KeyUp
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
 - IWMPEvents.KeyUp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents::KeyUp


## -description



The <b>KeyUp</b> event occurs when a key is released.




## -parameters




### -param nKeyCode [in]

Specifies which physical key is pressed. For possible values, see the Remarks section of the <b>KeyDown</b> event.


### -param nShiftState [in]

A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2). These bits correspond to the values 1, 2, and 4, respectively. The shift argument indicates the state of these keys. Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.


## -returns



This method does not return a value.




## -remarks



<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/3759d40c-414a-4f91-93eb-0ad4a4b091b9">KeyDown</a>
 

 

